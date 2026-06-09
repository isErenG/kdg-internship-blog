---
title: "Day 23 — Alignment and storage interfaces"
date: 2026-05-13
draft: false
tags: ["alignment", "storage", "mlflow", "minio"]
categories: ["internship"]
---

Merged PR #75. Added an AlignmentMethod enum and a base class for alignment strategies so we can switch between them easily. Added a BucketStorage interface with local and MinIO implementations including PyArrow adapters. Set up MLflow tracking in the features pipeline and added JSON logging. The feature columns now use real signal names instead of integer indices.
