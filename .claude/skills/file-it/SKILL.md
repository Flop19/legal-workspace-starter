---
name: file-it
description: Make a correction or a settled outcome permanent instead of losing it with the session, routing it automatically to where it belongs. This helps the workspace compound.
---
# File it

Durable facts, positions or feedback get lost when a session ends. This skill
routes what should outlast the session to the place it belongs, in the shape that
place needs, confirmed before it's written.

`AGENTS.md` says when to raise this skill.

Don't file one-off mistakes, temporary matter status or unsettled analysis. An
authoritative document arriving is a reason to inspect it, not automatically to
adopt its contents as a standing position.

## Where it goes

Route each item separately, but group related changes into one proposal and
confirmation.

1. **Durable knowledge — a conclusion, a fact, or a change to either** →
   `knowledge/`. The high-level picture every session needs goes in
   `counsel-brief.md`, under its matching heading; everything else goes in the
   `knowledge/<topic>.md` whose name already covers it — check existing files for overlapping topics before
   creating a new one. Cite the source where it lives. If a supporting document is in
   `desk/`, propose moving it to the relevant matter's `docs/` folder or, for
   company-level documents, `knowledge/sources/`. Include the move and any
   reference updates in the filing proposal.
2. **Taste or working style** — correct, but not how the user wants it →
   `knowledge/preferences.md`, one line carrying the rule and why it matters.
3. **A recurring process is wrong** — the steps, format or quality bar of work that
   repeats → edit the matching skill in `.claude/skills/`, so the correction applies on every run. If no skill covers it and the issue has come up before, offer to write one.
4. **How every session should behave** — a standing rule or routing habit that
   isn't tied to one procedure → `AGENTS.md`.

If a topic file becomes difficult to scan and contains distinct subtopics, propose
splitting it into more specific files. Move entries rather than copying them,
update references, and retain the parent file only if it still contains useful
general content. Include the split in the filing proposal.

## Writing it

- **Propose the destination and exact addition or replacement; obtain confirmation
  before writing.** Never write into `knowledge/`, a skill or `AGENTS.md` silently.
- **Give each distinct fact or position a descriptive heading, followed by
  Date · Position/Fact · Source.** Keep Position/Fact
  brief — executive-summary style. Date is when the fact or position was established
  or substantively reconfirmed, not when its wording was edited. Source points to
  the supporting document or records the user's dated confirmation. Keep
  counsel-brief summaries concise.
- Update a counsel-brief section's As of date when its content is substantively
  updated or reconfirmed, not merely reworded.
- **An entry that already exists gets edited, not duplicated.** Check directly
  related summaries and references, and include any necessary updates in the same
  proposal.
- **Write the why**, and ask if it isn't obvious. Without the reason, the rule can't be applied to edge cases.
- **Confirm in chat what was filed and where.**
