# DEZZTA CHART Runner

Zero-cost automation and validation scaffold for DEZZTA CHART. It does not provide autonomous background coding.

## Application repository and branch policy

- Application repository: `deszztagd377-pixel/dezzta-chart`.
- Approved integration base: `phase-2/market-data-foundation`.
- Feature work must occur on a reviewed work branch and be proposed through a pull request against the integration base.
- Never write to the application repository's `main`.
- Active PR #13 is `work/batch95-websocket-ack-protocol`; current app checkpoint and exact CI evidence are recorded in the top of `PROJECT_BRAIN.md`. Its branch is currently non-mergeable and must not be force-pushed or merged blindly.

## Workflow inventory and safe use

- `.github/workflows/preflight.yml`: manual, read-only preflight. It checks out the integration base; it does not install dependencies, run tests, edit files, push commits, or validate the active PR branch.
- `.github/workflows/batch89-runtime-gate.yml`: heavyweight manual validation for an older batch. Do not dispatch it for current PR #13 without a new, explicit approval and an updated source/branch contract.
- `.github/workflows/ai-coding-runner.yml`: legacy gated scaffold. It references Batch 91 acceptance and the integration-base Project Brain SHA; it does not currently generate or apply code. Do not treat its presence as an active coding agent.
- `.github/workflows/ai-project-audit.yml` and `ai-agent-smoke-test.yml`: manual Cloudflare Workers AI calls. They require credentials and consume a service quota; do not assume they are zero-cost or trigger them without a separately verified free allowance and approval.

## Automation cancellation — owner instruction

**The recurring 10-minute automation is cancelled.** Do not create, enable, or replace any cron-job.org schedule, Cloudflare Cron Trigger, GitHub schedule, or recurring relay dispatch. Do not route the relay to Preflight, Batch 89, or AI coding. The existing relay configuration must remain untouched/inert unless the owner separately instructs otherwise. External cron-job.org account state is not accessible from this repository, so do not claim it was verified.

## Current project constraints

- Official stage: Stage 1 only, 30/40 provisional; Gate 10 0/10 formally closed. Stage 2 is blocked until Stage 1 reaches 40/40 and the owner explicitly approves.
- No Footprint, Volume Profile, or Heatmap feature development during Stage 1; foundation work only.
- Delivery target: 24 December 2026.
- ZERO COST: no paid plans, trials, services, model APIs, infrastructure or billing changes.
- Never claim a workflow is running or successful without querying its exact commit and terminal status. Do not claim unattended waiting or background work.

## Relay boundary

The deployed Worker relay is documented as `https://dezzta-chart-runner-relay.deszztagd377.workers.dev`, but its configuration must not be changed or repurposed. A successful health check proves only that the Worker responds; it does not prove that an external scheduler is configured. No recurring trigger is authorized.

## Secrets and safety

- Keep secrets in approved GitHub Actions or Cloudflare secret storage; never commit or paste values into chat.
- Do not read, print, rotate, delete, or repurpose relay secrets as part of ordinary project work.
- Preserve the application feature set and require exact-head CI and owner evidence before accepting a batch.
