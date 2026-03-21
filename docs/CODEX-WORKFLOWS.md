# Codex Workflows

This repository now supports Codex as a first-class workflow target.
Use this file as the bridge between the repo's studio model and Codex's more
general agent execution model.

## How To Use This Repo In Codex

### 1. Start From Repo Docs, Not Tool Prompts

Read files in this order:

1. `AGENTS.md`
2. `ARCHITECTURE.md`
3. `docs/WORKFLOW-GUIDE.md`
4. `docs/COLLABORATIVE-DESIGN-PRINCIPLE.md`
5. The relevant file under `studio/roles/`, `studio/workflows/`, `studio/templates/`, or `studio/standards/`

This keeps the workflow portable across agents and prevents tool-specific drift.

### 2. Treat Specialist Roles As Execution Personas

The specialist definitions under `studio/roles/` are the primary role library. In Codex:

- Use the role roster to understand responsibilities and review lenses.
- Apply the role as a reasoning frame inside the current task.
- Only translate a role into delegated parallel work when the task actually
  benefits from parallelism or separation of concerns.

### 3. Use Workflows, Not Slash Commands

Codex works better with repo-native workflows than command aliases. Use the
corresponding docs and templates instead:

| Studio workflow | Codex pattern |
|----------------|------------------|
| `studio/workflows/start/` | Read `docs/WORKFLOW-GUIDE.md` and identify the current project phase |
| `studio/workflows/brainstorm/` | Run a structured ideation session using the collaboration guide |
| `studio/workflows/code-review/` | Review files directly against repo conventions and design intent |
| `studio/workflows/sprint-plan/` | Create or update a plan under `production/` |
| `studio/workflows/reverse-document/` | Read code or docs and write the missing repo artifact directly |
| `studio/workflows/setup-engine/` | Update root docs and engine reference files manually |

### 4. Preserve Human Approval For Creative Decisions

The collaboration model remains deliberate and user-driven:

- Ask questions before filling in missing game-design decisions.
- Present tradeoffs when multiple valid directions exist.
- Avoid silently writing speculative design docs.
- For implementation work, state assumptions clearly and keep changes visible.

### 5. Prefer Repo-Native Artifacts Over Hidden Session State

When a task produces useful context, write it down in:

- `production/` for planning and delivery artifacts
- `docs/` for reusable guidance
- `studio/templates/` or `docs/examples/` when the pattern should be repeated later

## Suggested Codex Operating Pattern

1. Identify the project phase and missing artifact.
2. Read the smallest set of docs needed to act correctly.
3. Make the change in the repo.
4. Verify links, references, and any commands or tests affected.
5. Leave the repo more legible than you found it.
