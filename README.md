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

## Safety and cost boundaries

- No paid services, model APIs, or market-data subscriptions are assumed.
- No autonomous AI coding is provided by GitHub Actions; workflows execute only the tasks explicitly defined here.
- Secrets must be stored in GitHub Actions or Cloudflare secret storage, never committed here or pasted into chat.
- Do not run the full application CI every 10 minutes.
- Preserve existing application features and require evidence before marking any batch accepted.
