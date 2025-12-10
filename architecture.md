# Architecture overview (short)

- API: FastAPI (Python) or Express (Node) for orchestration + auth
- Web: Next.js React app for dashboard & marketplace
- Workers: Dockerized model runners; job queue via Redis/Celery or Bull
- Storage: Postgres for transactional data, S3-compatible for artifacts
- Orchestration: k8s manifests under `infra/` later
- Auth: Clerk or Auth0; Billing: Stripe