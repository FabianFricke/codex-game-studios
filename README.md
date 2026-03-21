<p align="center">
  <h1 align="center">Codex Game Studios</h1>
  <p align="center">
    Turn a single coding-agent session into a full game development studio.
    <br />
    Structured roles, reusable workflows, and a repo that works with Codex first.
  </p>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="MIT License"></a>
  <a href="studio/roles"><img src="https://img.shields.io/badge/roles-48-blueviolet" alt="48 Roles"></a>
  <a href="studio/workflows"><img src="https://img.shields.io/badge/workflows-37-green" alt="37 Workflows"></a>
  <a href="studio/templates"><img src="https://img.shields.io/badge/templates-26-orange" alt="26 Templates"></a>
  <a href="studio/standards"><img src="https://img.shields.io/badge/standards-11-red" alt="11 Standards"></a>
  <a href="AGENTS.md"><img src="https://img.shields.io/badge/entrypoint-AGENTS.md-111827" alt="AGENTS.md"></a>
  <a href="https://ko-fi.com/donchitos"><img src="https://img.shields.io/badge/Ko--fi-Support%20this%20project-ff5e5b?logo=ko-fi&logoColor=white" alt="Ko-fi"></a>
</p>

---

## Why This Exists

Building a game solo with AI is powerful — but a single chat session has no structure. No one stops you from hardcoding magic numbers, skipping design docs, or writing spaghetti code. There's no QA pass, no design review, no one asking "does this actually fit the game's vision?"

**Codex Game Studios** solves this by giving your AI session the structure of a real studio. Instead of one general-purpose assistant, you get a documented studio hierarchy, specialist role definitions, reusable workflows, templates, and standards that keep work legible. The repo is organized around a Codex-native `studio/` library plus root docs that tell agents where to look next.

The result: you still make every decision, but now you have a team that asks the right questions, catches mistakes early, and keeps your project organized from first brainstorm to launch.

---

## Table of Contents

- [What's Included](#whats-included)
- [Studio Hierarchy](#studio-hierarchy)
- [Codex Workflow Model](#codex-workflow-model)
- [Getting Started](#getting-started)
- [Upgrading](#upgrading)
- [Project Structure](#project-structure)
- [How It Works](#how-it-works)
- [Design Philosophy](#design-philosophy)
- [Customization](#customization)
- [Platform Support](#platform-support)
- [Community](#community)
- [License](#license)

---

## What's Included

| Category | Count | Description |
|----------|-------|-------------|
| **Roles** | 48 | Specialist role prompts across design, programming, art, audio, narrative, QA, and production |
| **Workflows** | 37 | Reusable Codex-friendly workflows for ideation, reviews, planning, implementation, and release |
| **Standards** | 11 | Domain-specific quality standards for gameplay, engine, AI, UI, networking, docs, and tests |
| **Templates** | 26 | Document templates for GDDs, ADRs, sprint plans, economy models, faction design, and more |

## Studio Hierarchy

Roles are organized into three tiers, matching how real studios operate:

```
Tier 1 — Directors (Opus)
  creative-director    technical-director    producer

Tier 2 — Department Leads (Sonnet)
  game-designer        lead-programmer       art-director
  audio-director       narrative-director    qa-lead
  release-manager      localization-lead

Tier 3 — Specialists (Sonnet/Haiku)
  gameplay-programmer  engine-programmer     ai-programmer
  network-programmer   tools-programmer      ui-programmer
  systems-designer     level-designer        economy-designer
  technical-artist     sound-designer        writer
  world-builder        ux-designer           prototyper
  performance-analyst  devops-engineer       analytics-engineer
  security-engineer    qa-tester             accessibility-specialist
  live-ops-designer    community-manager
```

### Engine Specialists

The template includes role sets for all three major engines. Use the set that matches your project:

| Engine | Lead Agent | Sub-Specialists |
|--------|-----------|-----------------|
| **Godot 4** | `godot-specialist` | GDScript, Shaders, GDExtension |
| **Unity** | `unity-specialist` | DOTS/ECS, Shaders/VFX, Addressables, UI Toolkit |
| **Unreal Engine 5** | `unreal-specialist` | GAS, Blueprints, Replication, UMG/CommonUI |

## Codex Workflow Model

The repo exposes the studio system through normal markdown entrypoints:

- Start with `AGENTS.md`
- Use `ARCHITECTURE.md` to understand the repo layout
- Follow `docs/CODEX-WORKFLOWS.md` for Codex-specific usage
- Use `docs/WORKFLOW-GUIDE.md` for the end-to-end game-project process
- Use `studio/roles/`, `studio/workflows/`, `studio/templates/`, and `studio/standards/` as the operating library

## Getting Started

### Prerequisites

- [Git](https://git-scm.com/)
- A Codex-compatible environment that can read repo docs and edit files
- **Recommended**: [jq](https://jqlang.github.io/jq/) and Python 3 for some helper scripts

### Setup

1. **Clone or use as template**:
   ```bash
   git clone https://github.com/daveashworth/Codex-Game-Studios.git my-game
   cd my-game
   ```

2. **Start with the Codex entrypoint**:
   - Read `AGENTS.md`
   - Read `ARCHITECTURE.md`
   - Read `docs/CODEX-WORKFLOWS.md`

3. **Choose your phase** using `docs/WORKFLOW-GUIDE.md`.
4. **Use the studio library**:
   - Pick a role from `studio/roles/`
   - Follow a workflow in `studio/workflows/`
   - Create artifacts from `studio/templates/`
   - Review against `studio/standards/`

## Upgrading

Already using an older version of this template? See [UPGRADING.md](UPGRADING.md)
for step-by-step migration instructions, a breakdown of what changed between
versions, and which files are safe to overwrite vs. which need a manual merge.

## Project Structure

```
AGENTS.md                           # Codex entrypoint and project configuration
ARCHITECTURE.md                     # Repo map and dependency direction
docs/
  CODEX-WORKFLOWS.md                # Codex-specific usage
  WORKFLOW-GUIDE.md                 # End-to-end game project flow
studio/
  roles/                            # 48 specialist role definitions
  workflows/                        # 37 reusable workflow playbooks
  templates/                        # Reusable design and production templates
  standards/                        # Quality standards and review lenses
  docs/                             # Supporting studio references
src/                                # Game source code
assets/                             # Art, audio, VFX, shaders, data files
design/                             # GDDs, narrative docs, level designs
docs/                               # Technical documentation and ADRs
tests/                              # Test suites
tools/                              # Build and pipeline tools
prototypes/                         # Throwaway prototypes (isolated from src/)
production/                         # Sprint plans, milestones, release tracking
```

## How It Works

### Agent Coordination

Agents follow a structured delegation model:

1. **Vertical delegation** — directors delegate to leads, leads delegate to specialists
2. **Horizontal consultation** — same-tier agents can consult each other but can't make binding cross-domain decisions
3. **Conflict resolution** — disagreements escalate up to the shared parent (`creative-director` for design, `technical-director` for technical)
4. **Change propagation** — cross-department changes are coordinated by `producer`
5. **Domain boundaries** — agents don't modify files outside their domain without explicit delegation

### Collaborative, Not Autonomous

This is **not** an auto-pilot system. Every agent follows a strict collaboration protocol:

1. **Ask** — agents ask questions before proposing solutions
2. **Present options** — agents show 2-4 options with pros/cons
3. **You decide** — the user always makes the call
4. **Draft** — agents show work before finalizing
5. **Approve** — nothing gets written without your sign-off

You stay in control. The agents provide structure and expertise, not autonomy.

### Automated Safety

The studio system relies on explicit workflows and review passes rather than a hidden agent runtime:

- Workflows encode the expected sequence of questions, decisions, artifacts, and reviews.
- Standards provide the review checklist for each domain.
- Templates keep outputs consistent enough for both humans and agents to navigate.
- Root docs make the system discoverable without relying on tool-specific hooks.

### Path-Scoped Rules

Coding standards are automatically enforced based on file location:

| Path | Enforces |
|------|----------|
| `src/gameplay/**` | Data-driven values, delta time usage, no UI references |
| `src/core/**` | Zero allocations in hot paths, thread safety, API stability |
| `src/ai/**` | Performance budgets, debuggability, data-driven parameters |
| `src/networking/**` | Server-authoritative, versioned messages, security |
| `src/ui/**` | No game state ownership, localization-ready, accessibility |
| `design/gdd/**` | Required 8 sections, formula format, edge cases |
| `tests/**` | Test naming, coverage requirements, fixture patterns |
| `prototypes/**` | Relaxed standards, README required, hypothesis documented |

## Design Philosophy

This template is grounded in professional game development practices:

- **MDA Framework** — Mechanics, Dynamics, Aesthetics analysis for game design
- **Self-Determination Theory** — Autonomy, Competence, Relatedness for player motivation
- **Flow State Design** — Challenge-skill balance for player engagement
- **Bartle Player Types** — Audience targeting and validation
- **Verification-Driven Development** — Tests first, then implementation

## Customization

This is a **template**, not a locked framework. Everything is meant to be customized:

- **Add/remove roles** — delete role files you don't need, add new ones for your domains
- **Edit role prompts** — tune role behavior, add project-specific knowledge
- **Modify workflows** — adjust playbooks to match your team's process
- **Add standards** — create new path-scoped standards for your project's directory structure
- **Extend tooling** — add validation or helper scripts that fit your workflow
- **Pick your engine** — use the Godot, Unity, or Unreal role set (or none)

## Platform Support

Tested on **Windows 10** with Git Bash. Repo scripts and workflows use POSIX-compatible patterns (`grep -E`, not `grep -P`) and are intended to work on macOS and Linux as well.

## Community

- **Discussions** — [GitHub Discussions](https://github.com/daveashworth/Codex-Game-Studios/discussions) for questions, ideas, and showcasing what you've built
- **Issues** — [Bug reports and feature requests](https://github.com/daveashworth/Codex-Game-Studios/issues)

---

*This project is under active development. The role architecture, workflows, and coordination system are solid and usable today, but there is more coming.*

## License

MIT License. See [LICENSE](LICENSE) for details.
