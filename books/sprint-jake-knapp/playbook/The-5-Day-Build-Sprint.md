# The 5-Day Build Sprint

**Shipping working software with Claude in one week**

*A playbook adapted from Jake Knapp's Sprint (Google Ventures)*

Prepared for Michel · commutator.io

---

## Contents

1. [Why this playbook](#why-this-playbook)
2. [The skills worth stealing from Sprint](#the-skills-worth-stealing-from-sprint)
3. [Before you start: set the stage](#before-you-start-set-the-stage)
4. [Monday — Map & Target](#monday--map--target)
5. [Tuesday — Sketch: research & options](#tuesday--sketch-research--options)
6. [Wednesday — Decide & storyboard the build](#wednesday--decide--storyboard-the-build)
7. [Thursday — Build it for real](#thursday--build-it-for-real)
8. [Friday — Test & learn](#friday--test--learn)
9. [Appendix A — Claude prompt library](#appendix-a--claude-prompt-library)
10. [Appendix B — how sprints go wrong](#appendix-b--how-sprints-go-wrong)

---

## Why this playbook

The design sprint was built for a specific problem: teams spending months building something before finding out whether it was worth building. Jake Knapp's answer was to compress the riskiest thinking into five days and end the week with a realistic prototype tested on real people — before committing serious engineering.

You have an advantage Knapp's teams did not. With Claude, the prototype does not have to be a façade. In a single day you can produce genuinely working software, not a clickable illusion. So this playbook keeps the discipline that makes sprints work — the timeboxing, the Decider, sketching before building, testing with five users — and repoints Thursday from "fake it" to "build it for real."

> "Running a sprint is kind of like baking a cake: if you don't follow the recipe, you might end up with a disgusting mess." — *Sprint*

The rhythm below is the same one the book prescribes. Each day narrows the field: Monday you map the problem and pick one target, Tuesday you gather and sketch solutions, Wednesday you decide and storyboard, Thursday you build, and Friday you learn from real users.

| Day | Original Sprint | Your Build Sprint with Claude |
|-----|-----------------|-------------------------------|
| Monday | Map the problem, pick a target | Same — define the goal, risks, user flow; target the riskiest slice |
| Tuesday | Sketch competing solutions | Research prior art + sketch UX and architecture options with Claude |
| Wednesday | Decide and storyboard | Choose the approach; turn the storyboard into a build spec |
| Thursday | Build a fake prototype | Build the real thing with Claude — thin but working |
| Friday | Test with 5 customers | Same — five interviews, watch together, decide next step |

*This is a five-day commitment of roughly 35 hours — the same as the book. You will be home for dinner.*

---

## The skills worth stealing from Sprint

Before the day-by-day plan, here are the core techniques the book is really teaching — the transferable skills. Each maps onto a stage of your build week.

| Skill | What it means | Day |
|-------|---------------|-----|
| Start at the end | Agree on where you want to be in six months to a year, then work backward. Ambition first, then list every way it could fail as answerable questions. | Monday |
| Map before you build | Draw the customer's journey as a simple 5–15 step flowchart. It keeps everyone honest about what you're actually building and where the risk lives. | Monday |
| Ask the experts, then choose one target | Interview whoever knows the problem, capture opportunities as "How Might We" notes, then have the Decider pick one target customer and one moment on the map. Focus beats breadth. | Monday |
| Remix and improve | Great solutions are built from existing ones. Survey what already works — inside and outside your field — before inventing anything. | Tuesday |
| Work alone together | Group brainstorms produce mush. Give each mind (including Claude, run as parallel options) private time to develop a full solution, then compare. | Tuesday |
| Concrete beats abstract | Turn ideas into something you can look at and critique. A rough sketch settles arguments that endless discussion cannot. | Tuesday / Wednesday |
| Decide without draining the battery | Every decision costs energy. Use structured voting (heat map, straw poll, supervote) to converge fast, and let the Decider make the binding call. | Wednesday |
| Storyboard the whole thing first | Plan every step of the prototype on a grid before building, so Thursday is execution, not invention. | Wednesday |
| Prototype mindset & Goldilocks quality | Build just enough to learn — no more. It must feel real enough to earn honest reactions, but it is disposable. | Thursday |
| Five users, watched together | Five interviews reveal about 85% of the problems. Do them in one day and have the whole team watch, so you draw conclusions together. | Friday |

---

## Before you start: set the stage

Do this in the days before Monday. It is the single biggest predictor of whether the week works.

### Pick the right challenge

- **Use a sprint when the stakes are high, time is short, or you're stuck.** A build sprint is for the thing you keep meaning to start but never de-risk.
- Good candidates: a new product idea, a feature you're unsure users want, a workflow you want to automate, a prototype to show a stakeholder or investor.

### Name a Decider

Without a Decider, decisions don't stick. This is the person who can say "we're building this one." If that's you, own it. If it's someone else, get their buy-in for the week or have them delegate a stand-in who can commit.

### Assemble your team

A classic sprint is seven people or fewer with diverse skills. Yours can be much smaller — even just you and Claude — but the roles still exist. Assign them, even to yourself:

| Role | What they do in a Claude build sprint |
|------|---------------------------------------|
| Decider | Makes the binding call on target and approach. Reviews the prototype before Friday. |
| Facilitator | Runs the clock, keeps each day timeboxed, prevents scope creep. |
| Maker / Stitcher | Works with Claude to build and to keep the pieces coherent. |
| Interviewer | Runs Friday's five interviews. Writes the script Thursday. |
| Claude | Your on-demand expert, researcher, sketch generator, and builder. Give it one clear job at a time. |

### Time and space

- **Block five days**, roughly 10 a.m.–5 p.m. Mon–Thu and 9 a.m.–5 p.m. Fri. Protect the calendar.
- **No distractions.** Devices away during focused blocks. The book is strict about this for a reason — momentum is fragile.
- **Timebox everything.** A visible timer creates focus and urgency. Run behind gracefully; don't abandon the box.
- **One capture surface.** A whiteboard or a single shared doc where the goal, questions, map, and decisions live all week.

### Your build supplies

The book's markers and sticky notes become their software equivalents. Set these up before Monday so Thursday isn't spent on plumbing:

- A **fresh repository** and a place to run it (local dev environment or a sandbox).
- **Rough, fast, flexible tools** — a scaffolding framework, component library, and a deploy target that takes one command. Don't reach for your heavyweight production stack.
- **Test data and accounts** ready to go, so the prototype has something to show.
- **Five recruited users** for Friday. Start recruiting on day one; it takes an hour or two a day.

---

## Monday — Map & Target

Monday builds a shared picture of the problem and forces one decision: what exactly are you building this week? Resist the urge to open an editor. Today is thinking.

### Morning — set direction

**1. Set a long-term goal (get optimistic)**

Ask: why are we doing this? Where do we want to be in six months or a year? Write one sentence and post it where you can see it all week.

**2. List sprint questions (get pessimistic)**

Now flip it: how could this fail? Turn each fear into a question you could answer this week. "Will users trust it with their data?" "Can we make onboarding under two minutes?" These become your test criteria on Friday.

**3. Make a map**

Draw a simple flowchart of how a user gets from first contact to your goal. Actors on the left, the finished goal on the right, five to fifteen steps in between. Keep it crude. This is the skeleton of what you'll build.

> **Claude prompt:** "Here's my product idea and long-term goal. Act as a product strategist. Draw a simple 5–15 step user journey map from first contact to the goal, and list the top 5 ways this could fail as questions we could test this week."

### Afternoon — narrow to one target

**4. Ask the experts**

Interview anyone who understands the problem — teammates, a domain expert, a real user, or Claude standing in for research. Fifteen to thirty minutes each, like a reporter. Update your goal, questions, and map as you learn.

**5. "How Might We" notes**

As you listen, reframe every problem as an opportunity starting with "How might we…" One idea per note. Then cluster them, and vote for the ones that matter most.

**6. Pick a target**

The Decider circles one target customer and one target moment on the map — the riskiest, most valuable slice. Everything for the rest of the week aims at this one point. This single decision is the whole point of Monday.

> The narrower and riskier the target, the more the week is worth. Don't build the easy part.

### Monday checklist

- [ ] Long-term goal written and posted
- [ ] Sprint questions listed (your Friday test criteria)
- [ ] User journey map drawn (5–15 steps)
- [ ] Experts interviewed; map updated
- [ ] How Might We notes captured and voted
- [ ] One target customer + one target moment chosen by the Decider
- [ ] Recruiting for Friday's 5 users started

---

## Tuesday — Sketch: research & options

Monday gave you a target. Tuesday fills it with possible solutions. In the morning you steal the best ideas that already exist; in the afternoon everyone (including Claude, run as parallel drafts) sketches a detailed solution alone.

### Morning — Lightning Demos

Look at great solutions from a range of products — competitors, adjacent industries, your own past attempts. Three minutes each. For every one, capture the single good idea as a quick sketch or note on the board. You are remixing, not copying.

> **Claude prompt:** "For [target moment], show me how 6 well-designed products solve a similar problem — inside and outside my industry. For each, name the one idea worth stealing. Then list the technical approaches (libraries, patterns, APIs) that could implement each."

### Afternoon — the Four-Step Sketch

The book's core move: work alone together. Don't brainstorm as a group — it flattens ideas. Each person develops a complete solution privately, then you compare tomorrow.

1. **Notes** (20 min) — walk the room and your board, gather the goal, questions, and best demo ideas into notes.
2. **Ideas** (20 min) — privately jot rough ideas; circle the most promising.
3. **Crazy 8s** (8 min) — fold a sheet into eight frames, sketch eight fast variations of your best idea, one minute each. This forces you past the obvious first answer.
4. **Solution sketch** (30–90 min) — a three-panel storyboard of your best idea. Self-explanatory, anonymous, ugly is fine, words matter, give it a catchy title.

For a build sprint, run Claude as several of these "minds." Ask it for three genuinely different solution sketches — different UX, different architecture — rather than one averaged answer.

> **Claude prompt:** "Give me three distinct, complete solution sketches for [target moment]. Make them meaningfully different in UX and technical approach — not variations of one idea. For each: a catchy title, a 3-step user flow, the key screens, and the rough architecture. Ugly and concrete beats polished and vague."

### Also today: keep recruiting

Recruiting five good users is the sleeper task of the week. Post a screener, offer a small incentive, and confirm people by email and phone. An hour or two, every day.

### Tuesday checklist

- [ ] Lightning Demos done; best ideas captured on the board
- [ ] Decided how to split the target (divide or swarm)
- [ ] Four-Step Sketch completed by each participant
- [ ] 3 distinct solution sketches from Claude, concrete and titled
- [ ] Solution sketches saved for tomorrow's decision
- [ ] Friday users being confirmed

---

## Wednesday — Decide & storyboard the build

You have a stack of competing solutions. Wednesday morning you choose; Wednesday afternoon you turn the winner into a step-by-step plan Claude can build from tomorrow.

### Morning — the sticky decision

The book's five-step method converges a group fast without endless debate. Even solo, the structure keeps you honest:

1. **Art museum** — lay all solution sketches out in a row.
2. **Heat map** — silently mark every part you like. Patterns emerge without anyone talking.
3. **Speed critique** — three minutes per sketch; capture standout ideas and real objections.
4. **Straw poll** — each person picks one favorite.
5. **Supervote** — the Decider makes the binding choice. You build what the Decider picks.

**Rumble or all-in-one?**

If two strong ideas conflict, keep both and build competing prototypes (a "Rumble") to test head-to-head Friday. If they combine cleanly, merge into one. When you need any quick group decision, use a Note-and-Vote: write ideas privately, list them, vote, Decider picks.

### Afternoon — storyboard = build spec

This is where a build sprint diverges most usefully from the book. Your storyboard isn't just a test script — it's the specification Claude builds from. Make it concrete enough that Thursday is execution, not invention.

1. **Draw a grid** — about 10–15 frames.
2. **Choose an opening scene** — how the user first arrives (a link, a search, a login).
3. **Fill each frame** — one screen or step per frame: what the user sees, what they do, what the system does. Move existing sketches in where they fit; draw the rest. Include just enough detail to build. When in doubt, take the more ambitious risk.

Then translate the storyboard into a build plan: a short, ordered task list of components and screens, the data model, and which parts are real versus faked. Decide your Goldilocks line — what must genuinely work to answer Friday's questions, and what can be stubbed.

> **Claude prompt:** "Here's my storyboard (15 frames). Turn it into a build plan for a one-day prototype: an ordered task list, the screens and components, a minimal data model, and a clear line between what must really work and what we can stub. Recommend a lightweight stack that one person plus you can ship in a day."

> **Facilitator tip:** don't drain the battery. Defer big calls to the Decider, small ones to tomorrow, and don't let shiny new abstract ideas sneak in. Build with what you have.

### Wednesday checklist

- [ ] Solutions reviewed via heat map + speed critique
- [ ] Decider's supervote chosen the winning solution(s)
- [ ] Rumble vs. all-in-one decided
- [ ] Storyboard drawn (10–15 frames, concrete)
- [ ] Storyboard translated into an ordered build plan with Claude
- [ ] Goldilocks line set: what's real vs. stubbed
- [ ] Interviewer starts drafting Friday's script

---

## Thursday — Build it for real

The book fakes the prototype in a day. You'll build a real, thin version — because Claude lets you. The mindset is identical: build just enough to learn, and treat it as disposable.

### Adopt the prototype mindset

- **You can prototype anything.** Scope, don't compromise the illusion of realness where it matters.
- **Prototypes are disposable.** Don't fall in love with the code. If Friday says pivot, you throw it away — cheaply.
- **Build just enough to learn, but no more.** Every hour on something Friday won't test is wasted.
- **Goldilocks quality.** Real enough to earn honest reactions; not a line more polished than that.

### Pick the right tools

Don't use your everyday production tooling — it's optimized for quality and durability, which fights speed. Use tools that are rough, fast, and flexible. Let Claude scaffold aggressively and generate whole components; you steer and stitch.

### Divide and conquer

Assign the book's build roles, mapping them onto working with Claude:

| Role | In your Claude build |
|------|----------------------|
| Maker | Prompts Claude to build each component; iterates on output. |
| Stitcher | Keeps the pieces coherent — one voice, one design, one data flow. |
| Writer | Real microcopy and content; fake data that reads as real. |
| Asset Collector | Logos, images, sample records so it doesn't look empty. |
| Interviewer | Steps back from building to finish Friday's script and confirm users. |

Break the storyboard into scenes and build scene by scene. Give Claude one focused task at a time — a screen, a flow, a fix — rather than "build the whole app."

### Stitch, trial-run, finish

- **Stitch it together.** When work is split, it's easy to lose the whole. The Stitcher checks quality and that the pieces make sense as one product.
- **Do a trial run by 3 p.m.** Walk the entire prototype as a user. Fix what breaks. Make sure the Interviewer and Decider see it and sign off.
- **Finish and freeze.** Stop building. Load your test data. Make sure it survives a full run without you nursing it.

### Prepare Friday in parallel

The Interviewer finishes the five-act script (below), confirms all five users by phone, and prepares incentives. A second person owns the recording setup.

### Thursday checklist

- [ ] Rough/fast/flexible tools chosen — not the production stack
- [ ] Roles assigned (Maker, Stitcher, Writer, Assets, Interviewer)
- [ ] Prototype built scene by scene with Claude
- [ ] Pieces stitched into one coherent product
- [ ] Trial run completed by ~3 p.m.; Decider signed off
- [ ] Test data loaded; prototype frozen
- [ ] Friday's interview script done; 5 users confirmed

---

## Friday — Test & learn

The payoff. Five one-on-one interviews with real users, watched together by the whole team. By the fifth, the big patterns are unmistakable.

### Why five, and why together

- **Five is the magic number.** After five interviews, roughly 85% of problems have surfaced. Do all five in one day.
- **Watch together, learn together.** Don't disband the team. Stream the interview to a room where everyone takes notes on the same board — you'll draw better, shared conclusions.
- **There's a winner every time.** An efficient failure or a flawed success both tell you exactly what to do next.

### The five-act interview

1. **Friendly welcome** — put them at ease; you want candid feedback, and you're testing the product, not them.
2. **Context questions** — easy small talk, then ease into the topic to understand their world.
3. **Introduce the prototype** — remind them some things may not work, and to think aloud.
4. **Tasks and nudges** — give a task, then stay quiet. Watch them figure it out. Nudge gently; ask "what are you thinking?" — never lead.
5. **Debrief** — ask them to summarize; what worked, what confused them, how it compares. Thank them, give the incentive, show them out.

> **Claude prompt:** "Write a five-act interview script for testing [prototype] against these sprint questions: [list]. Include the welcome, context questions, 3 realistic tasks with neutral nudges, and debrief questions. Keep every question non-leading."

### Capture and learn

As the team watches, note reactions on a grid: one column per interview, one row per step of the flow. Use green for what worked and red for what failed. After the fifth interview, look for patterns across at least three users — those are real. Then, as a group:

- Compare what you saw against Monday's sprint questions. Which got answered?
- Decide the next step: ship it, fix and retest, pivot, or stop. Because you built thin and disposable, any of these is cheap.

> **Claude prompt:** "Here are my notes from 5 user interviews. Cluster the patterns that appeared in 3+ sessions, map each back to my sprint questions, and recommend a concrete next step with the reasoning."

### Friday checklist

- [ ] Interview room + recording/streaming set up (audio checked)
- [ ] Team watching together, capturing on a shared grid
- [ ] Five interviews completed in one day
- [ ] Patterns (3+ users) identified against sprint questions
- [ ] Next step decided: ship, iterate, pivot, or stop
- [ ] Prototype and learnings archived for the next sprint

---

## Appendix A — Claude prompt library

Paste-ready prompts for each stage. Replace bracketed text with your specifics, and always give Claude one clear job at a time.

| Day | Use | Prompt |
|-----|-----|--------|
| Mon | Map & questions | Act as a product strategist. Given [idea] and goal [goal], draw a 5–15 step user journey map and list the top 5 failure modes as testable questions. |
| Mon | Expert stand-in | Play a skeptical [domain] expert. Interview-style, tell me what usually goes wrong with [problem] and what users actually care about. |
| Tue | Lightning Demos | Show how 6 well-designed products solve [target moment], inside and outside my field. Name the one idea worth stealing from each and its technical approach. |
| Tue | Divergent sketches | Give 3 meaningfully different complete solution sketches for [target moment]: title, 3-step flow, key screens, rough architecture. Not variations of one idea. |
| Wed | Build spec | Turn this 15-frame storyboard into a one-day build plan: ordered tasks, screens/components, minimal data model, and what's real vs. stubbed. Recommend a lightweight stack. |
| Thu | Scaffold | Scaffold [stack] for this build plan. Set up the project, routing, and a component skeleton for these screens: [list]. Fast and rough over polished. |
| Thu | Build a scene | Build [screen/flow] to match frame [n] of the storyboard. Use this fake data: [data]. It must survive a full click-through unaided. |
| Thu | Stitch & smoke test | Review the whole prototype for coherence and dead ends. List anything that breaks a full run-through as a user, most severe first. |
| Fri | Interview script | Write a five-act interview script testing [prototype] against [sprint questions]: welcome, context, 3 tasks with neutral nudges, debrief. No leading questions. |
| Fri | Synthesize | Cluster patterns from these 5 interview notes that appear in 3+ sessions, map each to my sprint questions, and recommend a next step with reasoning. |

---

## Appendix B — how sprints go wrong

The book's hard-won warnings, translated to a build week:

- **No target, or a target that's too broad.** If you didn't force one narrow choice Monday, Thursday sprawls and Friday tests nothing clearly.
- **Building on Monday or Tuesday.** Opening the editor early feels productive and wrecks the week. Sketch and decide first.
- **Group brainstorming instead of working alone together.** You'll converge on the safe, average idea.
- **No Decider, or a Decider who won't decide.** Decisions won't stick and you'll re-litigate all week.
- **Over-building the prototype.** Polishing what Friday won't test is the most common time sink. Hold the Goldilocks line.
- **Skipping the real users.** The entire week exists to earn Friday's five interviews. Recruit from day one.

---

*Adapted from Sprint by Jake Knapp, John Zeratsky & Braden Kowitz. Method © the authors; this playbook restructures it for building software with Claude.*
