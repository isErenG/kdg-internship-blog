---
title: "Day 18 — Fixing storage and MinIO integration"
date: 2026-05-06
draft: false
tags: ["ray", "minio", "fsspec", "feature-extraction"]
categories: ["internship"]
---

I kept working on the Ray and MinIO integration, fixing a series of smaller issues that surfaced during cluster testing. The fsspec storage options were not being forwarded correctly to PyArrow, the RAY_ADDRESS check was returning a cached result instead of probing the daemon on each call, and the bootstrap step was reading stale AWS environment variables instead of the MINIO_* ones we use. By the end of the day the pipeline could run end to end against either local storage or MinIO by passing a --storage flag. Bayram also shared his finding that the 318-feature extraction had essentially no correlation with the OBD signals, which made it clear that the feature engineering step needed a deeper rethink.
