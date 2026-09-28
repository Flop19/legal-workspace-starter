---
name: setup-workspace
description: Onboards a new user. Interviews them about their profile and company, its legal setup, and their preferences, then fills the identity line in AGENTS.md and the forms in knowledge/counsel-brief.md and knowledge/preferences.md. Run at first launch; re-run any time to redo onboarding.
---
# Set up workspace

Fill the template files from an interview with the user. The
user supplies material and answers your questions in plain language. You ask the
questions, do the writing and fill the templates.

## Start: ask for material

Your first message asks for a website link, a pitch deck, or other existing context
documents on the company, to be linked or dropped in `desk/`.

If the user supplies anything, read it and draft what you can, then continue with
the interview. If the user doesn't supply anything or skips this step, continue
with the interview.

## How to run the interview

- Say what's coming — six rounds, one per heading of
  `knowledge/counsel-brief.md`, then preferences — and announce each as you go:
  "Round 2 of 6 — key people". Open with: name, role, company, what their work
  responsibilities are.
- The bracketed keywords under each heading note what belongs in that section —
  they are not a script. Compose plain, easy questions from them. Group what a
  person would answer in one breath. Skip anything an earlier answer or the
  material already covered.
- **Make it easy and engaging to answer.** Where an answer is a choice or a
  multi-select, offer options with room for an answer in the user’s own words (in Claude Code:
  `AskUserQuestion`) instead of asking an open-ended question, and include
  "none", "not sure", or "skip" where appropriate. Do not turn a skipped or
  uncertain answer into a statement that something does not exist.
  Otherwise use your judgement: the aim is a conversation, not a form.
- The user may skip any question. Ask at most one follow-up per round. If something is still
  missing after that, leave it out of the file and move on. Not every detail needs
  to be filled.
- Short answers are enough; draft from them. After each round, show the draft and get a confirmation or a correction. Keep their phrasing over the template's.

## What to fill

1. `AGENTS.md` — the one bracketed line at the top: who they are, their role, their
   company. One sentence, in their words.
2. `knowledge/counsel-brief.md` — the six sections. Replace the keywords with the
   answers, written as prose in the user's own words, and leave out anything
   unanswered rather than marking it.
   Set the initial-fill date and each section's As of date to the setup date.
   Don't create `knowledge/<topic>.md` files — those appear when work produces them.
3. `knowledge/preferences.md` — fill the **Language** line. Then ask whether they
   already have working preferences, an AI style guide or a house style note; if so,
   adapt the defaults to it. Otherwise ask: "What do you find yourself fixing in every AI draft?" and add the answer in their words. The shipped
   defaults are usable as they stand.

## Finish

List each file you changed, one line each, and say which questions are still
unanswered.

Then explain briefly how the workspace works — this is the first time they'll see
it:

- Anything they bring in is either **matter work** or a **quick ask**.
- `matters/` holds work they'll come back to — one folder each, and its `brief.md`
  says where things stand, so the user can resume work without re-explaining the background.
- `desk/` is everything else: a dropped file, a one-off task.
- `knowledge/` is the workspace's durable memory. It grows out of the work: when
  something gets settled or turns out wrong, `/file-it` records it — dated, with
  what it rests on — so it doesn't need repeating.

Then propose one concrete first step — open the first real matter, whatever is
actually on their plate today. Starting it is as simple as saying "new matter …".
