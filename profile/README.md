# ATLAS-TIA Team Workflow

Use this page to delegate repository work to your coding agent with clear controls.

GitHub workflow, in brief: work is done on personal branches, changes are pushed to GitHub, then reviewed in a Pull Request (PR) before anything is merged into `ATLAS-MAIN`.

If you are an AI coding agent (Codex/Claude), read and follow the `Agent Rules Of Engagement` section before making any changes.

When starting a session, tell your agent to treat this file as an active instruction source:
`.github/profile/README.md`

## Human Setup With Agent

Provide your agent with:

- Your GitHub username
- Repo URL: `git@github.com:ATLAS-TIA/ATLAS-MAIN.git`
- Base branch: `ATLAS-MAIN`

### First-Time Setup Prompt (Copy/Paste)

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

Important:
- Do not push any code yet.
- Pause before any step that requires browser clicks from me.
- Provide concise status updates and final verification.
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

Use this at the start of work. You can continue in the same chat after this.

### Engagement Prompt (Copy/Paste)

```text
You are working in repo ATLAS-MAIN.

Engagement rules:
1) Create and use my personal branch for all work.
2) If my personal branch already exists, continue working in it.
3) Do not push directly to ATLAS-MAIN.
4) Keep edits focused and easy to review.
5) List files changed and summarize what changed.
6) Push only to my personal branch.
7) Prepare or update a PR into ATLAS-MAIN.
8) Do not merge until I confirm group approval.

My personal branch:
<branch-name-or-create-one>

Task:
<describe your change in plain language>
```

### Add This Line To Any Prompt (Copy/Paste)

```text
While working, continuously reference and follow: .github/profile/README.md
```

### Continue Existing Work Prompt (Copy/Paste)

```text
Continue my existing personal branch:
<branch-name>

New request:
<what you want changed>

After editing:
1) Push updates to the same branch.
2) Summarize what changed in plain language.
3) Update the PR description if needed.
```

## Merge Policy

Before any merge into `ATLAS-MAIN`, confirm with the group.

Required sequence:
1) Agent prepares/updates PR into `ATLAS-MAIN`.
2) Team reviews and confirms merge is approved.
3) Only after group confirmation, proceed with merge.

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
