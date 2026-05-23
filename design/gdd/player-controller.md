# Player Controller: Retro Hop

## Overview

The player controller supports horizontal movement, jump, landing, respawn,
hazard stomp, gem collection, and finish-gate interaction.

## Player Fantasy

The character feels light, quick, and reliable. The player should feel that
missed jumps are their own timing error, not the controls fighting them.

## Rules

- Move left/right with keyboard input.
- Jump only when grounded.
- Use a small jump buffer so intentional jumps are not lost at landing.
- Use a small coyote window so edge jumps feel fair.
- Horizontal movement changes direction immediately.
- The player respawns at the start after falling or hazard side contact.

## Initial Tuning

| Value | Initial Target |
| --- | --- |
| Move speed | 8 |
| Jump speed | 14 |
| Gravity scale | 3.4 |
| Coyote time | 0.08 seconds |
| Jump buffer | 0.10 seconds |
| Stomp bounce | 10 |

## Edge Cases

- Jump input slightly before landing should fire on landing.
- Jump input slightly after leaving an edge should still fire.
- Falling out of the world should never softlock.
- Stomping a hazard should not also respawn the player.
- Reaching the finish gate should disable fail interactions.

## Acceptance Criteria

- Player crosses every required jump.
- Player cannot air-jump repeatedly.
- Player can stomp one hazard reliably.
- Player respawns after falling.
- Player completes the level with keyboard only.
