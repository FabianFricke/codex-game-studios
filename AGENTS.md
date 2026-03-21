# AGENTS.md

## Start Here
- Repository map: `ARCHITECTURE.md`
- Human and agent workflow guide: `docs/WORKFLOW-GUIDE.md`
- Codex-specific operating guidance: `docs/CODEX-WORKFLOWS.md`
- Collaboration protocol and approval model: `docs/COLLABORATIVE-DESIGN-PRINCIPLE.md`
- Studio role index: `studio/roles/README.md`
- Studio workflow index: `studio/workflows/README.md`
- Studio templates index: `studio/templates/README.md`
- Studio standards index: `studio/standards/README.md`
- Engine references: `docs/engine-reference/README.md`
- Example sessions and patterns: `docs/examples/README.md`

## What This Repo Is
- A role-first template for running an indie game project with structured specialist roles, reusable workflows, and documentation templates.
- The repo now treats Codex agents as the primary workflow target.
- The `studio/` directory is the operating system for the game studio model: roles, workflows, templates, and standards.

## Project Configuration
- Engine: `[CHOOSE: Godot 4 / Unity / Unreal Engine 5]`
- Language: `[CHOOSE: GDScript / C# / C++ / Blueprint]`
- Build System: `[SPECIFY]`
- Asset Pipeline: `[SPECIFY]`
- Target Platforms: `[SPECIFY]`

Update this section when the project chooses its engine and toolchain. Keep
engine-specific conventions and budgets in `studio/docs/technical-preferences.md`.

## Core Workflow
1. Read `ARCHITECTURE.md` to understand the repo layout and what each directory is for.
2. Read `docs/CODEX-WORKFLOWS.md` before changing docs, prompts, or agent guidance.
3. Keep work visible in the repo: write plans, assumptions, and decisions into versioned files.
4. Preserve the collaboration model in `docs/COLLABORATIVE-DESIGN-PRINCIPLE.md`: ask questions, surface tradeoffs, and avoid silent creative decisions.
5. Use `studio/roles/` to choose the right reasoning frame and `studio/workflows/` to execute common game-dev tasks.

## Working Conventions
- Prefer root docs over tool-specific prompt files as the source of truth.
- Keep new top-level guidance tool-agnostic unless a workflow is inherently platform-specific.
- When adding new agent behavior, write or update the role in `studio/roles/` and any supporting workflow in `studio/workflows/`.
- Do not rely on hidden session state for critical repo behavior.
- Keep reusable docs small and index deeper material instead of duplicating it.

## Common Tasks
- Update repo guidance: edit `AGENTS.md`, `ARCHITECTURE.md`, and the relevant file in `docs/`.
- Add or revise a workflow: update `docs/CODEX-WORKFLOWS.md` and any examples under `docs/examples/`.
- Maintain the studio model: update the relevant file under `studio/roles/`, `studio/workflows/`, `studio/templates/`, or `studio/standards/`.
- Review agent responsibilities: inspect `studio/roles/` and `studio/docs/agent-roster.md`.

## Safety Rules
- Avoid destructive git commands unless the user requests them.
- Keep repo-facing instructions in normal Markdown where all agents can read them.

## Validation
- Check for stale references to obsolete `.claude/` paths in root docs.
- When changing workflow docs, verify links and referenced files exist.
