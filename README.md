# HustleGPT-repo
Dev automation SaaS

# HustleGPT

HustleGPT is the repo for the HustleGPT platform — an AI PaaS for running models, exposing a marketplace, and offering a web UI & API for customers.

## Quick start

1. Copy `.env.example` → `.env` and fill secrets.
2. `docker compose up --build`
3. Visit `http://localhost:3000` for the frontend (if running locally).

## What’s in this repo

- `api/` — FastAPI (or Express) microservices for orchestration & auth
- `worker/` — background worker (Celery or Bull) for model jobs
- `models/` — model runner wrappers (Docker-in-Docker / containerized)
- `web/` — Next.js frontend
- `infra/` — terraform / k8s manifests (optional)
- `.github/workflows/ci.yml` — CI pipeline

## Goals & priorities

1. Secure, isolated model execution (Docker-based sandboxes)
2. Simple dev UX (docker-compose local dev)
3. Clear billing/auth integration (Stripe + Clerk)
4. Extensible marketplace & multi-tenant data partitioning

## Contributing

See `CONTRIBUTING.md`.
