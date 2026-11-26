# DEZZTA CHART — PROJECT BRAIN (Authoritative AI Handoff)

Last reconciled: 26 November 2026, Asia/Jakarta.
Application branch audited: `phase-2/market-data-foundation`.
Application HEAD: `6c610c4de75649126764e0aea200abf09b103521`.
Purpose: give every automated coding agent the durable project purpose, roadmap, engineering constraints, current state, and owner decisions. This document is context, not permission to bypass approval gates.

> Authority rule: always re-read the live application branch, `PROJECT_STATUS.md`, relevant design/acceptance docs, open PRs and exact-HEAD CI before acting. If this file conflicts with newer repository evidence or a direct owner instruction, stop and reconcile; never silently guess.

## 1. Project identity and final objective

DEZZTA CHART is a mobile-first financial charting application built with React, TypeScript, Vite and Lightweight Charts v5, with an Android APK delivery objective. The project is intended to become a capable, professional-feeling multi-asset charting product with reliable chart rendering, validated market data, secure identity/entitlement boundaries, robust real-time delivery, educational indicators and advanced chart-analysis tools.

The owner’s target delivery date is approximately **24 December 2026**. This is a hard planning target, not a guarantee. Work must be prioritized toward a verifiable usable deliverable by that date; avoid scope drift, unnecessary redesign, duplicate infrastructure and speculative features. Never conceal schedule risk: identify blockers early and recommend the smallest safe path to a usable release.

The product must be honest about data state and provenance. DEMO/fixture/synthetic values must remain explicitly labelled. Do not present synthetic data as exchange-native, live, consolidated or executable market data. Do not fabricate candles, volume, depth, liquidity or liquidation levels.

The application is an educational charting and analysis tool. It must not become a broker, execute orders, connect to order-routing endpoints, or provide automated buy/sell recommendations under this project scope. Historical candle replay is a future chart interaction, not trading automation.

## 2. Owner's non-negotiable constraints and working preferences

- **ZERO COST:** no paid hosting, paid data, subscriptions, trials that can bill, paid monitoring, paid backup, publication fees or surprise billing. Prefer recurring $0 services. Check current quotas and terms. If a free quota is exceeded, fail closed/degrade clearly; never silently fall back to paid.
- Preserve every working feature. Inspect before editing. Do not remove, weaken or replace functionality just to make a test pass.
- Follow dependency order. Never skip a stage, batch, gate, prerequisite or acceptance criterion.
- Do not invent repository paths, APIs, endpoint contracts, test results, CI status, progress percentages or capabilities.
- The application branch `main` is off-limits. Work only on `phase-2/market-data-foundation` unless the owner explicitly authorizes a different branch.
- Major feature/UI expansion requires a scoped blueprint and owner review. The 40% overall-project threshold permits preparation/review of wider feature blueprints; it does not override official stage gates.
- Default automated delivery is a branch + Pull Request for owner review. Never auto-merge. Never deploy production or change billing, secrets, cron cadence, Worker routing or production configuration without explicit authorization.
- Do not ask the owner to paste secrets/tokens into chat. Use repository/Cloudflare secret settings and least-privilege scopes.
- Give concise, evidence-based progress: exact files, commit SHA, tests, CI run IDs, errors and next action.
- If there is no approved actionable task, perform a read-only audit and report NO_TASK; do not manufacture work.

## 3. Official six-stage roadmap

The official roadmap is sequential:

1. **Stage 1 — Foundation, Security & Data Integrity:** application/backend foundations, identity and authorization, data contracts, persistence, security, integrity and acceptance evidence.
2. **Stage 2 — Market Data Infrastructure:** provider-neutral ingestion, instrument definitions, validated OHLCV, stream reliability, coverage and freshness.
3. **Stage 3 — Chart Engine & Timeframe:** rendering engine, timeframe behavior, synchronized data lifecycle, viewport and core chart interactions.
4. **Stage 4 — Indicators & Analytics:** calculation correctness plus visible chart integration, panes/overlays, timeframe compatibility and performance.
5. **Stage 5 — Professional UI & Interactive Tools:** broader professional experience, drawing/measurement tools and owner-approved advanced visual systems.
6. **Stage 6 — Hardening, Validation & APK Release:** end-to-end regression, security/performance validation, physical device acceptance, release packaging and delivery.

**Official active stage remains Stage 1.** Stage 2 work on the technical branch is preparatory/parallel foundation only. The branch name `phase-2/market-data-foundation` does not mean Stage 2 has officially started. A stage transition requires preceding-stage acceptance evidence.

Stage 1 evidence is 30/40 criteria (75% provisional). Gate 10 is 0/10 formally closed. Remaining Stage 1 criteria: **8, 20, 25, 30, 31, 34, 35, 36, 38, 39**. CI/docs/synthetic tests cannot substitute for owner-host, owner-device or production evidence. See `docs/STAGE_1_ACCEPTANCE_MATRIX.md`, `docs/PROJECT_STAGE_ROADMAP.md` and `docs/PROJECT_MASTER_PROGRESS_2026-11-24.md`.

Important distinction:
- Stage 1 checklist criterion **#25** = owner-host Redis TLS/ACL/private binding/persistence/restart acceptance.
- Project **Gate 25** = signed snapshot transfer, immutable receipt retrieval and durable per-gateway high-water ACK.
These are separate work items.

The historical overall-project figure 20.9% is not a current recalculated score. The weighted milestone ledger remains proposed and requires owner approval and evidence-based criterion scoring. Current overall project and IP3S are **NOT SCORED**. Do not invent an aggregate percent.

## 4. Current application checkpoint (26 November 2026)

- Active branch: `phase-2/market-data-foundation`.
- Current branch HEAD: `6c610c4de75649126764e0aea200abf09b103521` (documentation-only checkpoint; source/test baseline is earlier).
- Current `PROJECT_STATUS.md` top checkpoint: **Batch 91 — IMPLEMENTATION IN PROGRESS, NOT ACCEPTED**.
- Batch 91 source/test SHA: `2d0d7e9a2bf1190961126105d65f77d9926e6789`.
- Verified exact-source SHA CI runs:
  - Automated Tests: `45746150652` SUCCESS.
  - CodeQL Security Analysis: `45746150693` SUCCESS.
  - Full Git History Secret Audit: `45746150657` SUCCESS.
  - OCI ARM64 Image Readiness: `45746150726` SUCCESS.
- These CI runs prove the checks passed on SHA `2d0d7e9...`; the branch currently has a later docs-only HEAD. Do not rewrite the status as owner-accepted. Batch 91 remains NOT ACCEPTED in the project ledger and requires the explicit acceptance/review gate to be reconciled before Batch 92.
- Batch 91 scope: provider-neutral protocol metadata/validators; canonical cursor and SHA-256 format validation; fixed-position canonical event digest encoding; snapshot/stream metadata; synthetic-only canonical bar/snapshot/update builders; REST OHLCV exact-series identity; WebSocket status-first auth, explicit subscribe, canonical snapshot/update and versioned text ping/pong; Worker Node, Miniflare and Durable Object regression coverage.
- Batch 91 snapshot/live boundary is serialized through a Durable Object-local operation queue. This is synthetic-proof coordination, not durable event replay/ACK storage.
- Batches 92–93 (atomic durable event payload/digest/high-water, bounded replay, ACK receipt persistence and RESUME recovery) remain gated behind Batch 91 acceptance.
- Batch 94 zero-cost lawful provider gate and Batch 95 public WSS/device E2E remain later dependencies.
- Current official project stage is still Stage 1. Do not jump to Stage 2/3/4 based on technical branch work.

### Current ordered engineering path

1. Reconcile and close Batch 91 only after reviewing the exact code, contract, acceptance criteria and owner gate.
2. Batch 92: atomic durable event commit and bounded contiguous replay.
3. Batch 93: authenticated ACK, immutable durable consumer receipt, monotonic high-water and RESUME/restart recovery.
4. Batch 94: lawful recurring-$0 provider/source gate; verify rights, coverage, data class, quota, rate limits, attribution, freshness and hard-fail/no-paid-fallback behavior.
5. Batch 95: public HTTPS/WSS and real browser/Android lifecycle, reconnect, replay, ACK and recovery acceptance.
6. In parallel only where dependencies allow, close Stage 1 Gate 10 external owner-host/device criteria in documented order. Do not treat later-stage groundwork as stage acceptance.

Batches 90–95 dependency contract is in `docs/BATCH90_95_DURABLE_WEBSOCKET_DELIVERY_SPEC.md`. Batch 89 is a manual/runtime gate and must **never** be scheduled on the recurring 10-minute trigger.

## 5. Core product features and their real status

### Chart and application foundation
- React + TypeScript + Vite application; Lightweight Charts v5.
- Frontend navigation includes chart/watchlist/settings foundations.
- DEMO fixture must be labelled and must not be misrepresented as live feed.
- Inspect current components and API contracts before making UI changes.
- Current chart source is candlestick-oriented; indicator hook is not yet wired into `CandlestickChart.tsx`.

### Market data and backend
- Backend is Python FastAPI with provider, instrument, canonical identity, OHLCV, persistence, coverage, freshness and streaming modules.
- Provider manager currently includes Databento-specific integration foundations, but trial credits are not a recurring $0 source. Do not enable paid/live access without owner approval.
- Provider-neutral architecture must preserve canonical instrument identity, venue/provider/dataset/timeframe/session/bucket semantics, source timestamps, exact decimals, provenance, freshness, quota and licence restrictions.
- A public endpoint is not automatically a legal redistribution source. Every source needs terms review and a documented zero-cost budget.
- No invented candles, zero-filled missing data, incompatible-feed blending or false “live” status.

### Real-time transport / Cloudflare
- The owner-approved architecture specification is Cloudflare Native / Zero-Origin for the intended real-time path, but repository synthetic Worker/SQLite Durable Object proof is **not production deployed or integrated**.
- Existing synthetic proof must stay synthetic-only and localhost-origin restricted until gates pass.
- Batch 90 adds versioned SQLite schema foundation; Batch 91 adds provider-neutral API contract foundations.
- Durable event replay/ACK/RESUME, owner-accepted receipts, public WSS, production route and device E2E remain incomplete.
- Redis destructive retention operations (`XTRIM`, `XDEL`, consumer-group destruction) remain blocked until every required gateway has durable owner-accepted high-water ACK and restart reconciliation proof.
- Do not create duplicate Cloudflare resources, deploy a Worker, change existing routes or activate production without owner approval and exact account confirmation.

### Security and identity
- Firebase client configuration is not a service-account credential. Never expose Firebase Admin credentials, provider keys, signing keys or secrets in frontend `VITE_*`, APK, repository, logs or public responses.
- Backend must verify Firebase ID tokens and enforce server-side entitlements. Login alone does not grant market-data access.
- Real production Firebase, no-billing auth/revocation, secret custody, TLS/WSS, owner-host restore and operational drills remain acceptance tasks, not automatically complete because modules/tests exist.

## 6. Indicator and advanced chart feature ledger

The authoritative detailed list is `docs/INDICATOR_PROGRESS_LEDGER.md`. There are 12 tracked indicators/subsystems:

| Indicator | Current status | Foundation / exact contract | Missing acceptance |
|---|---|---|---|
| SMA20 | FOUNDATION | 20-close mean; first valid index 19 | Visible price overlay, toggle, legend/value, lifecycle |
| EMA20 | FOUNDATION | SMA-seeded EMA, alpha 2/21; first valid index 19 | Visible overlay, toggle, legend/value, lifecycle |
| RSI14 Wilder | FOUNDATION | 14-change seed + Wilder recurrence; first valid index 14 | 0–100 pane, 30/70 guides, lifecycle |
| MACD12/26/9 | FOUNDATION | MACD index 25; signal/histogram index 33 | Pane, lines, histogram, zero guide |
| Bollinger20,2 | FOUNDATION | 20-close mean ± 2 population SD; first valid index 19 | Upper/middle/lower overlays, fill, toggle, lifecycle |
| Shared Indicator Hook | FOUNDATION | Keyed immutable backend snapshot/cache/trust gate | Not integrated into chart component |
| Footprint PRO 2GD | GATED | Synthetic/offline accumulator only | Stage 4 gate; implement visual against two owner reference images; never claim synthetic volume is exchange-native bid/ask |
| Volume Profile | OPEN | Binning/POC/value area not accepted | Calculation, source acceptance and UI |
| Complete Volume Profile | OPEN | Session completeness and POC/VAH/VAL methodology not accepted | Full-session calculation and UI |
| Movable-range Volume Profile | OPEN | Range selection/recalculation not accepted | Deterministic selected-range calculation and UI |
| Heatmap | OPEN | Lawful depth source/aggregation/decay not accepted | User's visual reference is required before visual implementation |
| Liquidation Maps | OPEN | Data provenance/estimation/confidence limits not accepted | Validated method/source and UI |

Important indicator invariants:
- Warm-up output stays null.
- Prefix causality; no future-candle lookahead/repaint.
- Exact canonical series identity and timestamp alignment.
- Clear stale values immediately on instrument/timeframe identity changes.
- No indicator output from DEMO, loading, unavailable, error or empty snapshots.
- Deterministic finite values, no source mutation, bounded computation.
- Focused test declarations 21 calculation + 7 shared hook = 28 declarations, not 28 passing tests and not completion percentage.
- Visible indicator UI is Stage 4 work. `docs/INDICATOR_UI_BLUEPRINT.md` is parked and not authorized during Stage 1.
- The separate 40% overall-project gate does not waive Stage 4 or Stage 1 acceptance.

### Owner-supplied visual references
- Footprint PRO 2GD references show dark chart, candlesticks, red/green bid-ask volume cells, numeric volume labels, horizontal volume bars, highlighted price rows and deliberate candle-cluster spacing.
- Footprint OFF must preserve ordinary candle spacing. Explicit Footprint ON alone may use spaced clusters.
- Never label synthetic/offline accumulator values as real exchange bid/ask.
- Heatmap visual work remains blocked until owner supplies its reference image.

### Future chart interaction
- Historical candle replay is an owner-requested future Stage 3 feature: choose starting candle, hide later candles, step/play/pause/seek/back, and exit to a fresh live snapshot. No future candle may leak into chart or indicators while replay is active. It is not transport replay and not trading automation. Not active during Stage 1.

## 7. Zero-cost market-data policy

Authoritative policy: `docs/FREE_MARKET_DATA_SOURCE_POLICY.md`; source inventory: `docs/MARKET_DATA_SOURCE_INVENTORY_ZERO_COST.md`.

A source is production eligible only after evidence-backed review of recurring cost, quotas/rate limits, asset/venue/feed coverage, real-time/delayed/EOD classification, historical lookback, licence/display/redistribution rights, attribution, geography/account eligibility, authentication and over-quota behavior.

Current candidate notes are not approvals:
- Alpaca Basic may offer a narrowly scoped recurring-$0 IEX equities feed subject to current terms and eligibility; IEX is not consolidated all-US market.
- Alpha Vantage free tier is low quota and not a free real-time US stock feed.
- Databento credits are trial credits, not recurring free service; live data is paid.
- Public exchange endpoints require individual terms/protocol/coverage checks.
No source is to be enabled merely because it has a public API or free signup.

## 8. Stage 1 Gate 10 external acceptance blockers

Gate 10 is 0/10 formally closed. Remaining items:
- #8: actual owner-host secret injection, ownership/mode, UID readability, runtime exposure/rotation/log evidence.
- #20: no-billing Firebase sign-in, expiry/revocation, entitlement denial, ticket exchange and browser/Android reconnect E2E.
- #25 (Stage 1 checklist): owner-hardware Redis TLS, ACL, private binding/firewall, persistence and restart/failure recovery.
- #30: actual application DB restore into a fresh owner-host destination.
- #31: encrypted off-host backup, separate key custody and successful recovery restore, all $0.
- #34: real persistent-volume mount/ownership/permissions, restart durability and disk-pressure recovery.
- #35: backend running on existing owner hardware, health/startup/secret injection; public route only if incremental cost is zero.
- #36: authenticated HTTPS/WSS via owner-controlled reverse proxy from real web and Android clients, including reconnect/resnapshot/cross-instance.
- #38: durable owner-host metrics, retention, backup/restore, disk pressure, firewall, token rotation, dashboard, alert acknowledgement/recovery.
- #39: zero-cost local alert route, incident owner/escalation/acknowledgement and recovery drill.
No paid managed Redis, paid domain, paid hosting, paid monitoring, paid backup or paid market data.

Project Gate 25 separately covers signed snapshot transfer, immutable per-gateway receipts and durable high-water ACK. Keep this separate from Stage 1 checklist #25.

## 9. Progress and acceptance accounting

- Stage 1: 30/40 = 75% provisional, not whole-project progress.
- Gate 10: 0/10 formally closed.
- Stage 2: preparatory only.
- Stage 3: not scored.
- Stage 4: gated.
- Stages 5–6: not scored.
- Overall project and IP3S: NOT SCORED under approved reproducible weighting.
- The proposed weighted milestone model is in `docs/PROJECT_MILESTONE_LEDGER.md`; it needs owner review before any new overall percentage is published.
- Code, tests, documentation and CI are distinct evidence. Passing CI does not close external host/device/production acceptance.
- A batch is complete only when its stated acceptance conditions and exact-head evidence are satisfied and the owner gate is reconciled.

## 10. Repository map and source-of-truth documents

Application repository: `deszztagd377-pixel/dezzta-chart`.
Runner repository: `deszztagd377-pixel/dezzta-chart-runner`.

Key application files:
- `PROJECT_STATUS.md` — latest batch and current checkpoint.
- `README.md` — product and environment overview.
- `backend/app/` — FastAPI backend, market-data/provider/identity/OHLCV/alerts/security foundations.
- `src/` — React/TypeScript frontend and chart UI.
- `cloudflare/proof/` — synthetic-only Worker/DO proof; not production deployment.
- `docs/` — roadmap, acceptance matrices, ADRs, data policies, batch work cycles, indicator ledger and detailed design specs.

Priority documents to read before work:
1. `PROJECT_STATUS.md`.
2. `docs/PROJECT_STAGE_ROADMAP.md`.
3. `docs/STAGE_1_ACCEPTANCE_MATRIX.md`.
4. `docs/BATCH90_95_DURABLE_WEBSOCKET_DELIVERY_SPEC.md`.
5. `docs/BATCH89_93_SOURCE_AUDIT_2026-11-25.md`.
6. `docs/INDICATOR_PROGRESS_LEDGER.md`.
7. `docs/FREE_MARKET_DATA_SOURCE_POLICY.md`.
8. Relevant newest `docs/WORK_CYCLE_*.md` and ADRs for the exact task.

## 11. AI agent execution contract

Every run must:
1. Read this Project Brain and the live project checkpoint.
2. Confirm current branch/HEAD and verify no task is being run against application `main`.
3. Read latest work-cycle report, relevant source and tests; inspect open PRs and exact-head CI.
4. Determine the next dependency-ordered actionable task and whether owner approval is already present.
5. If blocked by owner-host/device evidence or an open approval gate, do not invent a code workaround. Prepare a concise blocker/evidence report.
6. Make only a small bounded patch to allowlisted source/test/doc paths. Do not accept arbitrary shell commands or unrestricted diffs from model output.
7. Run approved fixed test commands and validate the exact resulting commit. Parent SHA CI is not evidence for a new SHA.
8. Create a feature branch and PR for owner review. No auto-merge, no direct app-main writes, no production deploy.
9. Update `PROJECT_STATUS.md` and this Project Brain only with verified evidence; preserve historical records.
10. Report: stage/batch, before/after SHA, files changed, tests and exact results, CI URLs, PR URL, blockers, next action.

Stop safely if model quota, API access, credentials, tests, parsing, branch identity or task approval is missing. Never expose or log secret values.

## 12. Automation boundary

The Runner currently has a separate safe Preflight workflow. The Cloudflare relay/cron path has historically dispatched Preflight only; a successful Preflight is not an AI coding run. The AI model is a separate Cloudflare Workers AI model, not ChatGPT/GPT-6, and cannot directly access ChatGPT conversation memory.

The Runner repository's AI bootstrap blueprint and manual model smoke-test workflow are separate from the app. Do not claim recurring AI coding is active until:
- Cloudflare Workers AI credentials are configured as Runner repository secrets;
- manual model smoke test passes;
- bounded read-only task workflow is implemented and tested;
- patch safety, fixed tests, quota stop and PR-only write path are validated;
- only then, after owner confirmation, relay routing is changed to the AI workflow.
Do not alter the 10-minute cron cadence. Run inference only when an approved task is queued; no-op when queue is empty. Never schedule Batch 89.

## 13. Session checkpoint format

Every handoff must include:
- Current official stage and current batch.
- Exact application branch and HEAD.
- Verified implementation vs provisional/not accepted.
- Files added/changed and commit SHA.
- Exact test commands/results and CI run IDs/URLs on the relevant SHA.
- External owner/device/production blockers.
- Cost/secret/deployment status.
- Next action in dependency order and approval required.

## 14. Newly verified historical runtime evidence — 26 November 2026

Two completed executions of the manual Batch 89 Runtime Gate were inspected directly, including job steps and decoded logs:
- Run 45741138139: SUCCESS — https://github.com/deszztagd377-pixel/dezzta-chart-runner/actions/runs/45741138139
- Run 45741338203: SUCCESS — https://github.com/deszztagd377-pixel/dezzta-chart-runner/actions/runs/45741338203
- Both checked out application branch `phase-2/market-data-foundation` at exact SHA `4df26a66c9bc36174d35a1ba12e0237cdb74f595`.
- Both completed locked dependency installation, application tests (34 files / 325 tests passed), production build, Cloudflare Worker runtime test (1 test passed), Durable Object runtime tests (1 file / 11 tests passed), and clean working-tree verification. Both uploaded complete log artifacts (IDs 15080887091 and 15081735867).
- This is real historical Batch 89 runtime evidence for SHA `4df26a6...`, not proof for the later Batch 91 source/test SHA `2d0d7e9...` or current docs-only HEAD `6c610c4...`. Do not mark the current branch's Batch 89 gate as freshly revalidated. A new manual run on the current approved branch/HEAD is still required before relying on it as current-head evidence.
- These runs were manually dispatched / push-triggered in the past; **never add Batch 89 to the recurring 10-minute schedule**.
- This evidence does not accept Batch 91, close Stage 1 Gate 10, or authorize Batch 92.

Next bootstrap blocker remains unchanged: the Runner's Workers AI smoke test and AI project audit have no observed executions in the inspected Actions history. Configure the two least-privilege Cloudflare Workers AI secrets in Runner repository settings, then manually run the smoke test and audit. Do not expose secret values in chat. The relay still targets Preflight only.

## 15. Workers AI connectivity verified through connected Cloudflare account — 26 November 2026

A direct Cloudflare API inference smoke test was executed through the connected account (not through GitHub Actions):
- Model: `@cf/zai-org/glm-4.7-flash`.
- Endpoint returned `success: true`, no API errors, `finish_reason: stop`, and exact response `DEZZTA_CHART_AI_READY`.
- Successful request usage: 216 tokens and 6.9972 Neurons.
- A first deliberately tiny 32-token attempt ended with `finish_reason: length` and no message content because the model's reasoning consumed the output budget; the successful 512-token retry is the valid smoke-test evidence.
- This confirms the connected Cloudflare account can invoke the selected model. It does **not** prove that GitHub Actions has the required repository secrets or that the committed smoke/audit workflows have run. No GitHub Actions AI smoke-test or AI audit run was found in the inspected recent run history.
- Keep the existing zero-cost guardrail: one inference only for an actionable queued task, stop on quota/auth/capacity errors, never enable paid Workers AI.

Bootstrap next step: add `CLOUDFLARE_ACCOUNT_ID` and a least-privilege `CLOUDFLARE_API_TOKEN` as Runner repository Actions secrets (do not paste values into chat), then manually dispatch `ai-agent-smoke-test.yml` and `ai-project-audit.yml`. The connected-account smoke test does not replace those GitHub workflow validations.

## 16. Project status reconciliation — 26 November 2026 (latest direct check)

- Application branch: `phase-2/market-data-foundation`; current branch HEAD is documentation-only `6c610c4de75649126764e0aea200abf09b103521`.
- Current PROJECT_STATUS identifies latest source/test SHA `2d0d7e9a2bf1190961126105d65f77d9926e6789` as Batch 91 implementation in progress / not accepted. Exact-head CI for that source/test SHA is now terminal 4/4 SUCCESS: Automated Tests run 45746150652; CodeQL 45746150693; Full Git History Secret Audit 45746150657; OCI ARM64 45746150726. These runs all target the exact source/test SHA `2d0d7e9...`; they do not target the later docs-only branch HEAD `6c610c4...`. Do not infer Batch 91 acceptance solely from these four CI workflows; contract/owner acceptance gates remain.
- Stage accounting remains Stage 1 official active, 30/40 = 75% provisional; Gate 10 0/10 formally closed. Remaining criteria: 8, 20, 25, 30, 31, 34, 35, 36, 38, 39. Overall project and IP3S are NOT SCORED. Stage 2 preparatory only; Stage 4 gated.
- Batch 90 has historical exact-head acceptance 4/4 on SHA `9a2f2b9faebdcaf1e97e93c6dfe85a2c93319fbb`; Batch 91 is implementation in progress / not accepted; Batch 92 durable event commit/replay; Batch 93 ACK/receipts/high-water/RESUME; Batch 94 lawful zero-cost provider gate; Batch 95 public WSS/browser/Android E2E remain in dependency order.
- Stage 1 remaining acceptance items are external evidence, not simply ten coding tasks: (8) host secret injection/rotation; (20) real no-billing Firebase auth/entitlement/revocation web+Android E2E; (25) self-host Redis TLS/ACL/persistence on existing owner hardware; (30) DB restore drill; (31) encrypted off-host backup and separate key custody/recovery; (34) persistent volume/restart/disk recovery; (35) backend runtime on existing owner hardware; (36) authenticated HTTPS/WSS via owner reverse proxy from real web and Android; (38) durable metrics/ops/restore/alert evidence; (39) zero-cost alert and incident acknowledgement/recovery drill. Stage 1 criterion #25 is not the same as Project Gate 25 (signed snapshot/receipt/high-water ACK).
- AI role clarity: GPT-6 in the active ChatGPT session is the project architect/reviewer and can interpret this Project Brain; Workers AI `@cf/zai-org/glm-4.7-flash` is the external scheduled executor/auditor, not GPT-6 and not connected to ChatGPT private memory. The selected model was directly invoked through the connected Cloudflare account and returned `DEZZTA_CHART_AI_READY` successfully (216 tokens, 6.9972 Neurons). GitHub Actions smoke/audit workflows remain unverified/not observed as executed; their required repository secrets are not readable through the GitHub connector. User must configure `CLOUDFLARE_ACCOUNT_ID` and least-privilege `CLOUDFLARE_API_TOKEN` as Runner Actions secrets if not already present, then manually run smoke and audit workflows. Never ask for secret values in chat.
- Recent Runner history confirms Preflight only is recurring/manual; AI smoke/audit are not running on the 10-minute schedule. Keep relay unchanged until workflow-level smoke, read-only audit, bounded coding/PR workflow and owner approval pass. Never schedule Batch 89.
- Current highest-value next step: resolve Batch 91 acceptance disposition against exact source/test SHA `2d0d7e9...` and current contract blueprint/tests, then proceed to Batch 92 only if Batch 91 acceptance criteria and owner gate are satisfied. Do not start Batch 92/93 by bypassing Batch 91.

## 17. Batch 91 implementation reconciliation — 26 November 2026 (verified)

A fresh source-level audit and GitHub CI log inspection supersedes the older Batch 91 design-only note:
- Compared accepted Batch 90 baseline `9a2f2b9faebdcaf1e97e93c6dfe85a2c93319fbb` to Batch 91 source/test SHA `2d0d7e9a2bf1190961126105d65f77d9926e6789`: 43 commits ahead, 0 behind; 17 changed files (3 added, 14 modified).
- Batch 91 implementation is present: `cloudflare/proof/market-data-contract.mjs`, `src/types/marketDataProtocol.ts`, additive OHLCV metadata parsing, canonical synthetic snapshot/update envelopes and digests, exact-series REST path, status-first WebSocket auth/subscribe, literal text ping/versioned pong, and a DO-local operation queue for snapshot/live boundary serialization.
- Exact-source SHA CI is now terminal 4/4 SUCCESS: Automated Tests run 45746150652; CodeQL 45746150693; Full Git History Secret Audit 45746150657; OCI ARM64 45746150726.
- Automated Tests log: frontend Vitest 35 files / 331 tests passed; Worker Node proof 33/33; pinned local workerd/Miniflare 1/1; Durable Object runtime 15/15; backend pytest 1,435 passed / 1 skipped / 6 warnings; frontend build success; backend container smoke success; auxiliary bundle scanner 5/5, Android read-only preflight 1/1 and release publisher 4/4.
- These results apply to source/test SHA `2d0d7e9...`, not later documentation-only branch HEAD. Latest app branch HEAD after documentation reconciliation is `0dd2d35ec678da31b26fb9a1b091bab2c0801ed9`; app `main` remains untouched.
- Current source includes the Batch 91 synthetic contract, but remains synthetic-only. Cursor subscription currently requests `resnapshot_required` rather than durable replay; no event payload+digest+high-water transaction, durable replay source, ACK, consumer receipt ledger, RESUME or eviction recovery exists yet. Those are Batch 92/93 scope. Batch 94 provider gate and Batch 95 public WSS/device E2E remain open.
- Formal Batch 91 acceptance is still NOT CLOSED pending explicit owner review of final fields, canonical digest encoding, route mapping and synthetic-only compatibility. Do not begin Batch 92 runtime implementation until this gate is closed. Independent Batch 92 failure-injection/test design can proceed.
- A new reconciliation document was committed to app branch: `docs/WORK_CYCLE_2026-11-26_BATCH91_IMPLEMENTATION_RECONCILIATION.md` (commit `7e1cf25ad332b907869fecc7ff67e1635f1a6d66`). `PROJECT_STATUS.md` was corrected to replace stale "design-only/no source changes" and in-progress CI claims (commit `0dd2d35ec678da31b26fb9a1b091bab2c0801ed9`).
- This corrects the prior misstatement that Batch 91 source changes were absent and prior CI IDs still running. Do not carry forward that stale state.
