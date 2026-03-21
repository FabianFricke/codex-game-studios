# Architecture

This repository is a workflow template for AI-assisted game development. It is
not a game project itself; it is the scaffolding around one. The primary goal is
to give human users and coding agents a shared operating model for planning,
designing, implementing, reviewing, and shipping games with a consistent repo
structure.

## Top-Level Map

- `AGENTS.md`
  - Root entrypoint for Codex and other agents.
- `README.md`
  - Public-facing overview, setup, and positioning.
- `studio/`
  - Codex-native operating library for specialist roles, workflows, templates,
    standards, and studio reference docs.
- `docs/`
  - Tool-agnostic operating docs, workflow guides, examples, and engine references.
- `production/`
  - Project-management artifacts such as sprint plans, milestones, and releases.

## Functional Areas

### Root Guidance
- `AGENTS.md` is the first stop for Codex agents.
- `ARCHITECTURE.md` explains where to look next.
- `README.md` explains the template to humans browsing the repo.

### Studio System Of Record
- `studio/roles/` defines specialist role prompts and responsibilities.
- `studio/workflows/` defines reusable execution workflows for recurring tasks.
- `studio/templates/` holds design, production, and release templates.
- `studio/standards/` holds domain-specific quality rules and review lenses.
- `studio/docs/` holds supporting studio references such as rosters and coordination maps.

### Shared Documentation
- `docs/WORKFLOW-GUIDE.md` describes end-to-end project flow.
- `docs/CODEX-WORKFLOWS.md` translates that flow into Codex-friendly patterns.
- `docs/COLLABORATIVE-DESIGN-PRINCIPLE.md` defines the human-in-the-loop model.
- `docs/examples/` shows concrete session and workflow examples.
- `docs/engine-reference/` stores engine and version references.

## Dependency Direction

The intended documentation dependency direction is:

`README.md` / `AGENTS.md` -> `ARCHITECTURE.md` -> `docs/*.md` -> `studio/**`

That means:
- Root files should point to deeper docs, not restate everything.
- Shared docs should be tool-agnostic when possible.
- Studio execution assets should derive from shared repo guidance, not define it alone.

## Authoring Rule

When adding new workflow guidance:
- Put the source of truth in `docs/` or a root markdown file.
- Put executable role/workflow/template material in `studio/`.
- Prefer portable markdown instructions over tool-specific control files.
