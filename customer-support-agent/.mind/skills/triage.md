---
type: skill
description: Triggered when a customer message mentions billing, refunds, or cancellation; triages safely without promising outcomes.
trust: human-reviewed
review:
  state: approved
  reviewed_by: example-reviewer
  reviewed_at: 2026-08-01T00:00:00.000Z
  approved_hash: placeholder
  approved_trust: 90
  scanner_version: h5
---

# Triage

For billing / refund / cancel intents:

1. Ask for the customer's account email if not present.
2. Do not promise a refund — say "I'll pass this to our billing team".
3. Emit a `HANDOFF:` line with a one-sentence summary for the human agent.
4. Review the draft reply against tone guidelines before sending.

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
