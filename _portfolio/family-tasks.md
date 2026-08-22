---
title: "family_tasks: Shared to-do app on Cloud Run"
excerpt: "Mobile-first, server-rendered FastAPI + HTMX task list with Web Push reminders, deployed scale-to-zero on Google Cloud Run.<br/>"
collection: portfolio
---

**Stack:** Python · FastAPI · HTMX · SQLModel · Google Cloud Run · Google OAuth · Web Push (VAPID)

**Repo:** [github.com/PranavC225/family_tasks](https://github.com/PranavC225/family_tasks)

## Problem

A dead-simple, phone-first shared task list with reliable reminders, without the overhead of a single-page app or the cost of a paid push service.

## Approach

- Server-rendered task management (create/assign/complete), optimized for mobile.
- Google OAuth login restricted to an email allowlist.
- Web Push notifications via VAPID; no Firebase/FCM.
- Database-agnostic: SQLModel over `DATABASE_URL` (SQLite locally, Neon Postgres in production).
- Auto-deploys on push to `main` via a Cloud Build trigger; secrets in GCP Secret Manager.

## Architecture

```mermaid
flowchart LR
  U[Mobile browser · HTMX] --> F[FastAPI · server-rendered]
  F --> M[SQLModel]
  M --> DB[(SQLite local / Neon Postgres prod)]
  F --> OA[Google OAuth · email allowlist]
  F --> WP[Web Push · VAPID]
  GH[push to main] --> CB[Cloud Build trigger] --> CR[Cloud Run · europe-west4 · min-instances=0]
```

## Why this stack

- **FastAPI + HTMX:** server-rendered, no SPA build step or client-state overhead.
- **SQLModel:** a single model layer that swaps databases via one env var.
- **Google Cloud Run** (europe-west4): scale-to-zero.
- **Web Push / VAPID:** push notifications without a Firebase dependency.
- **Google OAuth:** auth gated to an email allowlist (`auth.py:auth_callback`).
- **GCP Secret Manager + Cloud Build:** secret storage and push-to-deploy CI/CD.

## Results

The live app is OAuth-gated to an email allowlist, so there's no public login to demo. The main task view, running on Cloud Run:

![Family Tasks web app showing the add-task bar with an assignee selector, and two active tasks with complete, repeat and archive actions]({{ base_path }}/images/family-tasks-ss.png)

Each task carries who added it, when, and who it's assigned to. The three actions per row are complete, make recurring, and archive; Active/Done/Archive filter the list, and Notify registers the browser for Web Push.

*A short demo video of the full task flow will replace this once the next round of UI work lands.*

## What I learned

- **Web Push:** implementing VAPID directly instead of reaching for a Firebase/FCM dependency.
- **DB-agnostic from day one:** putting SQLModel behind `DATABASE_URL` meant SQLite locally and Postgres in prod with zero code change.
- **Scale-to-zero economics:** `min-instances=0` + Cloud Build trigger gives push-to-deploy at no idle cost.
