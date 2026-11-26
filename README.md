# DEZZTA CHART Runner

Zero-cost automation scaffold for DEZZTA CHART.

## Status

Bootstrap only. No scheduled jobs, deployment, repository secrets, or external endpoint are configured yet.

## Safety boundaries

- The application repository is `deszztagd377-pixel/dezzta-chart`.
- Work is restricted to `phase-2/market-data-foundation`.
- Never write to `main` in the application repository.
- Do not run the full application CI every 10 minutes.
- No paid services, model APIs, or market-data subscriptions are assumed.
- Secrets must be stored in GitHub Actions or Cloudflare secret storage, never committed here.

## Next steps

1. Add a minimal manually-dispatched preflight workflow.
2. Validate the workflow and repository permissions.
3. Configure a secure trigger relay only after its deployment and secret handling are ready.
4. Keep cron-job.org inactive until a real HTTPS endpoint has been deployed and tested.

This scaffold does not provide autonomous AI coding. It can only execute explicitly defined automation tasks.
