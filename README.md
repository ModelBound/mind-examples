# mind-examples

Starter `.mind/` folders you can fork and adapt.

| Folder | What it demonstrates |
|--------|----------------------|
| `typescript-coding-assistant/` | A coding assistant with team preferences and per-user memory. |
| `customer-support-agent/` | Routes questions to product docs, tone guides, and customer history. |
| `onboarding-buddy/` | Helps new team members find rituals, docs, and people. |
| `docs-maintainer/` | Proposes README and runbook updates as the codebase changes. |

## Use one

```bash
cp -r typescript-coding-assistant/.mind ./
```

Or reference it from the [`mind` registry](https://mind.modelbound.co/registry).

## Contribute

Open a PR with a new folder. Every example must:

1. Have a top-level `README.md` explaining the persona and intended use.
2. Contain a valid `.mind/` folder (run `npx @modelbound/mind-cli validate`).
3. Include no secrets.

Apache 2.0.
