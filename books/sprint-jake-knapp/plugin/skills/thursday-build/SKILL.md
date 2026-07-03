---
name: thursday-build
description: >
  Run Thursday of a build sprint — build the real, thin prototype from the build plan with Claude, assign build roles,
  stitch the pieces, do a trial run, and freeze. Use when the user is on day 4 of a sprint, is ready to build/code the
  prototype, or needs to turn a storyboard/spec into working software in a day.
---

# Thursday — Build it for real

The classic sprint fakes the prototype; here you build a real, thin version because Claude makes it possible in a day. The mindset is identical: build just enough to learn, and treat it as disposable.

## Prototype mindset
- You can prototype anything — scope it, don't fake the parts that matter for the test.
- Prototypes are disposable — don't fall in love with the code.
- Build just enough to learn, but no more.
- **Goldilocks quality** — real enough to earn honest reactions; not one line more polished than that.

## Pick the right tools
Use rough, fast, flexible tools, not the production stack. Let Claude scaffold aggressively and generate whole components; the human steers and stitches. Give Claude one focused task at a time — a screen, a flow, a fix — never "build the whole app."

## Divide and conquer (map roles onto working with Claude)
- **Maker** — prompts Claude to build each component; iterates.
- **Stitcher** — keeps the pieces coherent: one voice, one design, one data flow.
- **Writer** — real microcopy; fake data that reads as real.
- **Asset Collector** — logos, images, sample records so it doesn't look empty.
- **Interviewer** — steps back to finish Friday's script and confirm users.

Break the storyboard into scenes and build scene by scene against the Wednesday build plan.

## Stitch, trial-run, finish
- **Stitch** — the Stitcher checks quality and that the pieces make sense as one product.
- **Trial run by ~3 p.m.** — walk the whole prototype as a user; fix what breaks; the Interviewer and Decider watch and sign off.
- **Freeze** — stop building, load test data, confirm it survives a full run unaided.

_Prompts to offer:_
- "Scaffold [stack] for this build plan: project, routing, component skeleton for these screens: [list]."
- "Build [screen/flow] to match frame [n]. Use this fake data: [data]. It must survive a full click-through unaided."
- "Review the whole prototype for coherence and dead ends; list anything that breaks a full run-through, worst first."

## Prepare Friday in parallel
Interviewer finishes the five-act script, confirms all five users by phone, prepares incentives; a second person owns recording setup.

## Exit checklist
Rough tools chosen · roles assigned · prototype built scene by scene · stitched coherent · trial run done + Decider signed off · test data loaded + frozen · interview script done + 5 users confirmed. Then move to `friday-test`.
