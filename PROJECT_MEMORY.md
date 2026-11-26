# DEZZTA CHART — AI Agent Project Memory

Last reconciled: 2026-11-26 (Asia/Jakarta)
Purpose: durable context for automated work. This file is a project handoff, not permission to bypass gates.

## Repositories and immutable boundaries

- Application: `deszztagd377-pixel/dezzta-chart`.
- Only approved application branch: `phase-2/market-data-foundation`.
- Never checkout for writing, commit to, merge into, or otherwise modify application `main`.
- Runner: `deszztagd377-pixel/dezzta-chart-runner`, default branch `main`.
- Keep `.github/workflows/preflight.yml` as a separate safe preflight workflow.
- `.github/workflows/batch89-runtime-gate.yml` is manual/heavyweight. Never schedule it or invoke it every 10 minutes.
- Inspect current refs, files, workflow state, and exact-head CI before each task. This document may become stale; repository evidence wins.

## Current verified application checkpoint

- Active branch: `phase-2/market-data-foundation`.
- Branch HEAD at handoff: `6c610c4de75649126764e0aea200abf09b103521`.
- Current project ledger: `PROJECT_STATUS.md`, whose top checkpoint is Batch 91 (26 Nov 2026).
- Batch 91 status: IMPLEMENTATION IN PROGRESS — NOT ACCEPTED. Do not claim acceptance until all exact-head CI checks are terminal SUCCESS on the current HEAD.
- Batch 91 work concerns provider-neutral protocol metadata/validators, canonical cursor and SHA-256 validation, canonical event digest encoding, snapshot/stream metadata, synthetic-only canonical bar/snapshot/update builders, REST OHLCV exact-series identity, WebSocket status-first auth/subscribe/snapshot/update and versioned text ping/pong, plus Worker/Miniflare/Durable Object regression coverage.
- The most recent project ledger reports the latest exact-head CI as running for Automated Tests, CodeQL and OCI ARM64; Full Git History Secret Audit succeeded. Re-query CI and compare every run's head SHA before declaring the batch accepted.
- Snapshot/live boundary is serialized through a Durable Object-local operation queue. This is synthetic-proof coordination only, not durable replay/ACK storage.
- Batch 92 scope includes durable event payload/digest/high-water, bounded replay, ACK receipt persistence and resume recovery. Batch 92/93 remain gated behind Batch 91 acceptance.
- Project stage accounting in the current ledger: Stage 1 remains official active at 30/40 criteria (75% provisional); Gate 10 is 0/10 formally closed. Do not infer overall project percentage or stage transitions from a batch.
- Delivery target is approximately 24 December 2026, a planning target only.

## Product requirements and feature constraints

- Product: mobile-first financial charting application named DEZZTA CHART.
- Strict ZERO COST objective: no paid hosting, subscriptions, publication fees, market-data vendors or paid services. Verify current free quotas and fail closed when a free quota is unavailable. Do not activate billing or recommend paid services as a default.
- No live market provider or production feed may be represented as implemented unless lawful source, provenance, reliability and integration acceptance are proven.
- No broker/order execution endpoints, production credentials, or Firebase production auth/entitlement changes without a separately reviewed scope and owner approval.
- Existing indicator foundations noted in the ledger: SMA20, EMA20, RSI14 Wilder, MACD12/26/9, Bollinger20, and Shared Indicator Hook. Foundation tests do not imply visible chart integration.
- Footprint PRO 2GD remains synthetic/reference-gated. Owner reference visuals show a dark chart, red/green bid-ask volume cells, numeric volume labels, horizontal volume bars, highlighted price rows, candlesticks and deliberate candle-cluster spacing. Normal candles must remain unchanged when Footprint is OFF; only the enabled Footprint mode may use spaced clusters. Never claim synthetic volume is exchange-native bid/ask truth.
- Heatmap, Liquidation Maps and advanced Volume Profile variants remain open until requirements, data provenance and reviewed designs are satisfied.
- Major UI/feature expansion requires a scoped blueprint and owner review. Expansion gate may start at 40% overall progress, but do not invent an overall score; the current ledger may show it as NOT SCORED.
- Preserve working features. No destructive migrations, retention changes, data deletion or production deployment without explicit approval.

## Work protocol for the AI agent

1. Read this file and the latest `PROJECT_STATUS.md` on the approved application branch.
2. Reconcile actual branch HEAD, recent commits, open PRs, exact-head CI and the current batch ledger. Treat stale memory as a warning, not authority.
3. Work only on one small, dependency-ordered, explicitly recorded task at a time. If there is no approved actionable task, do a read-only audit and report NO_TASK; do not invent work.
4. Never skip a batch, gate, acceptance criterion or review requirement.
5. Before editing, inspect relevant source, tests, docs and callers. Do not invent APIs or repository paths.
6. Do not execute arbitrary shell commands derived from model output. Any proposed change must be a bounded patch to allowlisted paths; reject absolute paths, traversal, binary changes, workflow/secret/config changes and unreviewed dependency changes.
7. Run the smallest relevant tests, then required project checks when practical. Report exact commands and outcomes. A passing parent SHA does not validate a new HEAD.
8. Default output is a patch/branch and a pull request for owner review. Never merge automatically. Never push directly to application `main`. If write credentials are unavailable, produce a patch artifact/report only.
9. Update project status/checkpoint only with evidence. Include changed files, commit/PR, exact SHA, test results, pending blockers and next stage-ordered task.
10. Do not reveal secrets, request users to paste secrets in chat, or commit credentials. Never read or print secret values.

## Automation and credentials boundary

- Existing relay dispatches the Runner's safe Preflight workflow; that successful preflight is not AI coding.
- A separate AI workflow/model is not this ChatGPT session or GPT-6 and has no automatic access to ChatGPT memory. This file is the explicit memory handoff.
- AI inference and app-repository PR creation require separately configured, least-privilege GitHub Actions secrets. Until they exist and are validated, the AI workflow must stop safely without attempting model calls or writes.
- Do not alter cron-job.org cadence, Cloudflare Worker secrets/configuration, or relay dispatch target without explicit owner approval.
- Do not assume every 10-minute trigger should invoke inference. Run only when a bounded task is queued and within the verified free quota.
- Never trigger Batch 89 on the recurring schedule.

## Session handoff format

- Current stage/batch and exact app branch HEAD.
- Verified completed work versus provisional/in-progress work.
- Files changed/added and commit SHA or PR URL.
- Exact tests/checks and terminal results.
- Errors, blockers, missing credentials or quota limits.
- Next action in dependency order.
