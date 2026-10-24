# Archived skills

This fork serves a single product. The skills in this folder do not fit its work or were never used, so they are moved out of `.claude/skills/` and no longer load in any session. Each skill's description costs tokens in every session while it is loaded.

| Skill | Why archived |
|---|---|
| release, release-sync | Framework release tooling for apexyard maintainers |
| split-portfolio, onboard, tutorial, orbit | One-time setup and onboarding, already done |
| eval-agents, mutation-test | Framework agent evaluation and a milestone-only sensor |
| extract-features, feature-diagram, process, walking-skeleton, tech-vision | Rewrite and greenfield planning tools this fork does not use |
| journey, prototype, prototype-close, design-sync | Replaced by design canvases outside the repo |

Two unused skills stay loaded because framework checks read their files:

- `geo-audit`: the sub-pack extraction check (`bin/extract-subpacks.sh`).
- `handover`: `.claude/hooks/tests/test_handover_clone_prompt.sh`, the sub-pack test and `bin/install-git-hooks.sh`.

Some hooks and scripts mention archived skills in comments only. They still work.

## Restore one

```bash
git mv .claude/skills-archive/<name> .claude/skills/<name>
```

Start a new session after the move.
