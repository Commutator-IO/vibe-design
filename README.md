# vibe-design

**Skillsets distilled from great books, turned into installable Claude plugins.**

Each book that changes how you work becomes a small, reusable toolkit here: a set of Claude *skills* that walk you through the book's method, plus a human-readable *playbook*. Install a plugin and Claude runs the method with you; read the playbook when you want the ideas in your own head.

The first entry adapts Jake Knapp's *Sprint* into a five-day workflow for building working software with Claude. More books will follow.

## What's inside

```
vibe-design/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace manifest — lists every book's plugin
├── books/
│   └── sprint-jake-knapp/        # One folder per book
│       ├── README.md             # About this book's skillset
│       ├── plugin/               # Installable Claude plugin (skills)
│       └── playbook/             # Human-readable guide (Markdown)
├── templates/
│   └── book-template/            # Copy this to start a new book
├── docs/
│   └── ADD-A-NEW-BOOK.md         # Step-by-step guide for adding a book
└── LICENSE
```

Every book lives in its own self-contained folder under `books/`, holding both the plugin and the playbook. Adding a book never touches the others.

## The library

| Book | Author | Plugin | What it does |
|------|--------|--------|--------------|
| [Sprint](books/sprint-jake-knapp/) | Jake Knapp, John Zeratsky, Braden Kowitz | `build-sprint` | A 5-day sprint to build and test working software with Claude |

## Install a plugin

This repo is a Claude Code / Cowork **plugin marketplace**. Add it once, then install any book's plugin:

```
/plugin marketplace add Commutator-IO/vibe-design
/plugin install build-sprint@vibe-design
```

Or, in Cowork, open the `.plugin` file from a book's folder to install it directly.

## Add your own book

1. Copy `templates/book-template/` to `books/<book-slug>/`.
2. Fill in the skills and playbook (see [`docs/ADD-A-NEW-BOOK.md`](docs/ADD-A-NEW-BOOK.md)).
3. Register the plugin in `.claude-plugin/marketplace.json`.
4. Add a row to the library table above.

## License

MIT — see [LICENSE](LICENSE). Book methods remain the intellectual property of their authors; these plugins restructure their ideas for use with Claude and credit each source.
