---
title: "Day 19 — merge_asof alignment and frontend bootstrap"
date: 2026-05-07
draft: false
tags: ["alignment", "sveltekit", "optuna", "validation"]
categories: ["internship"]
---

This was the most productive day of the week. I replaced the 100 ms bin-based OBD alignment with a merge_asof timeline match, which directly addressed the zero-correlation problem Bayram and I had been investigating. I bootstrapped the SvelteKit, TypeScript, and Tailwind 4 frontend so the web UI work could begin. I added per-stage YAML configuration with a Pydantic RunContext so each stage has typed, overridable settings. I introduced plain-function stage entry-points in the CLI so config-driven knob overrides work cleanly. I cleaned up dead code in the BITMAG and API modules, added an Optuna tuning driver with a features-stage result cache so hyperparameter search does not repeat expensive computation, and replaced the standard deviation proxy in the validation step with a proper cantools DBC round-trip mean absolute error score.
