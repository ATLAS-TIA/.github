# ATLAS-TIA Team Workflow

Use this page to delegate repository work to your coding agent with clear controls.

GitHub workflow, in brief: work is done on personal branches, changes are pushed to GitHub, then reviewed in a Pull Request (PR) before anything is merged into `ATLAS-MAIN`.

If you are an AI coding agent (Codex/Claude), read and follow the `Agent Rules Of Engagement` section before making any changes.

When starting a session, tell your agent to treat this file as an active instruction source:
`.github/profile/README.md`

## How to Setup GitHub With Agent

The following two prompts set up first-time use with Codex/Claude to connect to your GitHub and this project. Prompt #1 should help provide you with explicit instructions for how to setup SSH to push changes/updates directly from Codex/Claude, without having to open GitHub. Prompt #2 will have Codex/Claude set up an instruction file for themselves to follow rules for version control and ensuring that we do not erase eachother's work.

### First-Time Setup (Prompt #1)

```text
Configure GitHub SSH access for this workstation and verify this repo is ready for contributions.

Repo: git@github.com:ATLAS-TIA/ATLAS-MAIN.git
Base branch: ATLAS-MAIN
My GitHub username: <your-username>

Please execute in this order:
1) Check if SSH is already set up on my machine.
2) If SSH is not set up, create a key and show me exactly what to copy.
3) Tell me exactly where to paste that key in GitHub.
4) Test GitHub connection.
5) Confirm this repo is connected and ready.
6) Set up my personal branch using my username.

Important:
- Do not push any code yet.
- Pause before any step that requires browser clicks from me.
- Provide concise status updates and final verification.
```

### Policy/Rule File Setup (Prompt #2)

```text
Set up persistent agent policy files for this ATLAS repo so future sessions follow our workflow rules automatically.

Please:
1) Create or update AGENTS.md for Codex-style agents.
2) Create or update CLAUDE.md (or READMECLAUDE.md if that is the active file) for Claude-style agents.
3) Include these required rules in both files when working on ATLAS:
   - Never push directly to ATLAS-MAIN.
   - Always create/use a personal branch for task work.
   - Open PRs targeting ATLAS-MAIN.
   - Wait for group confirmation before merge.
   - Keep commits small and list files changed.
4) Keep wording concise and consistent across files.
5) Show me the exact file paths and final content before committing.
6) Commit and push on my personal branch only.
```

### If The Agent Asks You To Add An SSH Key

Complete these steps in GitHub:

1) Open `GitHub > Settings`.
2) Open `SSH and GPG keys`.
3) Click `New SSH key`.
4) Paste the key the agent gave you.
5) Save.
6) Tell the agent: `SSH key added, continue`.

## General Engagement Instructions

This section provides an overview of general rules of engagement and conduct when pushing changes to your branch. Prompt #3 effectively provides the same instructions as the policy/rule setup prompt above, but may be useful as a reminder if you find that Codex/Claude is not following instructions, especially at the start of a new session.

### Reminder/Instruction Prompt (Prompt #3)

```text
You are working in repo ATLAS-MAIN under my personal branch.

Engagement rules:
1) Create and use my personal branch for all work.
2) If my personal branch already exists, continue working in it.
3) Do not push directly to ATLAS-MAIN.
4) Keep edits focused and easy to review.
5) List files changed and summarize what changed.
6) Push only to my personal branch.
7) Prepare or update a PR into ATLAS-MAIN.
8) Do not merge until I confirm group approval.

```

## Agent Rules Of Engagement

The agent must follow these rules:

1) Never push directly to `ATLAS-MAIN`.
2) Always create/use a personal branch per task.
3) Keep commits small and clear.
4) Explain changes in plain language.
5) List exact files changed.
6) Run available checks/tests when possible.
7) Open PRs targeting `ATLAS-MAIN`.
8) Wait for group confirmation before merge.
9) If `AGENTS.md` / `CLAUDE.md` policy files exist, treat them as binding instructions.
