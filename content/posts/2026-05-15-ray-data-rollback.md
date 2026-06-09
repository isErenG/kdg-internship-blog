---
title: "Day 25 — Rolling back the ray.data migration"
date: 2026-05-15
draft: false
tags: ["ray-data", "ray", "minio"]
categories: ["internship"]
---

Continued the ray.data migration but then ran into state-API problems on the HPC cluster. I switched back to plain @ray.remote workers per file and dropped the groupby shuffle. The pipeline now reads and writes directly from MinIO.
