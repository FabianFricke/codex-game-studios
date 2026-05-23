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
- Workstation toolchain: `docs/WORKSTATION-TOOLCHAIN.md`
- Example sessions and patterns: `docs/examples/README.md`

## What This Repo Is
- A role-first template for running an indie game project with structured specialist roles, reusable workflows, and documentation templates.
- The repo now treats Codex agents as the primary workflow target.
- The `studio/` directory is the operating system for the game studio model: roles, workflows, templates, and standards.

## Project Configuration
- Engine: Unity 6000.4.8f1
- Language: C#
- Build System: Unity Editor / Unity CLI using `C:\Program Files\Unity 6000.4.8f1\Editor\Unity.exe`
- Asset Pipeline: Blender 5.1.2 via `C:\Users\corey\Tools\bin\blender.cmd`, Codex image workflows for prototype sprites and 2D assets
- Primary Editor: VS Code 1.121.0 via `C:\Users\corey\AppData\Local\Programs\Microsoft VS Code\bin\code.cmd`
- C# IDE / Build Tools: Visual Studio Community 2022 17.14.33 via `C:\Program Files\Microsoft Visual Studio\2022\Community\Common7\IDE\devenv.exe`
- Target Platforms: TBD per game project

Update this section when a specific game project chooses target platforms,
rendering pipeline, or a different pinned engine version. Keep workstation paths
and verification commands in `docs/WORKSTATION-TOOLCHAIN.md`.

## Core Workflow
1. Read `ARCHITECTURE.md` to understand the repo layout and what each directory is for.
2. Read `docs/CODEX-WORKFLOWS.md` before changing docs, prompts, or agent guidance.
3. Read `docs/WORKSTATION-TOOLCHAIN.md` before invoking Unity, Blender, VS Code, Visual Studio, or local validation tools.
4. Keep work visible in the repo: write plans, assumptions, and decisions into versioned files.
5. Preserve the collaboration model in `docs/COLLABORATIVE-DESIGN-PRINCIPLE.md`: ask questions, surface tradeoffs, and avoid silent creative decisions.
6. Use `studio/roles/` to choose the right reasoning frame and `studio/workflows/` to execute common game-dev tasks.

## Working Conventions
- Prefer root docs over tool-specific prompt files as the source of truth.
- Keep new top-level guidance tool-agnostic unless a workflow is inherently platform-specific.
- When adding new agent behavior, write or update the role in `studio/roles/` and any supporting workflow in `studio/workflows/`.
- Do not rely on hidden session state for critical repo behavior.
- Keep reusable docs small and index deeper material instead of duplicating it.
- Keep high-churn Unity projects and generated folders such as `Library/` outside OneDrive unless Corey explicitly chooses otherwise.

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
