# Technical Preferences

<!-- Populated by /setup-engine. Updated as the user makes decisions throughout development. -->
<!-- All roles reference this file for project-specific standards and conventions. -->

## Engine & Language

- **Engine**: Unity 6000.4.8f1
- **Language**: C#
- **Rendering**: Unity render pipeline selected per project
- **Physics**: Unity Physics / project-selected physics stack
- **Unity Editor Path**: `C:\Program Files\Unity 6000.4.8f1\Editor\Unity.exe`
- **Unity Hub Path**: `C:\Program Files\Unity Hub\Unity Hub.exe`

## Naming Conventions

- **Classes**: PascalCase
- **Variables**: camelCase
- **Signals/Events**: PascalCase event names with clear past-tense or action naming
- **Files**: Match primary type name for C# scripts
- **Scenes/Prefabs**: PascalCase descriptive names
- **Constants**: PascalCase for C# constants unless a project standard says otherwise

## Performance Budgets

- **Target Framerate**: 60 FPS default, revise per platform
- **Frame Budget**: 16.67 ms default, revise per platform
- **Draw Calls**: Project-specific budget after art direction and target platform are known
- **Memory Ceiling**: Project-specific budget after target platform is known

## Testing

- **Framework**: Unity Test Framework for Unity projects; plain .NET tests where engine isolation is practical
- **Minimum Coverage**: Risk-based until a production project sets a numeric gate
- **Required Tests**: Balance formulas, gameplay systems, networking (if applicable)

## Forbidden Patterns

<!-- Add patterns that should never appear in this project's codebase -->
- [None configured yet — add as architectural decisions are made]

## Allowed Libraries / Addons

<!-- Add approved third-party dependencies here -->
- Blender 5.1.2 for 3D asset creation and review via `C:\Users\corey\Tools\bin\blender.cmd`
- Codex image workflows for prototype sprites and 2D asset generation

## Local Toolchain

- **Primary editor**: VS Code 1.121.0 via `C:\Users\corey\AppData\Local\Programs\Microsoft VS Code\bin\code.cmd`
- **C# IDE / build tooling**: Visual Studio Community 2022 17.14.33 via `C:\Program Files\Microsoft Visual Studio\2022\Community\Common7\IDE\devenv.exe`
- **Git**: 2.54.0.windows.1 via `C:\Program Files\Git\cmd\git.exe`
- **Python**: 3.14.3 via `C:\Users\corey\AppData\Local\Programs\Python\Python314\python.exe`
- **Node.js**: 24.15.0 via `C:\Program Files\nodejs\node.exe`
- **jq**: 1.8.1 via `C:\Users\corey\AppData\Local\Microsoft\WinGet\Links\jq.exe`
- **Full workstation map**: `docs/WORKSTATION-TOOLCHAIN.md`

## Architecture Decisions Log

<!-- Quick reference linking to full ADRs in docs/architecture/ -->
- [No ADRs yet - use `architecture-decision` to create one]
