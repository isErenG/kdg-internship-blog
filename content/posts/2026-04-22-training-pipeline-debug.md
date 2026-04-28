---
title: "Day 8 — Debugging the training pipeline"
date: 2026-04-22
draft: false
tags: ["ray-train", "training", "feature-extraction"]
categories: ["internship"]
---

Today I worked on the training pipeline that Bayram was running on the HPC cluster. He sent me the errors and the unstable training results, and I tried to reproduce the same problems on my laptop. Most of the issues were around the Ray Train checkpoint handling and a few small problems in the feature extraction step. The neural network itself worked well once the data side was fixed.
