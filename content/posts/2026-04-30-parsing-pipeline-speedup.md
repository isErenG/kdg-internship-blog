---
title: "Day 14 — A 100x faster parsing pipeline"
date: 2026-04-30
draft: false
tags: ["ray", "parsing", "performance", "notebooks"]
categories: ["internship"]
---

I worked on the parsing pipeline today. The Ray-based parsing was working correctly but was too slow for practical use on the cluster. I rewrote the core of the implementation and achieved roughly a 100x speed improvement. I also fixed the output bucket path so that parsed files land in `carve/interim/parsed/<vehicle_name>` consistently across all vehicles. In the afternoon I reorganised the project folder structure and added Jupyter notebooks so we could run individual pipeline stages interactively for debugging and exploration.
