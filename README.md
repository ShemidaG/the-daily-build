# the-daily-build → Momentum

**One productivity tool, made a little better every day — by Claude.**

This repo builds and continuously improves **Momentum**, a productivity command
center that runs entirely in your browser. Every day at **12:00 PM Manila time**,
Claude spends ~30 minutes adding a genuinely useful improvement — a new feature,
a refinement, or a polish pass — and ships it.

## 🚀 Use it

- **Live app:** https://shemidag.github.io/the-daily-build/daily-apps/2026-07-26-momentum/
- **Landing page & changelog:** https://shemidag.github.io/the-daily-build/daily-apps/

It's a single `index.html` — no install, no backend, fully offline, and all your
data stays in your browser (with JSON export/import for backups).

## ✨ What Momentum does

- **Projects & tasks** — color-coded projects; tasks with P1–P4 priorities, due
  dates, tags, notes, and subtask checklists
- **Recurring tasks** — daily / weekly / every-weekday / monthly, auto-rescheduled
- **Smart quick-add** — `Draft Q3 report !p1 #Work @deep every weekday` parses
  priority, project, tag, due date, and recurrence
- **Views** — Today, Upcoming (7-day), All, a drag-and-drop **Kanban board**, and
  Completed, each with sort & filter controls
- **Command palette (⌘K)** — jump to any view, run any action, or search tasks
- **Focus timer** — Pomodoro sessions logged against the specific task
- **Analytics** — 7-day completion chart, focus minutes, streak, completion rate
- **Quality of life** — search, undo delete, keyboard shortcuts, JSON
  export/import, dark/light themes

## 🛠️ How the daily improvement runs

1. **GitHub Action (permanent)** — [`.github/workflows/daily-web-app.yml`](.github/workflows/daily-web-app.yml)
   runs on a `cron` at `04:00 UTC` (= 12 PM Manila) every day. It improves
   Momentum and pushes to `main` (served live by GitHub Pages) using a Claude
   **Pro/Max subscription** via a `CLAUDE_CODE_OAUTH_TOKEN` secret — no
   pay-per-use API billing.
2. **In-session scheduler** — while a Claude Code session is live, an in-memory
   daily job does the same thing.

See [`daily-apps/README.md`](daily-apps/README.md) for the one-time token setup.

## 🌱 Principles

- **Depth over novelty.** Improve one real tool instead of shipping throwaway toys.
- **Always usable.** Every change is verified to run error-free before it ships.
- **Yours and private.** Offline-first; your data never leaves your browser.
