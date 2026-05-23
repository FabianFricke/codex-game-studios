# Technical Architecture: Retro Hop

## Repositories And Paths

Studio/control repo:

```text
C:\Users\corey\OneDrive\Documents\Game Development
```

Unity project:

```text
C:\Users\corey\Game Development\Unity\RetroHop
```

## Engine

- Unity Editor: 6000.4.8f1
- Build target: Windows x64
- Rendering: 2D sprites
- Physics: Unity 2D physics

## Unity Structure

```text
Assets/_RetroHop/
  Art/
    Sprites/
  Scenes/
  Scripts/
    Editor/
    Runtime/
Packages/
ProjectSettings/
```

## Runtime Components

- `RetroHopPlayer`: player movement, jump buffering, coyote time, respawn.
- `RetroHopGameManager`: game state, gem count, restart, finish state.
- `RetroHopCameraFollow`: horizontal camera follow.
- `RetroHopGem`: pickup behavior.
- `RetroHopWalker`: simple walking hazard.
- `RetroHopGoal`: finish gate.
- `RetroHopKillZone`: fall recovery.

## Editor Components

- `RetroHop.Editor.SceneBuilder`: creates the Level 01 scene and source
  sprites.
- `RetroHop.Editor.LocalBuild`: builds the Windows development executable.

## Build Output

```text
C:\Users\corey\Game Development\Builds\Retro Hop\WindowsDev\RetroHop.exe
```

## Source Control Boundary

The Unity project is its own Git repo. Track:

- `Assets/**`
- `Packages/**`
- `ProjectSettings/**`
- `.gitignore`
- `README.md`

Ignore generated folders:

- `Library/`
- `Temp/`
- `Obj/`
- `Logs/`
- `UserSettings/`
- `Build/`
- `Builds/`
