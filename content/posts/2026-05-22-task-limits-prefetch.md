---
title: "Day 29 — Task limits and file prefetching"
date: 2026-05-22
draft: false
tags: ["performance", "memory", "ray"]
categories: ["internship"]
---

Continued the performance work. Added a limit on how many tasks can run at the same time so the cluster does not run out of memory. Also added a background thread that starts loading the next file while the current one is still being processed. Cleaned up some old tests.
