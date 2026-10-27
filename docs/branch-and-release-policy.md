---
title: ScoreBook branch and release policy
status: current-governance
date: 2026-10-27
---

# ScoreBook branch and release policy

`main` is the protected product-template branch. Use short-lived `feat/*`, `fix/*`, `docs/*`, and `chore/*` branches. A pull request is required for every change to `main`; direct pushes, force pushes and deletion of `main` are forbidden.

At least one of `egoleecode`, `yry0008`, `icelee-asr`, or `even-ship-it` must approve a pull request without having authored it. A new push dismisses stale approvals, the most recent reviewable push needs approval from someone other than its pusher, and all conversations must be resolved. Squash merge is the enabled merge method, linear history is required, merged working branches are deleted automatically, and auto-merge is disabled. There is currently no CI-backed up-to-date-branch requirement; that rule joins the verified check requirements when CI is ready.

The three additional maintainers have Write permission, while `egoleecode` retains administrator permission. Main protection applies to administrators. CODEOWNERS enforcement uses the base branch's file and becomes effective after this initial governance PR is reviewed and merged. Ordinary independent approval is already required. Coding agents may prepare changes and PRs but do not approve, merge or publish without an explicit human decision.

ScoreBook currently has no repository-wide automated CI gate. Reviewers must inspect source attribution, licenses, information classification, template consistency, links and the separation between product templates and enterprise instances. A future check may become required only after it has run successfully on a real pull request and its reported status name is recorded in the branch rule.

The first stable release is an explicit maintainer decision represented by a non-prerelease GitHub Release and an immutable semantic-version tag, normally `v1.0.0`; alpha, beta and release-candidate versions do not count. Each product reaches stable independently. The current template content and MIT publication do not constitute a stable release. Before that release, verify branch rules, effective CODEOWNERS, an actual template validation CI and human release approval; publishing a Release does not configure these automatically. Product releases do not publish enterprise instances or their private data. A release PR must identify the protected-branch commit, content review, license review and any migration or upgrade implications.

Active tag rules prohibit updates and deletions of `v*` and `orchestra-upstream/*` tags, including by administrators; tag creation is not release approval. If an older release needs independent maintenance, protect `release/x.y` with equivalent rules before accepting fixes and return fixes to `main` through PRs. Any emergency protection change requires an explicit human administrator decision, a recorded reason, restoration and independent follow-up review.

Changes to `reference-company/` are reviewed as reusable template content. They do not automatically become an enterprise policy or change a Stage deployment. Enterprise repositories may use their own private branch and approval rules after copying the template.
