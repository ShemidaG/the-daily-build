# Momentum

**Momentum** is a productivity command center that runs entirely in your browser —
projects, priorities, planning, focus, and analytics in one fast, offline app.
Claude improves it a little every day at **12:00 PM Manila time**.

- **Launch the app:** [`2026-07-26-momentum/index.html`](./2026-07-26-momentum/index.html)
- **Landing page & changelog:** [`index.html`](./index.html)
- **Live:** https://shemidag.github.io/the-daily-build/daily-apps/2026-07-26-momentum/

## Highlights

Projects and tasks (P1–P4 priorities, due dates, tags, notes, subtasks) ·
recurring tasks · natural-language quick-add · Today / Upcoming / All / Kanban
board / Completed views with sort & filter · command palette (⌘K) · focus timer
with per-task logging · analytics dashboard · search · undo · JSON export/import ·
dark/light themes. Fully offline; data stays in your browser.

## How the daily improvement runs

Two mechanisms, same result — every day Claude adds one useful improvement and
pushes it to `main` (served live by GitHub Pages):

1. **GitHub Action (permanent)** — [`../.github/workflows/daily-web-app.yml`](../.github/workflows/daily-web-app.yml),
   on a `cron` at `04:00 UTC` (= 12 PM Manila).
2. **In-session scheduler** — while a Claude Code session is alive.

### One-time setup for the GitHub Action (no paid API needed)

The workflow runs on your **Claude Pro/Max subscription** via an OAuth token —
no pay-per-use billing:

1. In a terminal with Claude Code installed, run `claude setup-token` and copy
   the token.
2. In the repo's **Settings → Secrets and variables → Actions**, add a secret
   named **`CLAUDE_CODE_OAUTH_TOKEN`** with that token.

You can trigger a build on demand from the **Actions** tab (**Run workflow**),
and change the time by editing the `cron` line (UTC; Manila is always UTC+8).
