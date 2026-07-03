# Sprint → Build Sprint

Adapted from **_Sprint: How to Solve Big Problems and Test New Ideas in Just Five Days_** by Jake Knapp, John Zeratsky & Braden Kowitz.

The classic design sprint spends four days de-risking an idea and fakes a prototype on Thursday to test on Friday. This adaptation keeps the discipline — a narrow target, timeboxing, a Decider, sketch-before-build, five-user testing — but because Claude can build real software in a day, **Thursday builds a thin-but-working prototype instead of a façade.**

## Contents

```
sprint-jake-knapp/
├── plugin/        # Installable Claude plugin — 7 skills, one per sprint phase
└── playbook/      # Human-readable guide (Markdown + Word)
```

## Plugin: `build-sprint`

| Skill | Runs when |
|-------|-----------|
| `build-sprint` | Orchestrator — routes you to the right day, enforces the principles |
| `set-the-stage` | Before Day 1 — challenge, Decider, roles, calendar, tools, recruiting |
| `monday-map` | Monday — goal, sprint questions, journey map, one narrow target |
| `tuesday-sketch` | Tuesday — Lightning Demos + Four-Step Sketch, 3 competing solutions |
| `wednesday-decide` | Wednesday — sticky decision + storyboard turned into a build plan |
| `thursday-build` | Thursday — build the real prototype with Claude, stitch, trial run, freeze |
| `friday-test` | Friday — five-act interviews, synthesize, decide next step |

**Install:** `/plugin install build-sprint@vibe-design`, or open a packaged `.plugin` file in Cowork.

**Use:** say *"let's run a build sprint"* to start with the orchestrator, or name a day (*"I'm on Wednesday of my sprint"*) to jump straight in.

## Playbook

- [`The-5-Day-Build-Sprint.md`](playbook/The-5-Day-Build-Sprint.md) — full day-by-day guide with prompts and checklists

## Credit

Method © Jake Knapp, John Zeratsky & Braden Kowitz. This skillset restructures their framework for building software with Claude.
