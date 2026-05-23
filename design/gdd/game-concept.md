# Game Concept: Retro Hop

*Created: 2026-05-23*
*Status: Draft*

---

## Elevator Pitch

Retro Hop is a platformer about a tiny clockwork courier who runs, jumps, collects, and dodges through bright obstacle-filled routes to complete deliveries.

---

## Core Identity

| Aspect | Detail |
| ---- | ---- |
| Genre | Platformer |
| Platform | Windows PC first |
| Target Audience | Players who enjoy readable, cheerful, skill-based platforming |
| Player Count | Single-player |
| Session Length | Short levels, replayable for cleaner runs and better collection |
| Monetization | Not defined |
| Estimated Scope | To be defined after Level 1 |
| Comparable Titles | Classic side-scrolling platformers; original character, world, and assets |

---

## Core Fantasy

You are a small clockwork courier with springy movement and a job to finish. The fun comes from mastering clean jumps, reading the route ahead, grabbing optional collectibles, avoiding simple hazards, and reaching the delivery goal with confidence.

---

## Unique Hook

Retro Hop uses familiar platforming verbs through an original clockwork courier identity. The toy-like character and delivery framing give the world a reason for routes, goals, collectibles, gates, and mechanical hazards without copying existing platformer characters or worlds.

---

## Player Experience Analysis

### Target Aesthetics

| Aesthetic | Priority | How We Deliver It |
| ---- | ---- | ---- |
| Challenge | 1 | Clean platforming, readable jumps, simple hazards, skill growth |
| Sensation | 2 | Crisp movement, bright sprites, satisfying collection and landing feedback |
| Fantasy | 3 | Playing as a tiny clockwork courier in a playful mechanical world |
| Discovery | 4 | Optional collectibles and small route rewards |
| Narrative | Supporting | Delivery framing gives levels purpose without heavy story |
| Fellowship | N/A | Single-player focus |
| Expression | N/A | Not a customization-focused game |
| Submission | Supporting | Level 1 should be approachable and low-pressure |

### Key Dynamics

Players should naturally:
- Learn movement by moving forward through safe spaces first.
- Read platforms, collectibles, hazards, and goals visually before committing.
- Try optional collectible routes once basic movement feels comfortable.
- Replay levels to move more cleanly and collect more.

### Core Mechanics

1. Running and directional control.
2. Jumping, landing, and basic air correction.
3. Collectibles placed on safe paths and optional jump arcs.
4. Simple patrol hazards.
5. Delivery goal or endpoint that completes the level.

---

## Player Motivation Profile

### Primary Psychological Needs Served

| Need | How This Game Satisfies It | Strength |
| ---- | ---- | ---- |
| Autonomy | Optional collectibles and route choices within levels | Supporting |
| Competence | Movement mastery, readable hazards, cleaner clears | Core |
| Relatedness | Light character/world charm through the courier identity | Supporting |

### Player Type Appeal

- Achievers: collecting items, finishing levels, improving runs.
- Explorers: noticing optional routes and route details.
- Socializers: not a primary target.
- Competitors: not a primary target.

### Flow State Design

- Onboarding curve: Level 1 introduces movement, jumping, collectibles, hazards, and goal completion in that order.
- Difficulty scaling: Start safe, then combine one idea at a time.
- Feedback clarity: Every jump, collection, hazard contact, and goal completion needs immediate visual feedback.
- Recovery from failure: Level 1 should recover quickly and avoid harsh punishment.

---

## Core Loop

### Moment-to-Moment

Run, jump, land, collect, avoid, and keep moving toward the goal.

### Short-Term

Complete a level route while learning its platforming rhythm and collecting optional items.

### Session-Level

Play one or more short levels, improving movement confidence and collection.

### Long-Term Progression

To be defined after Level 1 proves the base movement, visual identity, and level grammar.

### Retention Hooks

- Mastery: cleaner movement and better collection.
- Curiosity: new routes, hazards, and delivery destinations in later levels.
- Investment: the clockwork courier identity and delivery framing.

---

## Game Pillars

### Pillar 1: Clean Platforming

Movement must feel responsive, readable, and fair.

*Design test*: If a feature makes the player less certain why a jump succeeded or failed, cut or revise it.

### Pillar 2: Readable First

The player should understand platforms, hazards, collectibles, and goals from their silhouettes and placement.

*Design test*: If an object's rule is unclear at gameplay size, the sprite or layout is not approved.

### Pillar 3: Original Retro Charm

The game can use familiar platformer grammar, but all characters, sprites, world details, names, and level layouts must be original.

*Design test*: If an asset or beat feels like it belongs to an existing franchise, redesign it.

### Pillar 4: Start Friendly

Level 1 teaches before it challenges.

*Design test*: If Level 1 requires precision before teaching the control, simplify the beat.

### Anti-Pillars

- NOT a copied mascot platformer: no protected characters, enemy designs, props, names, music, or recognizable level layouts.
- NOT a punishing first level: Level 1 should build confidence, not filter players.
- NOT placeholder art passed as sprites: real usable sprite assets are required before build approval.
- NOT feature sprawl: new mechanics wait until the base platforming grammar is working.

---

## Inspiration and References

| Reference | What We Take From It | What We Do Differently | Why It Matters |
| ---- | ---- | ---- | ---- |
| Classic side-scrolling platformers | Readable movement, collectible routes, simple patrol hazards | Original courier character, clockwork toy identity, original sprites and layouts | Establishes familiar platforming grammar |
| Toy-like mechanical worlds | Wind-up motion, gears, springs, delivery props | Keep visuals bright and readable rather than cluttered | Supports original identity |
| Arcade platforming | Immediate controls and short replayable levels | Keep Level 1 friendly and instructional | Keeps first playable target focused |

---

## Target Player Profile

| Attribute | Detail |
| ---- | ---- |
| Age range | Broad platformer audience |
| Gaming experience | Casual to mid-core |
| Time availability | Short sessions |
| Platform preference | PC first |
| Current games they play | Platformers, arcade games, retro-inspired indies |
| What they're looking for | Clean jumping, readable challenge, charming sprites |
| What would turn them away | Sloppy controls, unclear hazards, copied art, fake placeholder assets |

---

## Technical Considerations

| Consideration | Assessment |
| ---- | ---- |
| Recommended Engine | Unity 6000.4.8f1 |
| Key Technical Challenges | Movement feel, sprite import pipeline, animation, camera framing |
| Art Style | Retro Arcade Pop pixel-art sprites |
| Art Pipeline Complexity | Medium custom 2D |
| Audio Needs | Moderate: jump, collect, hazard, goal, light music |
| Networking | None |
| Content Volume | Level 1 first; broader level count not defined yet |
| Procedural Systems | None planned |

---

## Risks and Open Questions

### Design Risks

- Movement may not feel good without enough tuning time.
- Level 1 could become too busy if too many mechanics are introduced.
- Delivery framing needs to stay light and not slow the platforming.

### Technical Risks

- Sprite production and import must happen before Unity build approval.
- Animation and collision tuning need to match the character scale.
- Camera framing must support readable jumps.

### Market Risks

- Platformers are familiar, so Retro Hop needs strong feel and original visual identity.
- Weak sprites would make the project feel disposable.

### Scope Risks

- Adding mechanics before Level 1 works will dilute the first milestone.
- Treating temporary art as acceptable would create rework and quality drift.

### Open Questions

- What exact delivery goal object completes Level 1?
- What collectible best fits the courier identity?
- What is the first basic hazard: toy beetle, loose gear, slow patrol bot, or something else?
- How many animation frames are required for the first playable character set?

---

## MVP Definition

**Core hypothesis**: Retro Hop works if the clockwork courier feels good to control through a readable introductory platforming level using real sprite assets.

**Required for MVP**:
1. Responsive run and jump.
2. Real player sprite with idle, run, jump/fall, and hurt or respawn state.
3. Real Level 1 terrain sprites or tiles.
4. Real collectible sprite and collection feedback.
5. Real simple hazard sprite and consequence.
6. Goal object that completes Level 1.
7. Level 1 that teaches movement, jumping, collecting, hazards, and goal completion.

**Explicitly NOT in MVP**:
- Multiple levels.
- Power-ups.
- Bosses.
- Complex story scenes.
- Menus beyond what is needed to play/restart/quit.
- Placeholder squares or block stand-ins passed as sprites.

### Scope Tiers

| Tier | Content | Features | Timeline |
| ---- | ---- | ---- | ---- |
| MVP | Level 1 | Core movement, collectibles, one hazard, goal, real sprites | TBD |
| Vertical Slice | Level 1 polished | Art, sound, tuned feel, QA pass | TBD |
| Alpha | Multiple levels | Broader mechanics and content | TBD |
| Full Vision | Complete game | Final level set, audio, polish, release pipeline | TBD |

---

## Next Steps

- [ ] Approve concept direction.
- [ ] Create `design/gdd/game-pillars.md`.
- [ ] Create Level 1 design document.
- [ ] Create art bible / sprite requirements.
- [ ] Run design review.
- [ ] Create implementation work packet.
- [ ] Produce real sprite assets.
- [ ] Begin Unity implementation only after approval.
