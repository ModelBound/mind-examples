---
type: skill
description: Triggered when the user asks to add or update tests; colocates test files and follows table-driven patterns.
review:
  state: draft
---

# Write tests

- Colocate `*.test.ts` next to the file under test.
- One `describe` per exported symbol.
- Use `it.each` for table-driven cases.
- Never mock what you don't own — wrap it and mock the wrapper.
- Run the test suite and verify all new tests pass before finishing.

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
