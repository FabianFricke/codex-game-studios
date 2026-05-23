# Workstation Toolchain

Last verified: 2026-05-23

This file is the local tool map for Corey's game-development workstation. Agents
should read this before invoking Unity, Blender, editor, build, or validation
tools. Prefer exact paths over PATH lookup when an operation needs reliability.

## Primary Game Development Stack

| Tool | Version | Path / Command | Use |
| ---- | ---- | ---- | ---- |
| Unity Editor | 6000.4.8f1 | `C:\Program Files\Unity 6000.4.8f1\Editor\Unity.exe` | Primary Unity editor and batchmode executable |
| Unity Hub | 3.18.0 | `C:\Program Files\Unity Hub\Unity Hub.exe` | Managing Unity installs, licenses, modules, and projects |
| Blender | 5.1.2 | `C:\Users\corey\Tools\bin\blender.cmd` | Preferred Blender automation entrypoint |
| Blender executable | 5.1.2 | `C:\Program Files\Blender Foundation\Blender 5.1\blender.exe` | Direct Blender executable when the shim is not suitable |
| VS Code | 1.121.0 | `C:\Users\corey\AppData\Local\Programs\Microsoft VS Code\bin\code.cmd` | Primary repo editor |
| Visual Studio Community 2022 | 17.14.33 | `C:\Program Files\Microsoft Visual Studio\2022\Community\Common7\IDE\devenv.exe` | Unity/C# IDE and build tooling |

## Supporting Tools

| Tool | Version | Path / Command | Use |
| ---- | ---- | ---- | ---- |
| Git | 2.54.0.windows.1 | `C:\Program Files\Git\cmd\git.exe` | Source control |
| Bash | 5.2.21 | Git Bash on PATH | Shell scripts and repo helpers |
| Python | 3.14.3 | `C:\Users\corey\AppData\Local\Programs\Python\Python314\python.exe` | Preferred local scripting runtime |
| Python 3 launcher | 3.12.10 | `python3` | Available fallback |
| jq | 1.8.1 | `C:\Users\corey\AppData\Local\Microsoft\WinGet\Links\jq.exe` | JSON inspection |
| Node.js | 24.15.0 | `C:\Program Files\nodejs\node.exe` | JavaScript tooling |
| npm | 11.13.0 | `C:\Program Files\nodejs\npm.ps1` | JavaScript package management |

## Unity Project Placement

Keep this repo in OneDrive as the portable studio/planning/control layer.

Create high-churn Unity engine projects outside OneDrive unless Corey explicitly
chooses otherwise. Use this local pattern by default:

```text
C:\Users\corey\Game Development\Unity\<ProjectName>
```

Rationale: Unity-generated folders such as `Library/`, `Temp/`, `Obj/`, `Logs/`,
and `UserSettings/` create many small files and can overload OneDrive sync. Keep
planning docs here; keep generated engine caches local.

## Unity Notes

- Primary editor: `C:\Program Files\Unity 6000.4.8f1\Editor\Unity.exe`
- Retained older editor: `C:\Program Files\Unity\Hub\Editor\6000.3.9f1\Editor\Unity.exe`
- For batch operations, prefer explicit `Unity.exe` path plus `-batchmode`,
  `-quit`, and `-projectPath`.
- Verify Unity API guidance against the 6000.4 docs and release notes before
  making version-sensitive recommendations.

## Blender Notes

- Prefer `C:\Users\corey\Tools\bin\blender.cmd` for automation.
- For `.blend` inspection and repair workflows, use the active Codex Blender
  skill under `C:\Users\corey\.codex\skills\blender`.
- The Codex Blender Bridge add-on is expected in Blender's user add-ons and can
  be used interactively from `3D View > Sidebar (N) > Codex`.
- When command execution is flaky with long inline expressions, use temporary
  script files and run Blender with `--background <file.blend> --python <script.py>`.

## Update And Verification Commands

Use these commands to verify the local state:

```powershell
code --version
blender --version
git --version
python --version
python3 --version
jq --version
node --version
npm --version
winget list --name "Unity"
winget list --name "Visual Studio Code"
winget list --name "Visual Studio Community"
```

Use these commands to check for managed updates:

```powershell
winget upgrade --id Microsoft.VisualStudioCode
winget upgrade --id Unity.Unity.6000
winget upgrade --id Unity.UnityHub
winget upgrade --id Microsoft.VisualStudio.2022.Community
```

Blender may be installed outside Winget's package tracking. Verify it with:

```powershell
C:\Users\corey\Tools\bin\blender.cmd --version
```

## Official References

- Unity 6000.4 manual: https://docs.unity3d.com/6000.4/Documentation/Manual/
- Unity 6000.4.8f1 release notes: https://unity.com/releases/editor/whats-new/6000.4.8f1
- Blender manual: https://docs.blender.org/manual/en/latest/
- VS Code 1.121 release notes: https://code.visualstudio.com/updates/v1_121
- Visual Studio 2022 release notes: https://learn.microsoft.com/visualstudio/releases/2022/release-notes
