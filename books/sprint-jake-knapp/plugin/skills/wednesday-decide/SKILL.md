---
name: wednesday-decide
description: >
  Run Wednesday of a build sprint — the sticky decision (heat map, speed critique, straw poll, supervote) to choose the
  winning solution, then turn a storyboard into a concrete one-day build plan. Use when the user is on day 3 of a sprint,
  needs to decide between solution options, storyboard a prototype, or write a build spec for tomorrow.
---

# Wednesday — Decide & storyboard the build

Morning: choose among the competing solutions. Afternoon: turn the winner into a build plan Claude can execute tomorrow.

## Morning — the sticky decision
Converge fast without endless debate:
1. **Art museum** — lay all solution sketches in a row.
2. **Heat map** — silently mark every part worth liking; patterns emerge without talking.
3. **Speed critique** — 3 min per sketch; capture standout ideas and real objections.
4. **Straw poll** — each person picks one favorite.
5. **Supervote** — the Decider makes the binding choice. Build what the Decider picks.

**Rumble or all-in-one:** if two strong ideas conflict, keep both and build competing prototypes to test head-to-head Friday. If they combine cleanly, merge into one. For any quick group decision use a **Note-and-Vote**: write ideas privately → list → vote → Decider picks.

## Afternoon — storyboard = build spec
This is where a build sprint diverges from the classic sprint: the storyboard is the specification Claude builds from. Make it concrete enough that Thursday is execution, not invention.
1. **Draw a grid** — ~10–15 frames.
2. **Opening scene** — how the user first arrives (link, search, login).
3. **Fill each frame** — one screen/step per frame: what the user sees, what they do, what the system does. Reuse existing sketches; draw the rest. When in doubt, take the more ambitious risk.

Then translate the storyboard into a build plan: an ordered task list of screens/components, a minimal data model, and a clear **Goldilocks line** — what must genuinely work to answer Friday's questions vs. what can be stubbed.

_Prompt to offer:_ "Turn this 15-frame storyboard into a one-day build plan: ordered tasks, screens/components, minimal data model, and what's real vs. stubbed. Recommend a lightweight stack one person plus you can ship in a day."

**Facilitator tip:** don't drain the battery — defer big calls to the Decider, small ones to tomorrow, and don't let new abstract ideas sneak in. Build with what you have.

## Exit checklist
Heat map + critique done · Decider's supervote chosen the winner · rumble vs. all-in-one decided · storyboard drawn · build plan written · Goldilocks line set · Interviewer drafting Friday's script. Then move to `thursday-build`.
