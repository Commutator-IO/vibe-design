---
name: build-in-cycles
description: >
  Execute a six-week bet, adapted from Shape Up (Part 3). Use when a team is building a bet and needs to organize
  the work into scopes, track progress with hill charts, get a first slice done, cut scope, or decide when to ship.
  Triggers: "map the scopes", "hill chart", "we're building", "scope hammering", "when do we stop", "is it done".
---

# Build in Cycles

Turn a bet into shipped work over six weeks. The team owns the whole problem and discovers the tasks by building — nobody hands them a checklist.

## Hand over responsibility
Assign the **project, not tasks**. Give the team the pitch and let them figure out the work. "Done" means **deployed**, not "handed off to QA."

## Get one piece done first
Don't start with all the design or all the back-end. **Integrate one slice** end-to-end early — a real, working piece that touches UI and code together. This proves the approach and builds momentum. Use **affordances before pixel-perfect screens**, and **program just enough for the next step**. Start in the middle, not at setup.

## Map the scopes
Organize the project **by structure, not by person**. A **scope** is a slice of the project that can be finished and integrated independently — it becomes the language of the project ("drafts", "notifications"). Discover scopes by building; they're right when each is a meaningful, finishable part.
- **Layer cake** — thin, even UI + back-end: bundle design and code in one scope (good default for information-system apps).
- **Iceberg** — much more back-end than UI (or vice versa): factor the UI out as its own scope and split the complex side into finishable stages.
- **Chowder** — a short list for loose tasks that don't fit a scope. Stay skeptical: if it grows past three to five items, there's a scope hiding in there.
- Mark **nice-to-haves with `~`** so must-haves stay visible and separable.

## Show progress with hill charts
Work is like a **hill**: uphill is *figuring it out* (uncertainty), downhill is *execution* (known work). Plot each scope as a dot on the hill instead of a percentage. This reveals stuck work a "% done" bar hides — a scope parked uphill for days is a signal, not a status. Nobody has to say "I don't know"; the chart shows it. Use it to prompt refactoring scopes and to solve in the right sequence (tackle the scariest unknowns first).

## Decide when to stop
- **Compare to baseline**, not to an ideal. The question isn't "is it perfect" but "is this better than what customers have today, within the appetite?"
- **Limits motivate trade-offs.** The deadline makes the team make good cuts.
- **Scope hammering** — as the deadline nears, aggressively cut down to the must-haves. **Cutting scope isn't lowering quality** — it's choosing what matters. QA is for the edges, late.

## Exit checklist
Responsibility handed over · one slice integrated early · scopes mapped (layer cake / iceberg / chowder, `~` nice-to-haves) · progress tracked on a hill chart · scope hammered to fit · shipped by comparing to baseline. Then `cool-down`.
