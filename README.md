# DEZZTA CHART Runner

Zero-cost automation scaffold for DEZZTA CHART.

## Repositories and branch boundary

- Runner repository: `deszztagd377-pixel/dezzta-chart-runner` (default branch `main`).
- Application repository: `deszztagd377-pixel/dezzta-chart`.
- Application work is restricted to `phase-2/market-data-foundation`.
- Never write to `main` in the application repository.

## Workflows

- `.github/workflows/preflight.yml`: manually dispatched repository/branch preflight only. It does not install dependencies or run tests.
- `.github/workflows/batch89-runtime-gate.yml`: manually dispatched Batch 89 runtime validation. It runs `npm ci`, the application test suite, production build, Cloudflare Worker runtime tests, Durable Objects runtime tests, then checks the source working tree and uploads logs.

The Batch 89 workflow is intentionally manual. It can take a substantial amount of time and must not be triggered every 10 minutes.

## Automation relay status

A Cloudflare Worker relay has been deployed separately. Keep cron-job.org inactive until a specific lightweight recurring task is approved and the relay's secrets and dispatch target are configured. Do not point a 10-minute schedule at the Batch 89 validation workflow.

## Relay request contract

The deployed Worker relay is `https://dezzta-chart-runner-relay.deszztagd377.workers.dev`.

- Liveness check: `GET /health`. This confirms the Worker responds; it does not prove dispatch credentials are configured.
- Dispatch: `POST /trigger`, with an `Authorization: Bearer <CRON_SECRET>` header and no request body.
- The Worker requires two Cloudflare secrets: `CRON_SECRET` and `GITHUB_TOKEN`.
- `CRON_SECRET` must be a high-entropy value of at least 32 characters. Store the same value in the cron service's Authorization header; never commit or paste it into repository files.
- `GITHUB_TOKEN` must be a repository-scoped GitHub token with Actions: write permission for this runner repository, so the relay can dispatch `preflight.yml`.
- A successful dispatch responds with HTTP 202. Missing secrets respond with HTTP 503; invalid bearer authentication responds with HTTP 401.
- The preflight workflow runs on the runner repository's `main` branch only, then checks out the application repository's approved `phase-2/market-data-foundation` branch. It does not write to the application repository.
- The 10-minute cron-job.org schedule remains inactive until both Worker secrets are configured and a manual dispatch test returns HTTP 202. Do not schedule `batch89-runtime-gate.yml`; it is a heavyweight manual validation workflow.

## Safety and cost boundaries

- No paid services, model APIs, or market-data subscriptions are assumed.
- No autonomous AI coding is provided by GitHub Actions; workflows execute only the tasks explicitly defined here.
- Secrets must be stored in GitHub Actions or Cloudflare secret storage, never committed here or pasted into chat.
- Do not run the full application CI every 10 minutes.
- Preserve existing application features and require evidence before marking any batch accepted.
