# Shape Up Cycles

**Shaping, betting, and shipping work in six-week cycles**

*A playbook adapted from **Shape Up: Stop Running in Circles and Ship Work that Matters** by Ryan Singer (Basecamp).*

---

## Why this playbook

Most teams get stuck two ways: projects that drag on with no end, and backlogs that grow faster than anyone can clear them. Shape Up fixes both by fixing *time* and flexing *scope*. Work is shaped to the right level of detail, bet on for a six-week cycle, and built by a small team that owns the whole problem. Nothing is estimated; everything has an appetite.

It's the natural companion to the 5-Day Build Sprint. Use a sprint to de-risk a raw idea fast; then shape the winner and bet it into a cycle to build it for real.

## The rhythm

| Phase | Length | What happens |
|-------|--------|--------------|
| **Shape** | ongoing, closed-door | Turn raw ideas into bettable pitches |
| **Bet** | during cool-down | The betting table picks a few bets for the next cycle — no backlog |
| **Build** | 6 weeks | A small team ships the bet: scopes, hill charts, scope hammering |
| **Cool-down** | 2 weeks | Fix bugs, explore, rest, shape the next round |

## The core principles

- **Fixed time, variable scope.** Six weeks is the constant; scope is the shock absorber. This is what makes shipping reliable.
- **Appetite, not estimate.** Decide how much time an idea is *worth*, then shape a solution to fit — never estimate a fixed spec.
- **The right level of abstraction.** Wireframes are too concrete (they over-specify and steal the team's room to solve); words are too abstract (they hide the hard parts). Shape in between: **rough, solved, bounded.**
- **Teams are responsible.** Hand over the whole problem, not a task list. The team discovers the tasks by building.
- **Bets, not backlogs.** Un-bet ideas are dropped, not queued. Important ones come back on their own.

---

## Phase 1 — Shape a pitch

Shaping is closed-door work done before betting. Keep it rough and fast.

**Set the appetite.** How much is this worth — a **Small Batch** (one to two weeks of a team) or a **Big Batch** (a full six-week cycle)? The appetite constrains the solution.

**Narrow the problem.** Find the specific pain and a concrete use case. Beware grab-bags like "redo the calendar."

**Find the elements.** Rough out the solution without designing screens:

- **Breadboarding** — like a circuit diagram: *places*, the *affordances* on each, and *connection lines* between them.
- **Fat-marker sketches** — deliberately low-fidelity, so nobody over-invests in details the team should decide.

**De-risk.** Hunt **rabbit holes** (hidden complexity, unknowns, interdependencies) and patch them — decide, cut, or spike, and check with technical experts. Declare **no-gos** to keep the work inside the appetite.

**Write the pitch** — five ingredients:

1. **Problem** — the raw idea and the specific pain.
2. **Appetite** — Small or Big Batch.
3. **Solution** — the shaped elements, with annotated breadboards / fat-marker sketches so people can see it.
4. **Rabbit holes** — details worth flagging.
5. **No-gos** — what's explicitly excluded.

> With Claude: describe the raw idea and appetite, and ask it to draft a breadboard (places / affordances / connections), flag likely rabbit holes, and write the pitch in the five-ingredient format.

---

## Phase 2 — Bet the cycle

Betting happens during cool-down, among people who can commit. It's short and high-level.

**No backlogs.** Don't maintain a master to-do of everything. Un-bet pitches aren't scheduled; if an idea matters, it comes back.

**What a bet means.** The team gets **uninterrupted time** — a full, protected cycle. In return, the work ships within the cycle. The **circuit breaker:** if it doesn't ship in six weeks, it stops by default. No automatic extension.

**Choose the bets.** First read where the product is (R&D / production / cleanup mode). Then run each pitch through five questions:

1. Does the problem matter?
2. Is the appetite right?
3. Is the solution attractive?
4. Is this the right time?
5. Are the right people available?

Pick a small number of bets to fill the available teams (typically one designer + one or two programmers each). **Post a kick-off message** per bet: pitch, team, appetite, dates.

---

## Phase 3 — Build in cycles

**Hand over responsibility.** Assign the project, not tasks. "Done" means **deployed.**

**Get one piece done.** Integrate one real end-to-end slice early — UI and code together — to prove the approach. Affordances before pixel-perfect screens; program just enough for the next step; start in the middle.

**Map the scopes.** Organize by structure, not by person. A **scope** is a finishable, integrate-able slice that becomes the language of the project.

- **Layer cake** — thin, even UI + back-end: one combined scope (good default).
- **Iceberg** — lopsided back-end/UI: factor the UI out, split the heavy side into finishable stages.
- **Chowder** — a short list of loose tasks; if it grows past three to five items, a scope is hiding there.
- Mark **nice-to-haves with `~`** so must-haves stay separable.

**Show progress with hill charts.** Every scope is a dot on a hill: uphill is *figuring it out*, downhill is *execution*. This surfaces stuck work that a percentage bar hides. Solve the scariest unknowns first.

**Decide when to stop.**

- **Compare to baseline**, not to an ideal: is this better than what customers have today, within the appetite?
- **Scope hammering** — near the deadline, cut aggressively to the must-haves. **Cutting scope isn't lowering quality**; it's choosing what matters. QA the edges late.

---

## Phase 4 — Cool-down

Two weeks between cycles, with no scheduled project work.

- **Let the storm pass** — rest and tie off loose ends. Protect the time.
- **Fix bugs** — bugs are normal life; most wait for cool-down, only true fires interrupt a cycle.
- **Explore** — spike ideas and clean up without a bet's pressure.
- **Shape the next round** — refine pitches so the next betting table has good options. Remember: raw feedback must be *shaped* before it can be bet on.

Then the betting table picks the next bets, and the cycle begins again.

---

## The whole loop, in one line

Shape ideas into pitches → bet a few into a six-week cycle → build with scopes and hill charts, hammering scope to fit → cool down, fix, and shape the next round → repeat.

---

*Adapted from Shape Up by Ryan Singer. Method © Basecamp; the full book is free at basecamp.com/shapeup.*
