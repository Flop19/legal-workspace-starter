# AGENTS.md

[One line: who I am, my role, my company. Filled by `/setup-workspace`.]

This file is shared across agent tools; tool-specific files (`CLAUDE.md`) point
here. Edit this file, not those.

## Where things live

- `knowledge/`: what lasts — the business, the legal positions and how I work:
  - `counsel-brief.md`: the high-level picture — the business, key people, entities,
    applicable law, HR, tools — and the standing positions that shape all of it.
  - `preferences.md`: how I want you to work and write.
  - `<topic>.md`: the detail behind it, one file per topic, created as work produces it.
  - `sources/`: retained company-level source documents, created when needed.
- `matters/`: live work, one flat folder each. `matters/INDEX.md` lists every matter.
  Documents belonging to a matter go in its `docs/` folder, created when needed.
- `desk/`: anything that is not a matter: a dropped file, a quick task, a one-off
  work product.
- `.claude/skills/`: procedures for recurring work. Match the request to a skill's
  description and follow it; if none matches, proceed directly.

## Rules for every session

- Read `knowledge/counsel-brief.md` and `knowledge/preferences.md`.
- Before substantive work, check `knowledge/` for relevant topic files and read
  any that bear on the question.
- Decide what the request is:

  - **Matter work** — read `matters/INDEX.md` first. It answers two questions:
    - *Does this matter already exist?* If it does, read its `brief.md`, current
      state first. If an existing matter appears to cover the request, propose using it rather
      than opening a second folder; a subtask goes inside its parent. Only if it's genuinely new: copy
      `matters/_template/`, set `Opened` to today, add a row at the top of `INDEX.md`.
    - *What else does it touch?* Any other matter with the same counterparty, the
      same regulation, or an obligation one creates for the other — say so at the
      start, and again later if it becomes relevant.
  - **Quick ask or one-off task** — just do it; anything worth keeping goes in
    `desk/YYYY-MM-DD-slug/`. Don't create a matter unless I ask.
- When relying on a position or fact in `knowledge/<topic>.md`, cite its recorded
  source and date. If the date is missing or more than three months old, flag that
  the entry may need reconfirmation.
- Update the active matter's Current state before the end of a session.
- Keep this workspace compounding: proactively propose using `/file-it` rather than waiting to
  be asked — when I state something as settled or durable, when an authoritative
  document arrives, or when something already filed turns out wrong or out of date,
  whether I say so or your own work shows it.
- Always ask before changing this file and present what you want to change.
