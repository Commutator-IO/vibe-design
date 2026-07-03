# Adding a new book skillset

This repo turns a book's method into (1) an installable Claude plugin and (2) a human-readable playbook. Every book is self-contained under `books/<book-slug>/`. Here's the whole loop.

## 1. Scaffold the folder

```bash
cp -R templates/book-template books/<book-slug>
```

Use a clear slug: `<topic-or-title>-<author>`, e.g. `sprint-jake-knapp`, `deep-work-cal-newport`. Kebab-case, lowercase.

## 2. Distill the method into skills

The hardest and most valuable step. Read the book and pull out the *transferable techniques* — the moves the author is really teaching. Each becomes one skill under `plugin/skills/<skill-name>/SKILL.md`.

Guidelines:

- **One skill per phase or technique.** If the method is a sequence (days, steps, stages), make one skill per stage plus a short **orchestrator** skill that routes between them.
- **Write the body for Claude, not the reader.** Imperative, verb-first instructions ("Draw the map"), under ~500 words. Long reference material goes in a `references/` subfolder.
- **Nail the `description` frontmatter.** Third person, packed with the phrases a user would actually say. This is what makes the skill trigger at the right moment.
- **End each skill with an exit checklist** and a pointer to the next skill.

Delete the `example-skill` folder once you've added real ones.

## 3. Fill in the plugin manifest

Edit `plugin/.claude-plugin/plugin.json`:

- `name` — the plugin slug (kebab-case). This is what users type to install.
- `description` — what it does and when Claude should reach for it.
- `keywords` — searchable terms.

## 4. Write the playbook

`playbook/PLAYBOOK.md` is the human version — the same method as prose a person can read straight through, with paste-ready prompts and checklists. Keep it in Markdown so it renders cleanly on GitHub and stays diff-friendly.

## 5. Register in the marketplace

Add an entry to `.claude-plugin/marketplace.json`:

```json
{
  "name": "<plugin-slug>",
  "source": "./books/<book-slug>/plugin",
  "description": "…",
  "version": "0.1.0",
  "keywords": ["…"]
}
```

## 6. Update the library table

Add a row to the table in the root `README.md`.

## 7. Validate before committing

```bash
# JSON is well-formed
python3 -c "import json; json.load(open('.claude-plugin/marketplace.json'))"
python3 -c "import json; json.load(open('books/<book-slug>/plugin/.claude-plugin/plugin.json'))"

# Every skill folder has a SKILL.md with name + description frontmatter
find books/<book-slug>/plugin/skills -name SKILL.md
```

## Conventions

- **Credit the author** in every plugin README, playbook, and SKILL where natural. These skillsets restructure others' ideas; they don't replace the books.
- **Keep books independent.** Adding one should never edit another book's files — only the shared `marketplace.json` and root `README.md`.
- **Start at `0.1.0`** and bump the plugin version when you meaningfully change its skills.
