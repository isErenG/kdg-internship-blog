---
title: "Day 27 — Merging ray-data and simplifying config"
date: 2026-05-19
draft: false
tags: ["ray-data", "config", "api", "tang"]
categories: ["internship"]
---

Merged the ray-data migration branch (PR #78). Added the Tang alignment strategy to the factory so it can be selected from config. Simplified the config layer so all settings are in one flat model and CLI overrides work cleanly. Also restructured the API into separate handler packages.
