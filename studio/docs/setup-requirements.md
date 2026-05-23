# Setup Requirements

This template requires only a few core tools. Optional helpers improve
validation and convenience but are not part of the control plane.

## Required

| Tool | Purpose | Install |
| ---- | ---- | ---- |
| **Git** | Version control, branch management | [git-scm.com](https://git-scm.com/) |
| **Codex-compatible environment** | AI runtime that can read repo files and edit them | Use your preferred setup |

## Current Workstation Toolchain

This workstation is already configured for Unity-first development. Agents
should read `docs/WORKSTATION-TOOLCHAIN.md` for exact executable paths before
invoking local tools.

| Tool | Current Version |
| ---- | ---- |
| Unity Editor | 6000.4.8f1 |
| Unity Hub | 3.18.0 |
| Blender | 5.1.2 |
| VS Code | 1.121.0 |
| Visual Studio Community 2022 | 17.14.33 |
| Git | 2.54.0.windows.1 |
| Python | 3.14.3 |
| Node.js | 24.15.0 |
| jq | 1.8.1 |

## Recommended

| Tool | Used By | Purpose | Install |
| ---- | ---- | ---- | ---- |
| **jq** | Validation helpers | JSON parsing and inspection | See below |
| **Python 3** | Validation helpers | JSON validation and scripting | [python.org](https://www.python.org/) |
| **Bash** | Repo utilities | Shell script execution for helper scripts | Included with Git for Windows |

### Installing jq

**Windows** (any of these):
```
winget install jqlang.jq
choco install jq
scoop install jq
```

**macOS**:
```
brew install jq
```

**Linux**:
```
sudo apt install jq     # Debian/Ubuntu
sudo dnf install jq     # Fedora
sudo pacman -S jq       # Arch
```

## Platform Notes

### Windows
- Git for Windows includes **Git Bash**, which provides the `bash` command
  used by many repo utilities
- Ensure Git Bash is on your PATH (default if installed via the Git installer)

### macOS / Linux
- Bash is available natively
- Install `jq` via your package manager for full helper-script support

## Verifying Your Setup

Run these commands to check prerequisites:

```bash
git --version          # Should show git version
bash --version         # Should show bash version
jq --version           # Should show jq version (optional)
python3 --version      # Should show python version (optional)
```

## What Happens Without Optional Tools

| Missing Tool | Effect |
| ---- | ---- |
| **jq** | Some validation helpers and inspection commands become less convenient. |
| **Python 3** | Some validation helpers and utility scripts may be unavailable. |
| **Both** | The repo still works, but you lose some automation for validation and scripting. |

## Recommended IDE

Use VS Code as the primary editor for repo work and Visual Studio Community
2022 for Unity/C# IDE and build tooling when needed.
