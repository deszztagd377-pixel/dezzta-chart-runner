# LIVE CHECKPOINT — 28 NOVEMBER 2026 (SUPERSEDES OLDER SNAPSHOTS)

# CURRENT CROSS-REPOSITORY AUTHORITY — 28 NOVEMBER 2026 (supersedes stale checkpoints below)

- Application integration base: `phase-2/market-data-foundation`, HEAD `106082a92b1876125ccdf24065b751c000f1de8a`.
- Active application engineering PR: [#13](https://github.com/deszztagd377-pixel/dezzta-chart/pull/13), branch `work/batch95-websocket-ack-protocol`, HEAD `208165820ae0b02cfb55eff4b388786d55b6277b`. PR is OPEN, unmerged, and non-mergeable; comparison is 194 ahead / 16 behind. Never force-push or merge without safe divergence reconciliation and owner authorization.
- Application `main` is not the work target. Feature work stays on reviewed work branches and PRs against the approved integration base.
- Current production WebSocket ACK: FastAPI route integration exists, feature flag defaults OFF, and durable receipts are guarded by Redis lease/fencing. The latest change adds a narrow Redis ACL key pattern and a real Redis TLS/ACL lease integration test. Production activation remains blocked on owner-host WSS, Firebase identity/revocation/entitlement, durable SQLite topology, browser/Android E2E, and capacity/retention evidence.
- Exact current app-head CI for `2081658`: Automated Tests [46160324003](https://github.com/deszztagd377-pixel/dezzta-chart/actions/runs/46160324003) was IN PROGRESS at the last check; CodeQL [46160323886](https://github.com/deszztagd377-pixel/dezzta-chart/actions/runs/46160323886) SUCCESS; OCI ARM64 [46160323975](https://github.com/deszztagd377-pixel/dezzta-chart/actions/runs/46160323975) SUCCESS; Secret Audit [46160323966](https://github.com/deszztagd377-pixel/dezzta-chart/actions/runs/46160323966) SUCCESS. Re-query the run before accepting; never infer success from a previous SHA.
- Official stage: Stage 1 only, 30/40 provisional (75%); Gate 10 0/10 formally closed. Stage 2 cannot begin until 40/40 and explicit owner approval. No Footprint, Volume Profile or Heatmap feature development during Stage 1; foundations only.
- Target: 24 December 2026; 26 calendar days remained on 28 November. ZERO COST is mandatory.
- **OWNER OVERRIDE:** recurring 10-minute automation is cancelled. Do not create/reactivate cron-job.org, Cloudflare Cron, GitHub schedules or recurring relay dispatch. No autonomous background coding is running. The relay remains untouched/inert; external cron-job.org state is not accessible and must not be described as verified.
- Runner workflows are NOT a background coding service. `preflight.yml` is manual/read-only and checks the application integration base, not PR #13. `ai-coding-runner.yml` is gated by stale Batch 91 owner input and old Project Brain matching; it does not currently write application code. `batch89-runtime-gate.yml` is a heavyweight manual validation of an old task and must not be dispatched for this checkpoint. AI audit/smoke workflows require Cloudflare credentials/model usage and are not assumed zero-cost; do not trigger them.
- Android workflow in the app repo builds a debug APK only on manual dispatch or selected frontend changes; it does not build a final signed release APK for backend-only commits. Previous APK artifacts are not the final integrated app and are not device-accepted.
- No status in older historical sections below overrides these facts. Re-read the live app PR, branch heads, acceptance matrix and exact-head Actions before any future work.

---


- Active app branch: `phase-2/market-data-foundation`; latest app status/documentation checkpoint commit: `a6a7fbc6235f463dd39c980c96639a967815c5b5`. Active-branch source/test baseline remains `41f42a232a25987513c175ea6d271ae5389b1437`; later active-branch commits in this reconciliation are documentation-only.
- App `main` remains `e3841681bc69b73619058deaf939df82ae5116a1` and untouched.
- Exact-head PR validation: PR #4 clickable Footprint UI tests, PR #9 compaction/replay fault injection, and PR #12 required-consumer registry/reactivation fix each have 4/4 required workflows SUCCESS on their stated current source/test heads. PR #7, #8, #10, #11 also retain exact-head 4/4 evidence.
- PR #12 reactivation regression fix commit `b375ada72e7a1af1211c75f70c1cceb9d1f754a7` passed Automated Tests, CodeQL, OCI ARM64 and full-history secret audit. Its branch is 8 ahead / 6 behind the active base; GitHub reports mergeable, but do not merge automatically.
- PR #9 current head `22a05379ea957db93f1909867a74b28cfc5f22c9` passed all four required workflows. It depends on PR #8. CI branch triggers were extended for `test/**` so the full workflow set executes on test branches.
- PR #4 current head `884559e89517d237d256189be17d14deb28a240c` passed all four required workflows including new jsdom component interaction tests. The UI uses explicitly simulated sample data; it is not a live bid/ask feed.
- PR #13 current head `249ae9932784cf713baf7c5b5f11358ca9b456e7`; source/test validation remains on `e29040d4f3e9e5da5c9dd1400e102f5139b9ba41` (4/4). Current PR is 113 ahead / 6 behind and not mergeable. Production FastAPI still lacks ACK receive/receipt commit and capability advertisement. Additionally the SQLite global outbox retention floor advances at 100,000 events without consulting consumer leases/receipts; production ACK must be tied to global cursor and lease-aware retention before enablement.
- Stage 1 remains 30/40 = 75% provisional 🟨; Gate 10 0/10 formally closed; owner-controlled open criteria 8,20,25,30,31,34,35,36,38,39. Stage 2 remains preparatory only.
- Actions audit after PR #4/#9/#12 validation: no in-progress workflow remained in the 100 latest application runs.
- Owner cancellation is final: recurring 10-minute auto-running is CANCELLED. No cron-job.org, Cloudflare Cron, GitHub schedule, replacement trigger, or recurring relay dispatch may be created or reactivated. Manual workflows only when deliberately initiated for approved tasks. Existing relay is not to be deleted or repurposed without separate owner instruction; external cron-job.org state is not independently accessible.

---



## Live checkpoint refresh — 28 November 2026 (owner cancellation + PR evidence)

- Current app branch HEAD: `cb887950ae9a24f087cd2e3252097e7df5a19723` (documentation-only status reconciliation). Latest validated source/test SHA remains `41f42a232a25987513c175ea6d271ae5389b1437`, with exact-head required CI 4/4 SUCCESS; no application runtime source/test changes followed that SHA.
- The app dashboard now explicitly records the owner's cancellation of recurring 10-minute automation. No cron-job.org, Cloudflare Cron, GitHub schedule, replacement trigger, or recurring relay dispatch is authorized. Do not reactivate, route, delete, or repurpose the relay without separate owner instruction. External cron-job.org state is not independently accessible.
- Actions reconciliation: no in-progress runs in the 100 latest app runs or all 14 Runner runs checked. PR #7 and #8 each have 4/4 required workflows successful on their current heads; PR #9 has successful Automated Tests on its current head but no complete 4/4 set observed; PR #13 has 4/4 on validated source/test SHA `e29040d` but is now 4 commits behind/diverged from the app base. All PRs remain unmerged.
- Official Stage 1 remains 30/40 (75% provisional), Gate 10 0/10 formally closed, remaining criteria 8,20,25,30,31,34,35,36,38,39. Stage 2 preparatory only.
> **OWNER OVERRIDE — 28 NOVEMBER 2026: RECURRING 10-MINUTE AUTO-RUN IS CANCELLED.** This is a direct owner decision and supersedes all older text in this file, including historical notes that describe the cadence as active or propose keeping it unchanged. Do not enable, recreate, schedule, or route any recurring trigger (cron-job.org, Cloudflare Cron, GitHub schedule, or replacement). Do not route the relay to Preflight, Batch 89, or AI coding on a recurring basis. Do not treat recurring automation as a pending project deliverable. Manual Actions may only be deliberately initiated for an approved task. Keep the relay configuration untouched/inert; do not delete or repurpose it without separate owner instruction. The external cron-job.org account state is not accessible here, so record the owner cancellation without claiming external account verification.

# DEZZTA CHART — PROJECT BRAIN (Authoritative AI Handoff)

Last reconciled: 28 November 2026, Asia/Jakarta.
Application branch audited: `phase-2/market-data-foundation`.
Application HEAD: `cb887950ae9a24f087cd2e3252097e7df5a19723`.
Purpose: give every automated coding agent the durable project purpose, roadmap, engineering constraints, current state, and owner decisions. This document is context, not permission to bypass approval gates.

> Authority rule: always re-read the live application branch, `PROJECT_STATUS.md`, relevant design/acceptance docs, open PRs and exact-HEAD CI before acting. If this file conflicts with newer repository evidence or a direct owner instruction, stop and reconcile; never silently guess.


## 0. Live checkpoint reconciliation — 28 November 2026 (supersedes stale 26 Nov checkpoint fields below)

**Live repository evidence takes precedence over older dated snapshots in this file.**

- Application branch: `phase-2/market-data-foundation`.
- Application branch HEAD at reconciliation: `cb887950ae9a24f087cd2e3252097e7df5a19723` (documentation-only Batch 99 checkpoint; no application source/test changes in Batch 98/99).
- Latest source/test validation SHA: `41f42a232a25987513c175ea6d271ae5389b1437`. The six commits from the previous Batch 93 source/test SHA `9e7a7ec4534e0985b9ad123d70edfe9fdec76418` to `41f42a2` modify CI workflow configuration, PROJECT_STATUS/report documentation, and the Volume Profile requirements document; no application runtime source/test files changed in that comparison. Four required workflows on `41f42a2` are terminal SUCCESS: Automated Tests #2664 (46108286306), Secret History Audit #1591 (46108286305), OCI ARM64 #638 (46108286297), CodeQL #2009 (46108286284).
- Current app dashboard top section is Batch 92–93 execution state (27 Nov 2026), not the old Batch 91 implementation-in-progress snapshot in Section 4 below. Batch 91 is formally recorded as accepted for its synthetic-only scope in the live app `PROJECT_STATUS.md`; do not carry forward the older 26 Nov NOT ACCEPTED state. Batch 92/93 work is synthetic Worker/SQLite Durable Object proof only. Production WebSocket ACK/RESUME, stable owner-authenticated consumer identity, public WSS/device E2E and provider acceptance remain YELLOW/open.
- Official project stage remains Stage 1, 30/40 criteria (75% provisional); Gate 10 is 0/10 formally closed. Remaining Stage 1 owner-host/device/production evidence criteria: 8, 20, 25, 30, 31, 34, 35, 36, 38, 39. No overall-project score is approved. Stage 2 is not the official active stage.
- Open application PRs at reconciliation: #7 eviction/replay test; #8 legacy cursor authority recovery; #9 compaction rollback (based on #8); #10 provider eligibility audit; #11 Cloudflare/WS inventory; #12 required-consumer registry; #13 synthetic WebSocket ACK protocol. All remain unmerged. PR #8 and PR #9 are dependency-ordered (#8 before #9); PR #7 is a separate Batch 93 regression slice. Do not merge without explicit owner approval. PR #13 remains synthetic-only and does not provide production FastAPI ACK integration.
- Runner AI workflows exist but have no observed executions in the current Runner Actions history: `ai-agent-smoke-test.yml`, `ai-project-audit.yml`, `ai-coding-runner.yml`. Their presence is not evidence of AI automation. The Runner history shows Preflight runs only (latest observed run #45836285961 at 26 Nov 14:10 UTC) and manual Batch 89 runs; never schedule Batch 89.
- Cloudflare relay `dezzta-chart-runner-relay` is deployed and contains secret bindings named `CRON_SECRET` and `GITHUB_TOKEN` (values must never be read or printed). Deployed Worker code dispatches `preflight.yml` only. Cloudflare Cron Trigger schedule list is empty; the relay is driven externally if cron-job.org is enabled. The repository README says keep cron-job.org inactive until a lightweight recurring task is approved. External cron-job.org state is not directly readable through available connectors; do not claim it is active or inactive without fresh evidence.
- The separate AI coding bootstrap remains gated: the Workers AI direct account smoke was previously successful, but GitHub Actions model smoke and read-only project audit have not been observed. Runner repository secrets `CLOUDFLARE_ACCOUNT_ID` and `CLOUDFLARE_API_TOKEN` could not be verified through available GitHub connector permissions. The coding workflow also requires the explicit `confirm_batch91_acceptance=true` dispatch input and an exact Brain HEAD match. This Brain HEAD has been reconciled to the live app HEAD, but do not alter relay routing/cadence or enable recurring coding until the manual smoke, read-only audit, bounded coding workflow validation, secret prerequisites and explicit owner confirmation are all satisfied.
- ZERO COST; application `main` remains untouched; no production deployment, paid resource, billing change, secret value read, or relay target/cadence change was made during this reconciliation.

**Next safe engineering order from the live dashboard:** finish Batch 93 interrupted legacy-cursor initialization/DO eviction-restart persistence regression; then concurrent replay/compaction and rollback/corruption fault injection; then production ACK only after owner-authenticated stable consumer identity is defined. In parallel, owner-controlled Stage 1 Gate 10 evidence must be collected without pretending GitHub CI can supply host/device proof. Delivery target remains 24 December 2026.

---

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
- Current branch HEAD: `8c94b27e5cccb2de64417aad38829dbf86086ebe` (documentation-only checkpoint; source/test baseline is earlier).
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

**Current owner decision (28 Nov 2026): recurring 10-minute automation is CANCELLED.** No cron-job.org, Cloudflare Cron, GitHub schedule, or replacement recurring trigger may be enabled or recreated. The relay must not be routed to any recurring workflow. Older paragraphs in this section and historical sections describing a 10-minute cadence are superseded. Manual workflows are distinct and may only be deliberately initiated for approved work. Do not delete or repurpose the existing relay without separate instruction.


The Runner currently has a separate safe Preflight workflow. The Cloudflare relay/cron path has historically dispatched Preflight only; a successful Preflight is not an AI coding run. The AI model is a separate Cloudflare Workers AI model, not ChatGPT/GPT-6, and cannot directly access ChatGPT conversation memory.

The Runner repository's AI bootstrap blueprint and manual model smoke-test workflow are separate from the app. Do not claim recurring AI coding is active until:
- Cloudflare Workers AI credentials are configured as Runner repository secrets;
- manual model smoke test passes;
- bounded read-only task workflow is implemented and tested;
- patch safety, fixed tests, quota stop and PR-only write path are validated;
- only then, after owner confirmation, relay routing is changed to the AI workflow.
Recurring dispatch is cancelled and must not be used. Manual inference or workflow runs require a separately approved, deliberate task. Never schedule Batch 89.

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

- Application branch: `phase-2/market-data-foundation`; current branch HEAD is documentation-only `8c94b27e5cccb2de64417aad38829dbf86086ebe`.
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

## 18. Batch 92 test-design preparation — 26 November 2026

A dependency-safe Batch 92 test plan was created without touching runtime code:
- App branch file: `docs/WORK_CYCLE_2026-11-26_BATCH92_EVENT_COMMIT_REPLAY_TEST_PLAN.md`.
- Commit: `782fc5ddb2303faf284c208de24ada656ea2ef5a`.
- Defines a transactional event-log contract and 22 deterministic cases covering atomic rollback, post-commit fan-out recovery, idempotency, conflicting payload/digest, sequence gap/regression, generation mismatch, payload bounds, contiguous bounded replay, retention floor, integrity holes, cross-series isolation, eviction and concurrent commits.
- `PROJECT_STATUS.md` links the plan (follow-up docs commit `cd1e4fc33c9b34eff263a476ff6b0172e1cb5a58`).
- This is design/test preparation only. No Batch 92 runtime source or migration was changed. Runtime implementation remains blocked until Batch 91 formal acceptance is explicitly closed.

## 19. Cron relay status correction — 26 November 2026

The Batch 91 reconciliation also found an outdated Cron relay sentence in the app `PROJECT_STATUS.md`. It incorrectly said the relay secrets were absent and the 10-minute schedule inactive. Direct Cloudflare secret-name inventory showed `CRON_SECRET` and `GITHUB_TOKEN` exist (values are not exposed), and recent Runner Actions show successful Preflight dispatches at approximately 10-minute intervals: runs 45824937658, 45826534485, 45828148828, 45829773351 and 45831396293. The relay currently dispatches `preflight.yml` only; this is not AI coding automation. The status file was corrected in app branch commit `8c94b27e5cccb2de64417aad38829dbf86086ebe`. AI smoke/audit execution remains unverified. Never schedule Batch89.


## 20. Automation bootstrap correction — 26 November 2026

The current application branch HEAD is `8c94b27e5cccb2de64417aad38829dbf86086ebe`. The recurring 10-minute Cloudflare relay is confirmed active but dispatches `.github/workflows/preflight.yml` only. Therefore the current interval produces Preflight workflow activity, not autonomous application development, code commits, Pull Requests or APK builds. Do not describe this as an AI coding loop.

A concrete defect was found in Runner `.github/workflows/ai-agent-smoke-test.yml`: it requested only 32 output tokens. The same selected Workers AI model previously returned `finish_reason: length` with no message at that budget; a direct connected-account retry succeeded with a 512-token budget. The smoke workflow was corrected to request 512 tokens in Runner commit `ebe9931d12fddc2a8f8866c87853e2e9ec82688f`. This is a workflow configuration fix only; it does not prove the GitHub Actions smoke test has passed.

Remaining prerequisites before any recurring AI coding activation:
1. Verify Runner repository secrets `CLOUDFLARE_ACCOUNT_ID` and least-privilege `CLOUDFLARE_API_TOKEN` exist without exposing their values.
2. Manually run and verify the corrected AI model smoke workflow and read-only project audit.
3. Implement and test a bounded task-queue coding workflow with strict allowlisted paths, fixed commands, quota/auth stop behavior, exact-HEAD validation, branch + PR only, and no auto-merge.
4. Keep Batch 92 runtime implementation blocked until the owner explicitly accepts Batch 91.
5. Only after all checks and explicit owner confirmation may the relay dispatch target change from Preflight to the bounded AI coding workflow. Keep the 10-minute cadence unchanged and ensure empty queues produce a no-op.

Never claim the system is autonomously developing the APK until recurring runs produce verifiable task records, code diffs, exact-HEAD test evidence and reviewable Pull Requests.