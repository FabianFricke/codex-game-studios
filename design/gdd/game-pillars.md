# Game Pillars: Retro Hop

## Document Status
- Version: 1.0
- Last Updated: 2026-05-23
- Approved By: Pending
- Status: Draft

---

## Core Fantasy

You are a tiny clockwork courier moving through bright platforming routes with crisp jumps, readable hazards, optional collectibles, and a clear delivery goal.

---

## Target MDA Aesthetics

| Rank | Aesthetic | How Our Game Delivers It |
| ---- | ---- | ---- |
| 1 | Challenge | Clean jumps, simple hazards, clear level progression |
| 2 | Sensation | Responsive movement, readable sprites, satisfying pickups and landings |
| 3 | Fantasy | Original clockwork courier identity and delivery framing |
| 4 | Discovery | Optional collectibles, small route rewards, visual landmarks |

---

## The Pillars

### Pillar 1: Clean Platforming

**One-Sentence Definition**: Movement must feel responsive, fair, and readable from the first level onward.

**Design Test**: If the player cannot understand why a jump succeeded or failed, the movement, camera, collision, or layout must be revised.

**Department Meaning**
- Game Design: Teach one movement idea at a time.
- Art: Terrain, hazards, and goals must read instantly at gameplay size.
- Audio: Jump, landing, pickup, and fail feedback must be clear.
- Engineering: Prioritize input feel, collision stability, and camera framing.

### Pillar 2: Readable First

**One-Sentence Definition**: Every gameplay object must communicate its rule through silhouette, placement, motion, and contrast.

**Design Test**: If an object only works because we explain it, it is not ready.

**Department Meaning**
- Game Design: No blind jumps, unclear hazards, or misleading collectibles.
- Art: Real sprites only; no squares, no block stand-ins, no vague silhouettes.
- Audio: Feedback reinforces what happened.
- Engineering: Collision and visuals must match.

### Pillar 3: Original Retro Charm

**One-Sentence Definition**: Retro Hop uses familiar platformer grammar with original characters, sprites, props, hazards, level layouts, and world identity.

**Design Test**: If a character, object, enemy, sound, or level beat feels borrowed from an existing franchise, redesign it.

**Department Meaning**
- Game Design: Use genre conventions, not copied content.
- Art: Clockwork courier and toy-mechanical motifs carry the identity.
- Audio: Bright retro feel, original sounds/music only.
- Engineering: Support sprite animation and feedback that sell the identity.

### Pillar 4: Start Friendly

**One-Sentence Definition**: Level 1 teaches the player before it asks for precision.

**Design Test**: If Level 1 requires mastery before introducing the control, simplify the beat.

**Department Meaning**
- Game Design: Safe start, then movement, jump, collect, hazard, goal.
- Art: Level 1 should be bright, welcoming, and visually calm.
- Audio: Positive feedback should make learning feel good.
- Engineering: Recovery should be quick and non-punishing.

---

## Anti-Pillars

- **NOT a copied mascot platformer**: Familiar mechanics are acceptable; copied characters, enemies, sprites, props, music, names, or layouts are not.
- **NOT a punishing first level**: Level 1 should build confidence.
- **NOT fake sprite work**: Colored squares, generated blocks, and abstract placeholders do not qualify as sprites.
- **NOT feature sprawl**: Power-ups, bosses, and extra systems wait until the base platforming grammar works.

---

## Pillar Priority

| Priority | Pillar | Rationale |
| ---- | ---- | ---- |
| 1 | Clean Platforming | Movement feel is the foundation. |
| 2 | Readable First | Platforming only works when the player can read the screen. |
| 3 | Start Friendly | Level 1 must teach the language of the game. |
| 4 | Original Retro Charm | Identity matters, but never at the cost of feel or clarity. |

---

## Pillar Validation Checklist

- [x] 3-5 pillars
- [x] Falsifiable
- [x] Constraining
- [x] Cross-departmental
- [x] Design-tested
- [x] Anti-pillars defined
- [x] Priority-ranked
- [x] MDA-aligned
- [x] Core fantasy served
