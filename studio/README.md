# Studio Library

This directory is the Codex-native operating library for the game studio model.

## Contents

- `roles/`
  - Specialist role definitions that describe responsibilities, review lenses,
    delegation boundaries, and collaboration behavior.
- `workflows/`
  - Reusable playbooks for common game-development tasks such as brainstorming,
    planning, design review, code review, engine setup, and release prep.
- `templates/`
  - Reusable markdown templates for design, technical, production, release, and
    post-mortem artifacts.
- `standards/`
  - Domain-specific rules and quality expectations for gameplay, engine, UI,
    networking, tests, narrative, and related areas.
- `docs/`
  - Supporting references such as role rosters, coordination maps, standards
    summaries, directory structure, and technical preferences.

## Usage Pattern

1. Pick a role in `roles/` that matches the work.
2. Use a workflow in `workflows/` to structure the task.
3. Create or update artifacts with a template from `templates/`.
4. Review the result against the matching file in `standards/`.

## Migration Note

Some files in this library still use legacy slash-style examples and may mention
workflow names with a leading `/`. In Codex, treat those as normal playbooks and
map `/name` to `workflows/name/`.
