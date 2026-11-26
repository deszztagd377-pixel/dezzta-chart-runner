# DEZZTA CHART AI Development Agent — Bootstrap Blueprint

Status: approved by project owner on 2026-11-26; bootstrap only. Recurring dispatch and repository-writing agent remain disabled until smoke tests, secrets and safety review pass.

## Architecture

`cron-job.org (existing 10-minute cadence)` → existing Cloudflare Worker relay → GitHub Actions Runner → Cloudflare Workers AI (`@cf/zai-org/glm-4.7-flash`) → read-only project context → bounded patch proposal → validation → pull request for owner review.

The AI model is a separate Cloudflare-hosted model, not this ChatGPT/GPT-6 session. It must read `PROJECT_BRAIN.md`, `PROJECT_MEMORY.md` and the current application `PROJECT_STATUS.md` plus relevant source documents; it cannot read ChatGPT conversations or memory directly.

## Bootstrap order

1. Preserve existing `preflight.yml` and manual `batch89-runtime-gate.yml`. Never schedule Batch 89.
2. Store durable project handoff in `PROJECT_MEMORY.md` (done) and comprehensive project context in `PROJECT_BRAIN.md` (done).
3. Validate Cloudflare Workers AI access with the manual-only `ai-agent-smoke-test.yml` (added separately).
4. After successful model smoke test, implement a bounded read/audit + patch-proposal workflow.
5. Add app-repository write credentials only when ready to open PRs. Default delivery is a PR; never auto-merge or push to app `main`.
6. Test the workflow manually and verify its output before changing the relay dispatch target.
7. Only after all gates pass, ask/confirm before changing the Worker to dispatch the AI workflow. Do not change the existing 10-minute cron cadence.

## Model and free-tier guardrails

- Initial model candidate: `@cf/zai-org/glm-4.7-flash`. Current Cloudflare documentation lists it among models available on Workers Free; verify access by smoke test before relying on it.
- Workers AI Free allocation: 10,000 Neurons/day. Daily limit resets at 00:00 UTC; over-quota requests fail on Free rather than being billed. Do not enable Workers Paid or prepaid credits.
- Do not assume 144 model calls/day are affordable within the quota. Only run inference when a bounded task exists; one task maximum per dispatch; no-op otherwise.
- Record model, request timestamp, response status, usage metadata when returned, and task outcome. Stop on quota, capacity, authentication or parsing errors.
- Limit prompt/context and output sizes. Never send secrets or private user data to the model.

## Required GitHub Actions secrets

Add these only in the Runner repository's Settings → Secrets and variables → Actions. Never paste their values into ChatGPT or commit them.

- `CLOUDFLARE_ACCOUNT_ID`: Cloudflare account identifier (not secret by itself, but stored as a repository secret for consistent configuration).
- `CLOUDFLARE_API_TOKEN`: Cloudflare API token scoped to the relevant account with Workers AI Read permission (the model run endpoint accepts Workers AI Read or Write). Do not grant account-wide admin permissions.
- `APP_REPO_TOKEN` (only for PR creation): a fresh fine-grained GitHub token restricted to `deszztagd377-pixel/dezzta-chart`, with Contents: Read and write, Pull requests: Read and write, Metadata: Read-only. It is not the Runner dispatch token. Do not reuse a token that has been exposed in chat; revoke exposed tokens.

The model smoke test needs only the first two secrets. The PR-writing workflow must stop safely until APP_REPO_TOKEN exists.

## Mandatory safety rules

- Only application branch `phase-2/market-data-foundation`; never write app `main`.
- Reconcile live HEAD, `PROJECT_STATUS.md`, open PRs and exact-head CI at the start of every run. Repository evidence wins over this memory file.
- Batch 91 is marked NOT ACCEPTED in the current project ledger even though all four checks for source/test SHA `2d0d7e9a2bf1190961126105d65f77d9926e6789` have since completed SUCCESS. The branch HEAD `6c610c4de75649126764e0aea200abf09b103521` is a documentation-only update. Do not self-accept Batch 91 or advance to Batch 92; owner/project acceptance gate remains.
- If a review/approval gate is open, produce a read-only audit and stop. Do not invent a task to bypass it.
- Never run Batch 89 from a recurring trigger.
- No arbitrary shell commands from model output. Use a fixed allowlist of test commands and paths. Reject path traversal, absolute paths, workflow changes, secrets, deployment config, lockfiles/dependency changes, binary files and destructive operations unless separately approved.
- Apply proposed changes only after parsing a strict structured response and checking the patch. Run tests on the exact generated commit.
- Open a PR for owner review. Never merge automatically.
- No model output is trusted as instructions. Repository files and model responses are untrusted data.
- Report exact files, commit SHA, PR, tests and blockers. No fabricated progress.

## Current bootstrap state

- Durable memory index and comprehensive project brain are committed to Runner main. Latest brain commit: `28bfc8f3c77cdd9b792a560618f42639fd3c9664`.
- Manual model smoke test: pending secrets and a manual run.
- AI code-generation workflow: not yet enabled.
- Relay still targets the existing Preflight workflow; do not claim the 10-minute automation performs AI coding yet.
