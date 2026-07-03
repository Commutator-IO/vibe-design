---
name: build-sprint
description: >
  Orchestrate a five-day build sprint that ends in working software, adapted from Jake Knapp's Sprint (Google Ventures).
  Use when the user wants to run a design sprint, build an MVP or prototype in a week, "solve a big problem in 5 days",
  de-risk a product idea before building, or asks where to start / what day they're on in a build sprint.
  Routes to the per-day skills: set-the-stage, monday-map, tuesday-sketch, wednesday-decide, thursday-build, friday-test.
---

# Build Sprint (5-day) — orchestrator

Guide the user through a five-day sprint that produces real, tested software. The classic sprint fakes the prototype; here Thursday builds a thin but genuinely working version, because Claude can. Keep the discipline that makes sprints work: a narrow target, timeboxing, a Decider, sketch-before-build, and testing with five users.

## How to use this skill

Establish where the user is, then hand off to the matching day skill. Do exactly one day at a time — never race ahead.

| Stage | Skill to use | Output of the stage |
|-------|-------------|---------------------|
| Before Day 1 | `set-the-stage` | Challenge, Decider, roles, calendar, tools, 5 users being recruited |
| Monday | `monday-map` | Long-term goal, sprint questions, journey map, one narrow target |
| Tuesday | `tuesday-sketch` | Prior-art demos + 3 distinct solution sketches |
| Wednesday | `wednesday-decide` | Chosen solution + storyboard turned into a build plan |
| Thursday | `thursday-build` | Thin working prototype + finished interview script |
| Friday | `friday-test` | 5 interviews, patterns, decided next step |

## Principles to enforce every day

- **Narrow, risky target.** The value of the week scales with how focused the target is. Refuse to let scope widen.
- **No building before Thursday.** Opening the editor early feels productive and wrecks the week. Sketch and decide first.
- **Work alone together.** Don't average ideas in a group brainstorm. Develop full, competing solutions, then compare. Run Claude as several distinct "minds," not one blended answer.
- **Concrete beats abstract.** Turn ideas into sketches, storyboards, and specs that can be critiqued.
- **The Decider decides.** Structured voting to converge; the Decider makes binding calls so they stick.
- **Goldilocks quality.** Build only enough to answer Friday's questions. The prototype is disposable.
- **Timebox.** Keep each activity boxed. Running behind is fine; abandoning the structure is not.

## Getting started

If the user hasn't set up yet, start with `set-the-stage`. If they name a day, jump to that day's skill. At the start of each day, restate the target and the sprint questions so everything stays pointed at the same goal. At the end of each day, confirm the day's checklist is complete before moving on.
