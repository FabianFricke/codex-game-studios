# Upgrading Codex Game Studios

This repository no longer uses the old Claude-specific control plane. The
source of truth is now:

- `AGENTS.md`
- `ARCHITECTURE.md`
- `docs/`
- `studio/`

## If You Are Migrating An Older Copy

1. Replace any `.claude/`-based role, workflow, template, or rule reference
   with the matching path under `studio/`.
2. Replace any `PLAYBOOK.md` workflow references with `PLAYBOOK.md`.
3. Move project engine choices into `AGENTS.md` and
   `studio/docs/technical-preferences.md`.
4. Re-read `docs/CODEX-WORKFLOWS.md` and `docs/WORKFLOW-GUIDE.md` before doing
   new work.

## File Mapping

- `.claude/agents/` -> `studio/roles/`
- `.claude/skills/` -> `studio/workflows/`
- `.claude/docs/templates/` -> `studio/templates/`
- `.claude/rules/` -> `studio/standards/`
- `.claude/docs/agent-roster.md` -> `studio/docs/agent-roster.md`
- `.claude/docs/technical-preferences.md` -> `studio/docs/technical-preferences.md`
- `AGENTS.md` -> `AGENTS.md`

## Validation

After upgrading, search the repo for:

- `.claude/`
- `AGENTS.md`
- `PLAYBOOK.md`

Any remaining matches should be intentional historical references only.
