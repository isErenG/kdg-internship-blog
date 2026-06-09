---
title: "Day 12 — Byte-order selection and new features"
date: 2026-04-28
draft: false
tags: ["bitmag", "feature-extraction", "classifier", "fft"]
categories: ["internship"]
---

We had a progress meeting with Wouter today where we showed what we had built so far and talked through the planned frontend. After the meeting I focused on improving the quality of the classifier pipeline. I added variance-weighted byte-order selection to the BITMAG module so the pipeline picks the more informative signal representation between Intel and Motorola order. I also added FFT magnitude standard deviation as a new feature in the feature extraction step, added a held-out test set with a per-class accuracy report to the training pipeline, and fixed a bug where structural metadata fields were incorrectly leaking into the neural network input.
