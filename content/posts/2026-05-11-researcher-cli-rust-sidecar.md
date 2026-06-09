---
title: "Day 21 — Researcher CLI and Rust sidecar"
date: 2026-05-11
draft: false
tags: ["cli", "rust", "tauri", "performance"]
categories: ["internship"]
---

Pushed a large batch of work that had been accumulating on a feature branch. On the Python side I split the package dependencies into optional extras so the core stays lean. I built a complete researcher CLI sub-app with a dedicated script entry point, JSON error envelopes on every command, byte-order suggestion via shape-smoothness ranking, a rule-based shape-feature classifier, classified candidate listing per CAN ID, and per-window bit-change activity analysis. On the performance side I replaced the Theil-Sen fit with plain OLS to remove the O(n²) tail in large windows, chunked candidate lists with LPT-order dispatch, and assembled the output DataFrame column-wise to reduce memory copies. I also built a Rust sidecar binary that the researcher tool invokes, and scaffolded a lightweight Tauri wrapper around it as a standalone analysis prototype separate from the main web interface.
