# Playtest Report — Stuck On Set

Exploratory gameplay testing and feedback for
[Stuck On Set](https://driftingsignal.itch.io/stuck-on-set).

## Project Overview

**Game:** Stuck On Set  
**Developer / studio:** Drifting Signal  
**Game page:** https://driftingsignal.itch.io/stuck-on-set  
**Test date:** Not recorded  
**Build version:** Not recorded  
**Testing method:** Exploratory manual gameplay testing  
**Primary input device:** Keyboard and mouse  
**Additional input tested:** Controller / gamepad  

This repository documents observations made during a playtesting
session of Stuck On Set, a top-down action roguelite built around
a movie-production theme.

The purpose of this report is to document gameplay issues,
control inconsistencies, usability concerns, combat readability,
and opportunities to improve the player experience.

The findings are based on my own gameplay session. They are not
a comprehensive quality assurance assessment of the game.

## Testing Scope

The session covered the following areas:

- Tutorial and onboarding
- Keyboard and controller inputs
- Character movement and dashing
- Combat and enemy behavior
- Boss encounter
- Weapons and upgrades
- Traps and combat mechanics
- In-game menus and interface
- Progression and upgrade economy
- Environmental collisions
- General gameplay readability

Testing was exploratory rather than scripted. I played the game,
observed its behavior, and took notes when I encountered issues
or mechanics that warranted further investigation.

## Project Context

This project was independently created for QA practice through the Play2Review website. The goal was to document gameplay observations, identify potential bugs and usability issues, and practice writing structured QA reports based on hands-on testing.

The playtest was conducted on the final executable of *Stuck On Set*, Version 7, available since October 13, 2026. No source code or development environment was used.

This repository is an independent portfolio project and is not an official QA report or an endorsement by the game's developers.

This repository may be updated based on feedback from the game developer regarding the findings submitted through Play2Review.

## Summary of Findings

The session revealed issues and opportunities across several
areas:

- Keyboard movement appeared inconsistent, particularly when
  combining horizontal and vertical inputs.
- Controller menu navigation was not functional during testing.
- The tutorial provided incorrect information about the dash
  controls.
- Some enemy attacks were difficult to anticipate, and several
  enemy types were difficult to distinguish.
- Some enemies appeared to spawn partially inside the ground
  and become stuck.
- Some wall collisions appeared incorrect.
- The "Call Sheet" and other menus felt visually cluttered.
- Certain weapons and upgrades felt less effective or less
  controllable than others.
- Some gameplay mechanics, including trap setup time and
  Genre progression, could be communicated more clearly.

These findings include both observed technical behavior and
subjective usability or design feedback. Not every observation
has been confirmed as a defect.

## Positive Observations

Several elements showed promise:

- **Dashing:** The dash felt fluid and responsive.
- **Galleria Shotgun:** The weapon was straightforward and
  satisfying to use, although it may be stronger than intended.
- **Survival encounters:** The enclosed survival mission created
  an intense and engaging situation.
- **Roguelite structure:** Weapons, Roles, Scripts, and Genres
  suggest opportunities for varied builds and replayability.
- **Theme:** The movie-set concept provides a distinctive
  foundation for the game's identity.

These strengths are worth preserving while improving controls,
readability, and overall polish.

## Main Areas for Improvement

### 1. Controls and Input

Keyboard movement appeared to favor horizontal movement over
vertical movement, making diagonal movement difficult.

Controller menu navigation was not functional during testing.
The tutorial also incorrectly described the dash inputs:
RT/R2 fired the weapon, while RB/R1 performed the dash.

### 2. Combat Readability

Some enemies were difficult to distinguish from one another.
Several attacks lacked clear telegraphs, and incoming damage
sometimes felt unpredictable.

The boss's large "IMMUNE" text and shield initially made its
intended interaction unclear.

### 3. Interface and Tutorial

The Call Sheet and other menus felt cluttered. Although this
may support the movie-production aesthetic, gameplay-relevant
information could be separated more clearly from decoration.

The tutorial relied too heavily on the written manual to explain
important gameplay concepts.

### 4. Collision and Enemy Behavior

Some wall collisions appeared incorrect, and some enemies
appeared to spawn partially inside the ground and become stuck.

The relevant footage should be reviewed before determining the
cause or scope of these behaviors.

### 5. Weapons and Progression

"Sentinel Spheres" encouraged dangerous proximity to enemies.
"Ol' Painless" felt unreliable at range because of its poor
accuracy. The double-small-trap upgrade also felt less
reliable than using a single trap.

Genre point acquisition and the trade-off involving maximum
health were not sufficiently clear during the session.

## Testing Limitations

- **Test date:** October 16, 2026.
- **Game build:** Version 7, available since October 13, 2026.
- **Testing approach:** Exploratory playtesting based on my experience as a long-time gamer, without a predefined test script or formal test cases.
- **Reproduction steps:** Included only when the behavior could be described clearly using the final executable, without access to source code or the development environment.
- **Root causes:** Not investigated or confirmed. Findings describe observed behavior and player-facing impact rather than presumed technical causes.
- **Build verification:** Findings were not independently retested against subsequent builds.
- **Performance:** No crashes, performance drops, or other performance issues were observed or reported during the session.
- **Meta-progression:** No noticeable meta-progression system was encountered during testing. Its presence or absence was not independently verified.

The findings represent observations from a single exploratory playtest of Version 7. Behaviors may be intentional design choices, known limitations, or defects; further investigation by the development team may be necessary to determine which applies.


## Conclusion

Stuck On Set has a promising foundation, particularly in its
dash mechanics, weapon feel, and intense survival encounters.

The most important areas to investigate are keyboard movement,
controller menu navigation, tutorial accuracy, combat
readability, and collision behavior.

The reports in this repository are intended to provide
actionable feedback while distinguishing observed behavior
from subjective impressions and unverified explanations.

No claims are made about the status of these issues in
subsequent builds.

## Feedback and Corrections

Feedback from the developer is welcome. If any findings are inaccurate, have already been addressed, or require additional context, I am open to reviewing and correcting the documentation.

For concerns regarding the content of this repository, the developer may contact me to discuss possible corrections or removal of specific material.
