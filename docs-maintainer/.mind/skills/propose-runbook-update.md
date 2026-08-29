---
type: skill
description: Triggered when a runbook needs updating after an incident or PR; proposes a scoped diff instead of editing docs/runbook.md directly.
trust: human-reviewed
review:
  state: approved
  reviewed_by: example-reviewer
  reviewed_at: 2026-08-01T00:00:00.000Z
  approved_hash: placeholder
  approved_trust: 88
  scanner_version: h5
---

# Propose a runbook update

Same flow as `propose-readme-update.md`, but target is `docs/runbook.md`. Cite the incident, PR, or commit that motivated the change in the proposal's `reason:` frontmatter.

Review the proposal against `context/style.md` before submitting.

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
