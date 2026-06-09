---
title: "Day 16 — Unified CLI and API architecture"
date: 2026-05-04
draft: false
tags: ["cli", "fastapi", "ray", "architecture"]
categories: ["internship"]
---

I designed and built the unified CLI and API architecture for the project. The central component is a RunContext dataclass that carries paths and settings through every pipeline stage, and a Stage dataclass with a built-in skip-if-exists check so the pipeline is idempotent by default. On top of that I added a PIPELINE registry that maps each stage to a typed adapter, a Ray Jobs API wrapper for submitting heavy stages to the cluster, a FastAPI scaffold with a `/healthz` endpoint and jobs and artifacts routes, and a carve console-script entry point with per-stage CLI commands and a run-all orchestrator. I also added fsspec-aware path helpers so each stage can read from and write to either local storage or MinIO without changing its logic. This was a large day but it gave the project a solid, extensible foundation.
