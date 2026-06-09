---
title: "Day 24 — Migrating to the ray.data streaming API"
date: 2026-05-14
draft: false
tags: ["ray-data", "streaming", "ingestion"]
categories: ["internship"]
---

Started moving the pipeline to the ray.data streaming API. Replaced the ingestion step with a whole-file reader and moved the boundaries stage to a streaming groupby. Added PyArrow adapters so ray.data can write to local storage or MinIO.
