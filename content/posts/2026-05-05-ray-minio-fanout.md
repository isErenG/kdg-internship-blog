---
title: "Day 17 — Ray and MinIO integration"
date: 2026-05-05
draft: false
tags: ["ray", "minio", "feature-extraction", "dependencies"]
categories: ["internship"]
---

We had a meeting with the supervisors today and discussed the current state of the algorithm as well as other related research in the same area. In the afternoon I continued the Ray and MinIO integration work. I added a two-wave fan-out to the features stage so that workers dispatch per-CAN-ID scans in parallel rather than sequentially, and I added a unified drain over both waves to collect results efficiently. I also fixed several worker dependency issues. scipy, scikit-learn, joblib, and cantools were missing from the worker pip list so I added them to the runtime_env. I also added a carve sync command that mirrors parsed parquets from MinIO to local storage for offline development.
