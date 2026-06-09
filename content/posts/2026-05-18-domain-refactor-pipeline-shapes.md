---
title: "Day 26 — Domain refactor and pipeline experiments"
date: 2026-05-18
draft: false
tags: ["refactor", "domain", "ray", "feature-extraction"]
categories: ["internship"]
---

We had the third internship visit with Elke, Wouter, Bayram, and myself. After the meeting I focused on backend work: extracted CandidateRow into carve.domain.candidate, moved the BITMAG CSV loader into carve.domain.bitmag, and separated the output schema from the feature computation code. I also ran a series of experiments with different @ray.remote pipeline shapes for the features stage, testing file-level maps, per-CAN-ID fans, and alignment placement options, and settled on a two-stage orchestrator by the end of the day.
