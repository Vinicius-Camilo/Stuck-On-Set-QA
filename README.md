# Playtest Report — Stuck On Set

Documentation of an independent exploratory playtest of *Stuck On Set*, focusing on potential bugs, usability, combat clarity, and player experience.

## Project Context

This project was independently created for QA (Quality Assurance) practice through the Play2Review website.

The goal is to document observations from hands-on gameplay, identify potential defects and usability issues, and practice writing structured QA reports.

Testing was performed using the game's executable, without access to source code or the development environment.

This repository is an independent portfolio project. It is not an official QA report and is not formally affiliated with the game's developers.

## Test Information

| Field | Details |
|---|---|
| Game | Stuck On Set |
| Game page | [itch.io — Stuck On Set](https://driftingsignal.itch.io/stuck-on-set) |
| Test date | October 16, 2026 |
| Tested version | Version 7 |
| Version availability date | October 13, 2026 |
| Test type | Exploratory |
| Test platform | PC |
| Primary input device | Keyboard and mouse |
| Additional input device | Controller/gamepad |
| Test environment | Final executable available to players |
| Recording tool | OBS Studio was used during the session; no recording is published in this repository |

## Testing Approach

Testing was exploratory and based on my experience as a long-time gamer. No predefined test script or formal test case suite was used.

During the session, I explored the controls, menus, weapons, upgrades, traps, enemies, combat encounters, and other systems available in the tested version.

Findings describe behaviors observed during gameplay. Reproduction steps are included only when the behavior could be described clearly using the available executable, without access to source code or the development environment.

The findings should not automatically be interpreted as confirmed defects. Some behaviors may be intentional design choices, known limitations, or issues requiring further investigation.

## Key Findings

### Controls and Movement

- Keyboard movement appears to have different speeds along the horizontal and forward/backward axes.
- Diagonal movement does not appear to work consistently.
- Menus do not appear to be fully usable with a controller.
- The tutorial provides incorrect instructions for the dash command.
- The dash feels responsive and fluid, but the overall movement experience is affected by the observed control issues.

### Combat and Enemies

- Some enemy types are difficult to distinguish during combat.
- Certain attacks do not appear to provide sufficiently clear visual warning cues before dealing damage.
- Inconsistent-looking projectile and enemy behaviors make the source of damage difficult to identify.
- Some enemies appear to spawn partially inside the ground and may become unable to move.
- The boss's immunity text can create uncertainty about how to overcome its defenses.
- Clown balloons appear to damage the player when touched and when shot, although the intended behavior was unclear during testing.

### Weapons, Upgrades, and Progression

- The Galleria Shotgun provides a satisfying combat experience but appeared potentially stronger than other tested options.
- Ol' Painless has a reasonable rate of fire, but its long-range accuracy appears limited.
- Sentinel Spheres may require the player to approach enemies dangerously closely.
- The upgrade that creates two small traps feels less controllable than using a single trap.
- The relationship between Genre points, upgrades, and sacrificing maximum health was not sufficiently clear.
- The available budget appears generous, allowing the purchase of many presented upgrades. It was not possible to determine whether this is intentional.

### Interface and Usability

- The Call Sheet contains many visual elements, making functional information harder to distinguish from decorative elements.
- The tutorial appears to rely too heavily on the manual to explain some systems.
- The ESC menu uses white text on a gray background, which appears to provide insufficient contrast.
- The camera occasionally appears to clip into or move too close to scenery, and it was mistaken for an enemy during gameplay.
- Trap setup time is not sufficiently apparent, although the behavior seems to be part of the intended mechanic.

## Positive Aspects

- The dash feels responsive and satisfying to use.
- The movie-production theme gives the game a distinctive identity.
- Survival missions in enclosed environments create intense and engaging combat encounters.
- The Galleria Shotgun provides a satisfying sense of impact and effectiveness.
- The weapon and upgrade systems encourage experimentation.
- Combat has enjoyable moments despite the observed clarity issues.

## Testing Limitations

- **Test date:** October 16, 2026.
- **Game build:** Version 7, available since October 13, 2026.
- **Testing approach:** Exploratory playtesting based on my experience as a long-time gamer, without a predefined test script or formal test cases.
- **Reproduction steps:** Included only when the behavior could be described clearly using the final executable, without access to source code or the development environment.
- **Root causes:** Not investigated or confirmed. Findings describe observed behavior and player-facing impact rather than presumed technical causes.
- **Build verification:** Findings were not independently retested against subsequent builds.
- **Performance:** No crashes, performance drops, or other performance issues were observed or reported during the session.
- **Meta-progression:** No noticeable meta-progression system was encountered during testing. Its presence or absence was not independently verified.

The absence of a reported issue does not establish that the corresponding system is free of defects.

## Repository Structure

- `README.md` — project overview in English.
- `README.pt-BR.md` — project overview in Brazilian Portuguese.
- `bug-reports.md` — bug reports and observations in English.
- `bug-reports.pt-BR.md` — bug reports and observations in Brazilian Portuguese.

## Feedback and Corrections

Feedback from the developers is welcome. If any finding is inaccurate, has already been addressed, or requires additional context, I am open to reviewing and correcting the documentation.

If the developers have concerns about the content of this repository, they may contact me to discuss possible corrections or the removal of specific material.

This repository may be updated based on developer feedback regarding the findings submitted through Play2Review.

## Conclusion

The playtest identified opportunities for improvement in control consistency, attack clarity, enemy differentiation, communication of gameplay mechanics, and interface visual hierarchy.

The game also demonstrated positive qualities, particularly in dash responsiveness, thematic identity, and the combat experience provided by certain weapons.

These reports represent observations from a single exploratory playtest and should be interpreted within the limitations described in this document.
