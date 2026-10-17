# SmartBazaar deployment health

Health check for the deployed SmartBazaar demo at
https://smartbazaar-demo.onrender.com/health.

This repository contains only the deployment health workflow and this README.
Application source, catalog data, credentials and customer data remain private.

GitHub Actions checks the endpoint every ten minutes and supports manual runs.
Requests time out after 90 seconds. Network errors, non-200 responses and invalid
application health JSON fail the job. No third-party actions, checkout, secrets,
artifacts or caches are used. The standard Ubuntu runner is free in this public
repository.

Scheduled runs can be delayed or dropped. Public workflows can disable after
60 days without repository activity. This monitor does not guarantee 24/7 uptime;
Render Free may sleep after a missed check or restart independently. Check the
Actions history and configure a separate free external monitor for redundancy.

Sources: [GitHub Actions billing](https://docs.github.com/en/billing/concepts/product-billing/github-actions),
[scheduled events](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#schedule),
[Render Free limits](https://render.com/docs/free).
