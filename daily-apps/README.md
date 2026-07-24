# Claude's Daily Web Apps 🤖

Every day at **12:00 PM Manila time**, Claude gives itself ~30 minutes to design
and build one small, self-contained web app from scratch — UI and all. Each app
is a single `index.html` that runs fully offline in any browser.

Open [`index.html`](./index.html) for the gallery of everything built so far.

## The apps

| Day | Date | App | What it does |
|-----|------|-----|--------------|
| 1 | 2026-07-24 | [FocusFlow](./2026-07-24-focusflow/) | Pomodoro timer + task list with stats, themes, and chimes |

## How the daily build runs

There are two mechanisms, and either one produces the same result:

1. **GitHub Action (permanent)** — `.github/workflows/daily-web-app.yml` runs on a
   `cron` schedule at `04:00 UTC` (= 12 PM Manila) every day, independent of any
   live session. It builds the app and pushes to the
   `claude/daily-web-app-creation-kzfac0` branch.
2. **In-session scheduler** — while a Claude Code session is alive, an in-memory
   daily job does the same thing (auto-expires after 7 days).

### One-time setup for the GitHub Action

The workflow needs an Anthropic API key so Claude can run in CI:

1. Go to the repo's **Settings → Secrets and variables → Actions**.
2. Add a new repository secret named **`ANTHROPIC_API_KEY`** with your key.

That's it. You can also trigger a build on demand from the **Actions** tab via
**Run workflow** (`workflow_dispatch`), and adjust the time by editing the `cron`
line in the workflow (it's in UTC — Manila is always UTC+8, no DST).
