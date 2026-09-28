# Legal workspace starter

A lean, ready-to-use starter setup for in-house lawyers who want their AI work to compound. The workspace contains an opinionated folder structure and a set of plain-text files for an AI assistant to retain context on your company and legal positions, track ongoing work, and continuously improve based on your feedback. The goal: less repeating of context, a compounding home for your work, and a place to try out and learn agentic legal work.

Optimized for Claude Code, but vendor-agnostic and portable to any model and harness that reads `AGENTS.md`. You download the starter files, point your AI assistant at them and run `/setup-workspace` to self-onboard and start doing real work in less than 15 minutes. Zero coding experience needed.

**What it is not:** The workspace is not a legal product. It is an opinionated folder and logic structure. You bring your own legal skills, knowledge, tools and judgment; this workspace connects them and brings them together through custom memory, routing and feedback logic. You retain full freedom and control: files live on your machine; you decide what to bring in and connect, what to keep outside of the system, and which model providers and plans you work with.

## What's inside

```text
legal-workspace-starter/

├── AGENTS.md                  ← the map: who you are, what lives where, how to work
├── CLAUDE.md                  ← points Claude to the shared agent instructions
├── knowledge/                 ← lasting context on company, legal positions, preferences
│   ├── counsel-brief.md       ← how you'd brief new counsel on your work
│   ├── preferences.md         ← how you want the agent to work with you
│   └── <topic>.md             ← detailed knowledge on a topic, added as work produces it
├── matters/                   ← ongoing work, one folder per matter
│   ├── INDEX.md               ← index of every matter
│   └── _template/             ← copy to start a new matter
│       ├── brief.md           ← current state, context, decisions, and related work
│       └── docs/              ← work products for the matter
├── desk/                      ← dropped files, quick asks, and one-off work products
└── .claude/skills/            ← recurring tasks (legal and non-legal)
    ├── setup-workspace/       ← interviews you and fills the starter files
    └── file-it/               ← routes context and corrections to the right file; keeps this workspace compounding
```

## How to set it up

The interface of this workspace (where real work happens) is VS Code, a free editor tool. It is hooked up to Claude Code or Codex as the AI assistant (used interchangeably). It lets you run multiple sessions in parallel and shows your entire workspace as a folder tree on the left, like you're familiar with from any DMS. *Note:* you can absolutely run this through other tools/harnesses that work on local folders (e.g., Claude Cowork).

1. **Download the workspace files.** Download the ZIP (green `Code` button at the top → `Download ZIP`) and unzip it wherever you keep your files. Rename the folder to something you like (e.g., `legal-workspace`).
2. **Install VS Code.** Download and install it for free from [code.visualstudio.com](https://code.visualstudio.com).
3. **Open your workspace in VS Code.** `File → Open Folder` → select your workspace. The file tree appears on the left. Then `Terminal → New Terminal` opens a terminal already inside your folder.
4. **Connect your AI assistant.** Install [Claude Code](https://code.claude.com/docs/en/quickstart) or [Codex](https://github.com/openai/codex) by pasting the install command from its *quickstart tutorial* into the terminal. Then type `claude` or `codex`, sign in and confirm. The assistant reads the workspace map automatically (`CLAUDE.md` for Claude, `AGENTS.md` for other compatible assistants).
5. **Run onboarding.** Tell the assistant to set up the workspace. It invokes the `/setup-workspace` skill and interviews you about your company, role and work, then fills in the starter files. Paste links or material (e.g., your company website) for quicker onboarding.
6. **(Optional) Add VS Code extensions.** Extensions such as Office Viewer let you open and edit Word, Excel and PowerPoint files directly through VS Code.
7. **Start with real work.** Ask to open your first matter, or drop a file in `desk/` for a quick task.

## How to use it

- **Work on your matters.** Use it like the chat window of Claude or ChatGPT: tell the assistant what you want to work on, and it classifies and routes it — a new matter, an existing one, or a quick ask. New matters are set up from `matters/_template/`. Work products land in each matter's `docs/`; the `brief.md` carries a summary and the current state. Durable positions and facts get promoted to `knowledge/`, where future work sessions fetch them.
- **Organize your knowledge.** Use `/file-it` when a fact, legal position, or working preference becomes settled. The assistant proposes the exact change and destination for confirmation, preserving sources and dates in the convention you like, then makes the change to keep your system organized and growing.
- **Automate your workflows.** Add new skills in `.claude/skills/<name>/SKILL.md` and adapt third-party skills to your work. A skill describes when it applies and how the assistant should carry out the task. Use it to automate both legal and non-legal workflows.
- **Give it your voice.** `knowledge/preferences.md` holds your preferences for tone and working style. Start with the template and let it adapt as you work, or bring in your existing preferences at onboarding.
- **Maintain the map.** Let your assistant keep `AGENTS.md` current so it always has the relevant context at the start of every session.

## Grow it yourself

This workspace is just a starting point. The design is carried by the routing (`AGENTS.md`), the workspace structure (`knowledge/`, `matters/`, `desk/`, `.claude/skills/`) and the feedback logic (`/file-it`). Beyond that, decide yourself what to add:

- **Structure:** Rename folders, add knowledge files for areas you work in a lot, add your templates, and adapt the workspace to how you organize your own work.
- **Skills:** Bring your own (legal and non-legal) skills or adapt existing ones. Add one whenever you have recurring work.
- **Connectors:** Connect Slack, Notion, or any other tool that offers an MCP connector. Scope connectors carefully and review data flows and access.
- **Model routing:** Use different models depending on task and complexity; set up routing for research, execution and review tasks.
- **Build tools:** Build on top of your work, e.g. a matter dashboard, a deadline tracker or a Slack notifier.

## Credits

This idea and structure for this workspace is inspired by Adam Faik's [Claude Code PM Starter](https://github.com/adamfaik/claude-code-pm-starter).
