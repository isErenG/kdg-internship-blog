---
title: "Day 9 — Improving the classifier with a voting layer"
date: 2026-04-23
draft: false
tags: ["classifier", "voting", "feature-extraction"]
categories: ["internship"]
---

I kept working on the training pipeline based on the results from the cluster runs that Bayram was doing. We looked together at where the model was confident and where it was not, and it became clear that the simple feature extraction step was not strong enough on its own. I noted that we needed a better voting layer on top of the classifier, while Bayram kept running the pipeline on the cluster so we had a steady flow of feedback.
