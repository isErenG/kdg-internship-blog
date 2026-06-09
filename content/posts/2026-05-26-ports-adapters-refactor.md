---
title: "Day 31 — Ports-and-adapters refactor"
date: 2026-05-26
draft: false
tags: ["architecture", "api", "sqlite", "artifacts"]
categories: ["internship"]
---

Big refactoring day. In the morning we met with Wouter and I showed the architecture changes. After the meeting I merged the performance branch and restructured the project folders. I separated the code into inbound and outbound adapters with the business logic in the middle. I also added a SQLite repository to save run state, added signed URLs and a DBC download endpoint to the API, and wrote six JSON artifact writers so Bayram could display the pipeline results in the web interface.
