# Sprint 001: First Playable

## Sprint Goal

Create the first complete playable level for Retro Hop.

## Tasks

| ID | Task | Owner | Dependencies | Status |
| --- | --- | --- | --- | --- |
| RH-001 | Write production docs | Producer | None | In Progress |
| RH-002 | Create Unity project | Unity Developer | None | Pending |
| RH-003 | Implement runtime scripts | Gameplay Programmer | RH-002 | Pending |
| RH-004 | Generate Level 01 | Tools Programmer | RH-003 | Pending |
| RH-005 | Build Windows executable | Build Engineer | RH-004 | Pending |
| RH-006 | Run QA checklist | QA Lead | RH-005 | Pending |

## Risks

| Risk | Mitigation |
| --- | --- |
| Unity package/module mismatch | Keep `Packages/manifest.json` explicit and check compile logs |
| Movement feels loose | Tune player values before adding features |
| Level readability fails | Keep visual roles color-coded and simple |
