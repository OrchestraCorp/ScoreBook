---
title: ScoreBook branch and release policy
status: current-governance
date: 2026-10-27
---

# ScoreBook branch and release policy

`main` is the protected product-template branch. Use short-lived `feat/*`, `fix/*`, `docs/*`, and `chore/*` branches. A pull request is required for every change to `main`; direct pushes, force pushes and deletion of `main` are forbidden.

At least one of `yry0008`, `icelee-asr`, or `even-ship-it` must approve a pull request without having authored it. A new push dismisses stale approvals, the latest commit must be reviewed, all conversations must be resolved, and the branch must be current before merge. Squash merge is the default.

ScoreBook currently has no repository-wide automated CI gate. Reviewers must inspect source attribution, licenses, information classification, template consistency, links and the separation between product templates and enterprise instances. A future check may become required only after it has run successfully on a real pull request and its reported status name is recorded in the branch rule.

The first stable release is an explicit maintainer decision represented by a GitHub Release and an immutable `v1.0.0`-style tag. The current template content and MIT publication do not constitute a stable release. Product releases do not publish enterprise instances or their private data. A release PR must identify the template commit, content review, license review and any migration or upgrade implications.

Changes to `reference-company/` are reviewed as reusable template content. They do not automatically become an enterprise policy or change a Stage deployment. Enterprise repositories may use their own private branch and approval rules after copying the template.
