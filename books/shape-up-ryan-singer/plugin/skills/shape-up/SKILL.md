---
name: shape-up
description: >
  Orchestrate product development in six-week cycles, adapted from Ryan Singer's Shape Up (Basecamp).
  Use when the user wants to run Shape Up, work in cycles, shape a project, run a betting table, plan a
  six-week bet, track build progress with hill charts, or asks "what should we work on next cycle" / "how do
  we stop projects dragging on". Routes to: shape-a-pitch, bet-the-cycle, build-in-cycles, cool-down.
---

# Shape Up — orchestrator

Guide the user through Basecamp's product development method: work is **shaped** at the right level of abstraction, **bet** on in six-week cycles, and **built** by small teams given full responsibility. Route to the matching stage skill and hold the line on the principles below.

## The cycle

| Stage | Skill | Output |
|-------|-------|--------|
| Shape (ongoing, closed-door) | `shape-a-pitch` | A written pitch: problem, appetite, solution, rabbit holes, no-gos |
| Bet (betting table) | `bet-the-cycle` | A few bets chosen for the next six weeks; kick-off message |
| Build (6 weeks) | `build-in-cycles` | Shipped work — scopes mapped, hill charts, scope-hammered |
| Cool-down (2 weeks) | `cool-down` | Bugs fixed, exploration, next pitches shaped |

## Principles to enforce every stage

- **Fixed time, variable scope.** The six weeks are fixed. Scope flexes. This is the shock absorber that makes shipping reliable.
- **Appetite, not estimate.** Decide how much time an idea is *worth* (the appetite), then design a solution to fit — never estimate a fixed spec.
- **Work at the right level of abstraction.** Wireframes are too concrete (they over-specify and remove the team's room to solve); words are too abstract (they hide the hard parts). Shape in between: rough, solved, and bounded.
- **Make teams responsible.** Hand over the whole problem, not a task list. The team discovers the tasks by building.
- **No backlogs.** Un-bet ideas are dropped, not queued. Genuinely important ones come back.
- **Bets are commitments with a circuit breaker.** A bet means uninterrupted time to finish within the cycle; if it doesn't ship, it stops by default rather than auto-extending.

## How to start

If the user has a raw idea, start with `shape-a-pitch`. If they have shaped pitches and need to choose, go to `bet-the-cycle`. If a bet is in flight, use `build-in-cycles`. Between cycles, use `cool-down`. At each stage, restate the appetite and the shaped boundaries so the work stays inside them.
