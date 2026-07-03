---
name: example-skill
description: >
  One sentence on what this skill does, then the trigger phrases a user would say to invoke it.
  Use when the user wants to [do X], asks about [topic], or says things like "[phrase 1]", "[phrase 2]".
  Write in third person; pack in concrete trigger words — this is what routes the user to the skill.
---

# Example Skill

Write the body as instructions **for Claude**, not documentation for the user. Use verb-first, imperative sentences ("Draw the map," not "You should draw the map").

## Structure that works

State the goal of this step, then the ordered actions to take. Keep the core SKILL.md under ~500 words; push long reference material into a `references/` subfolder and point to it.

1. **First move** — what to do and why it matters.
2. **Second move** — the technique from the book, translated into action.
3. **Decision point** — what the user (or the Decider) must choose before moving on.

## Prompts to offer

Give the user paste-ready prompts where useful:

_Prompt to offer:_ "Do [specific task] given [inputs]. Output [format]."

## Exit checklist

End every skill with a short checklist so the user knows the step is done, and name the next skill to hand off to.
