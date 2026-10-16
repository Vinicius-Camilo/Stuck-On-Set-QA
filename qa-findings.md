# Stuck On Set — QA Bug Reports and Observations

This document collects apparent technical issues, usability concerns, balance observations, and improvement suggestions identified during an independent exploratory playtest.

## Testing Context

- **Game:** Stuck On Set
- **Test date:** October 16, 2026
- **Version:** Version 7, available since October 13, 2026
- **Platform:** PC
- **Primary input device:** Keyboard and mouse
- **Additional input device:** Controller/gamepad
- **Approach:** Independent exploratory testing based on player experience, without a predefined test script.
- **Environment:** Final executable, without access to source code or the development environment.
- **Project origin:** Independent QA practice through Play2Review.

### How to Interpret These Reports

The reports describe observed behavior and its potential impact on the player. Suggested priorities are independent classifications for portfolio purposes, not official priorities assigned by the developers.

- **Apparent technical bug:** Behavior that appears incorrect or inconsistent.
- **Usability:** Behavior that makes the game more difficult to understand or use.
- **Balance/design:** Subjective feedback about the effectiveness, difficulty, or behavior of a mechanic.
- **Suggestion:** A proposed improvement that does not imply an existing defect.

Technical causes have not been confirmed. Findings have not been retested against subsequent builds.

---

# Apparent Technical Issues

## BUG-001 — Inconsistent Keyboard Movement

**Category:** Controls / Movement  
**Suggested priority:** High  
**Type:** Apparent technical bug

### Description

Horizontal movement appears significantly faster than forward and backward movement. Additionally, pressing two directions simultaneously does not appear to produce consistent diagonal movement.

The behavior does not appear to manifest in the same way when using a controller.

### Impact

Inconsistent movement affects directional precision and may make combat and dodging more difficult.

### Reproduction Steps

1. Start a session using keyboard and mouse.
2. Move the character horizontally.
3. Move the character forward and backward.
4. Compare the perceived movement speeds.
5. Press two directional inputs simultaneously and observe diagonal movement.

**Limitation:** No objective movement-speed measurements were taken. The difference was observed during gameplay.

---

## BUG-002 — Menus Appear Incompatible with Controller Input

**Category:** Controls / Interface  
**Suggested priority:** Medium  
**Type:** Apparent technical bug

### Description

During testing, menus did not appear to be fully interactive when using a controller/gamepad.

### Impact

Players who prefer controller input may have difficulty navigating the interface or accessing certain options.

### Reproduction Steps

Inconsistent interaction was observed while using a controller. Sufficient detailed steps were not recorded to specify which menu elements failed in each situation.

---

## BUG-003 — Dash Can Be Triggered While Main Menu Is Open

**Category:** Controls / Interface  
**Suggested priority:** Low  
**Type:** Behavior requiring verification

### Description

The dash could be triggered while the Main Menu was open, although normal character movement did not appear to work.

### Impact

The action may be triggered accidentally while navigating the interface.

### Reproduction Steps

1. Open the main menu of the game.
2. Press the dash input.
3. Observe whether the character performs the action.

**Note:** It was not possible to determine whether this behavior is intentional.

---

## BUG-004 — Incorrect Dash Instructions in the Tutorial

**Category:** Tutorial / Controls  
**Suggested priority:** Medium  
**Type:** Documentation inconsistency

### Description

The tutorial indicates RT/R2 for the dash command. During testing, RT/R2 fired the weapon, while RB/R1 performed the dash.

### Impact

The instructions may cause players to use the wrong command, particularly during the first few minutes of gameplay.

### Expected Result

The instructions displayed in the tutorial should match the controls actually configured in the game.

---

## BUG-005 — Incorrect Wall Collisions

**Category:** Physics / Collision  
**Suggested priority:** Medium  
**Type:** Apparent technical bug

### Description

Some wall collisions appeared inconsistent with the visible geometry of the environment.

### Impact

This behavior may interfere with movement and create the impression that the character is colliding with invisible obstacles or passing through inappropriate boundaries.

### Evidence

The behavior was observed during testing. The existence of supporting footage does not mean that a recording is published in this repository.

**Limitation:** Sufficiently precise reproduction steps were not documented to establish a specific scenario.

---

## BUG-006 — Enemies Spawn Partially Inside the Ground

**Category:** Spawning / Physics  
**Suggested priority:** Medium  
**Type:** Apparent technical bug

### Description

Some enemies appeared to spawn partially inside the ground and, in certain situations, became unable to move. They could apparently still be hit by weapon fire.

### Impact

This behavior may interfere with enemy movement and make combat encounters inconsistent.

### Limitation

The technical cause could not be determined, and it was not possible to confirm whether the issue occurs under specific spawning conditions or specific enemy types.

---

# Usability and Clarity

## OBS-001 — Excessive Visual Clutter in the Call Sheet

**Category:** Interface / UX  
**Suggested priority:** Low  
**Type:** Usability observation

### Description

The Call Sheet contains many visual and decorative elements, making it less obvious which information is functional and which elements are primarily thematic.

### Impact

Players may need additional time to locate relevant information.

### Suggestion

Visually separate functional information from decorative elements while preserving the movie-production theme.

---

## OBS-002 — Tutorial Relies Too Heavily on the Manual

**Category:** Tutorial / UX  
**Suggested priority:** Medium  
**Type:** Usability observation

### Description

The tutorial appears to assume that players will consult the manual to understand certain systems.

### Impact

Players who expect to learn mechanics directly through gameplay may struggle to understand controls, upgrades, or combat rules.

### Suggestion

Add brief contextual explanations for essential mechanics and allow the manual to provide supplementary information.

---

## OBS-003 — Insufficient Contrast in the ESC Menu

**Category:** Interface / Accessibility  
**Suggested priority:** Low  
**Type:** Usability observation

### Description

The menu opened with ESC uses white text on a gray background, which appears to reduce readability.

### Suggestion

Increase the contrast between text and background, checking legibility under different lighting conditions and display settings.

---

## OBS-004 — Camera Can Be Mistaken for an Enemy

**Category:** Camera / Visual Presentation  
**Suggested priority:** Low  
**Type:** Usability observation

### Description

In some situations, the camera appears to move too close to scenery or clip through environmental objects. Its appearance was mistaken for an enemy during gameplay.

### Impact

Players may misinterpret environmental elements as threats and waste ammunition.

### Suggestion

Review camera behavior near objects and walls, and evaluate the visual clarity of elements presented on screen.

---

## OBS-005 — Differences Between Enemy Types Are Not Obvious

**Category:** Combat / Visual Clarity  
**Suggested priority:** Medium  
**Type:** Usability observation

### Description

Some enemy types are difficult to distinguish during combat. More obvious differences could be identified in certain cases, such as the clown with slower ranged attacks and larger enemies with greater health pools. Other enemy types appeared similar in behavior or threat.

### Impact

Players may have difficulty quickly identifying threats and prioritizing targets during combat.

### Suggestion

Strengthen differences in visual design, animations, silhouettes, or attack patterns between enemy types.

---

## OBS-006 — Poor Attack Telegraphing and Unclear Damage Sources

**Category:** Combat / Player Feedback  
**Suggested priority:** High  
**Type:** Usability observation

### Description

Some attacks do not appear to provide sufficiently clear visual warning cues before dealing damage. Additionally, certain projectile and enemy behaviors appear inconsistent, making it difficult to identify the source of damage received.

### Impact

Players may feel that damage occurs unexpectedly. This can also make challenges requiring a no-damage run more difficult.

### Suggestion

Review the visual and audio cues preceding attacks and make the relationship between enemy behavior and damage more consistent.

---

## OBS-007 — Boss Immunity Text Creates Uncertainty

**Category:** Combat / Mechanic Clarity  
**Suggested priority:** Medium  
**Type:** Usability observation

### Description

The large “IMMUNE” text displayed during the boss encounter initially created uncertainty about how to progress. It was not immediately clear whether the player needed to wait for the immunity to end, weaken the boss, or attack its protection.

An attempt was later made to attack the boss's shield.

### Impact

Players may not understand which action is required to progress through the encounter.

### Suggestion

Evaluate whether the immunity text and visual representation of the shield communicate redundant or insufficient information. A contextual indicator could clarify the objective without removing the challenge.

---

## OBS-008 — Boss Attacks Appear Easy to Dodge

**Category:** Combat / Balance  
**Suggested priority:** Low  
**Type:** Subjective design observation

### Description

During the tested encounter, some boss attacks appeared relatively easy to avoid with small movements.

### Impact

Depending on the intended design, this may reduce the challenge of the encounter.

### Limitation

This is a subjective impression based on the observed gameplay. It was not possible to evaluate the balance of later bosses or determine the intended difficulty of the encounter.

---

## OBS-009 — Clown Balloons Cause Damage When Shot

**Category:** Combat / Interaction Clarity  
**Suggested priority:** Medium  
**Type:** Behavior requiring clarification

### Description

Clown balloons damage the player when touched. During testing, shooting the balloons also appeared to damage the player.

Although contact damage seems understandable, the consequences of shooting the balloons were unclear.

### Impact

During encounters involving multiple enemies and projectiles, it may be difficult to avoid the balloons and determine which action caused the damage.

### Suggestion

If damage caused by shooting the balloons is intentional, communicate the interaction through visual cues, audio feedback, or contextual instructions.

---

## OBS-010 — Sentinel Spheres Require Risky Proximity

**Category:** Combat / Balance  
**Suggested priority:** Low  
**Type:** Subjective design observation

### Description

Sentinel Spheres orbit the player at a distance that appears to require approaching enemies too closely to deal damage.

### Impact

The mechanic may encourage players to expose themselves to attacks to use the upgrade effectively.

### Suggestion

Evaluate the orbit distance and the relationship between risk, range, and upgrade effectiveness.

---

## OBS-011 — Two-Small-Trap Upgrade Feels Less Controllable

**Category:** Upgrades / Balance  
**Suggested priority:** Low  
**Type:** Subjective design observation

### Description

The upgrade that produces two small traps appeared less predictable or less effective in practice than using a single trap.

### Impact

Players may perceive the upgrade as offering limited benefits or being difficult to use consistently.

### Suggestion

Review trap placement, area of effect, and effectiveness so that the upgrade provides clear advantages.

---

## OBS-012 — Limited Long-Range Accuracy of Ol' Painless

**Category:** Weapons / Balance  
**Suggested priority:** Low  
**Type:** Subjective design observation

### Description

Ol' Painless has a reasonable rate of fire, and the restriction on movement while firing felt less problematic than expected. However, its long-range accuracy appears limited, with few projectiles hitting targets.

No obvious way to improve accuracy through aiming or available upgrades was identified during testing.

### Impact

The weapon may feel unreliable in long-range encounters.

### Suggestion

Evaluate accuracy, spread, and available options for improving the weapon's effectiveness at different ranges.

---

## OBS-013 — Galleria Shotgun May Be Overpowered

**Category:** Weapons / Balance  
**Suggested priority:** Low  
**Type:** Subjective design observation

### Description

The Galleria Shotgun provided a satisfying experience and appeared to be one of the most effective weapons tested.

### Impact

If its effectiveness is excessively high compared with other weapons, this may reduce the incentive to experiment with alternative options.

### Limitation

No damage measurements or controlled comparative tests were performed. This observation reflects the experience during the session.

---

## OBS-014 — Relationship Between Genre, Upgrades, and Maximum Health Is Unclear

**Category:** Progression / UX  
**Suggested priority:** Medium  
**Type:** Usability observation

### Description

The acquisition and use of Genre points were not sufficiently clear. Upgrades considered meaningful appeared to require sacrificing maximum health.

### Impact

Players may struggle to understand the costs, benefits, and consequences of progression decisions.

### Suggestion

Explain how points are acquired, what upgrades cost, and what happens when maximum health is sacrificed.

---

## OBS-015 — Trap Setup Time Is Not Obvious

**Category:** Combat / Player Feedback  
**Suggested priority:** Low  
**Type:** Usability observation

### Description

In some situations, enemies walked over player-placed traps without any apparent effect. It later became clearer that traps have a setup period.

The behavior appears to be part of the mechanic, but the activation delay was not initially obvious.

### Impact

Players may interpret the lack of an effect as a trap malfunction.

### Suggestion

Communicate the setup state through an animation, visual indicator, or audio cue.

---

## OBS-016 — Budget Appears to Allow Purchase of Most Upgrades

**Category:** Economy / Balance  
**Suggested priority:** Low  
**Type:** Subjective design observation

### Description

The available budget appears generous, allowing players to purchase many of the presented upgrades.

### Impact

If the intended design is to encourage difficult resource-allocation decisions, the economy may not create sufficiently meaningful choices.

### Limitation

It was not possible to determine whether the generous budget is intentional, particularly given the possibility that the tested version may also be used to evaluate systems in development.

---

## OBS-017 — Offer Multiple Choices for the Next Round

**Category:** Design Suggestion  
**Suggested priority:** Informational  
**Type:** Improvement suggestion

### Description

One possibility would be to offer more than one option for the next round or encounter, similar to the path and encounter selection found in games such as *Hades*.

### Potential Benefit

This could increase run variety and allow players to influence the type of challenge or reward they want to pursue.

### Limitation

This is a design suggestion, not a reported defect.

---

# Testing Limitations

- The test was conducted on October 16, 2026, using Version 7, available since October 13, 2026.
- Testing was exploratory and based on player experience, without a predefined test script.
- Reproduction steps were included only when the behavior could be described clearly using the final executable.
- The causes of the reported behaviors were not established.
- Findings were not retested against subsequent builds.
- No performance drops, crashes, or other performance issues were observed or reported during the session.
- No meta-progression system was noticed during testing. Its presence or absence was not independently verified.

The absence of a reported issue does not establish that the corresponding system is free of defects.

# Feedback and Corrections

These reports were independently created for QA practice through Play2Review. The findings represent the player's observations and have not been confirmed by the developers.

If a finding is inaccurate, has already been addressed, or requires additional context, I am open to reviewing the documentation.

The developers may contact me to discuss possible corrections or the removal of specific material. This repository may be updated based on feedback regarding the observations submitted through Play2Review.
