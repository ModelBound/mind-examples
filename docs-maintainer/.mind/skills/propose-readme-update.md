---
type: skill
description: Triggered when README is stale relative to recent commits; proposes a diff under .mind/diff/ instead of editing directly.
trust: human-reviewed
review:
  state: approved
  reviewed_by: example-reviewer
  reviewed_at: 2026-08-01T00:00:00.000Z
  approved_hash: placeholder
  approved_trust: 88
  scanner_version: h5
---

# Propose a README update

1. Read the current `README.md`.
2. Diff against recent commits (`git log --since='14 days ago'`).
3. Write a proposal to `.mind/diff/<date>-<seq>-readme.md` with `target: README.md`, `confidence: 0.7`, and the proposed replacement body.
4. Do not touch `README.md` directly.
5. Validate the proposal references the motivating commits.

## Scope Constraints (hard limits — split task if exceeded)

- **Max files per task:** 5
- **Max lines of code changed per task:** 250
- **Max features per task:** 1

If any of these would be exceeded, STOP and produce a split plan instead of writing code:

<task-split>
  <reason>Why this exceeds scope</reason>
  <subtasks>
    <task name="..." files="..." exit-criteria="..." />
  </subtasks>
</task-split>
