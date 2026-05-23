# Game Design Document: Retro Hop

## Overview

Retro Hop is a one-level 2D side-scrolling platformer. The player starts on
the left, travels right across a compact course, collects optional gems, avoids
or stomps simple walking hazards, and finishes by entering the finish gate.

## Core Loop

1. Read the next obstacle.
2. Move and jump through it.
3. Collect optional gems.
4. Avoid, bypass, or stomp hazards.
5. Continue toward the finish gate.

## Controls

| Action | Keyboard |
| --- | --- |
| Move | A/D or Left/Right |
| Jump | Space, W, or Up |
| Restart | R |
| Quit | Escape |

## Player Rules

- Player accelerates immediately to a readable run speed.
- Jump only starts while grounded.
- Falling below the level respawns the player at the start.
- Touching a hazard from the side respawns the player at the start.
- Landing on a hazard defeats it and bounces the player upward.
- Gems are optional; collecting all gems is not required to finish.

## Level Rules

- The level scrolls horizontally.
- No blind jumps.
- Every hazard must be visible before it threatens the player.
- Optional gems can reward risk, but the critical path remains simple.

## Completion

The level ends when the player enters the finish gate. The build displays a
level-clear message and leaves the player in the completed scene.

## Acceptance Criteria

- Player can complete the level from a fresh launch.
- Player can collect every gem.
- Player can recover from falls and hazard contact.
- At least one hazard can be avoided.
- At least one hazard can be stomped.
- Finish gate triggers level completion.
- Build launches without runtime errors on the target machine.
