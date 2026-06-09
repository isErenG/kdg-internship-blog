---
title: "Day 28 — Features stage performance"
date: 2026-05-21
draft: false
tags: ["performance", "feature-extraction", "ray", "alignment"]
categories: ["internship"]
---

Started working on performance improvements for the features stage. Moved the OBD alignment step into the worker task so the driver does not have to handle it. Added two config options to control how many tasks run at the same time on the cluster.
