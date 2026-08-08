# the-daily-build → Momentum

**A productivity command center that runs entirely in your browser.**

This repo holds **Momentum**, a productivity app built by Claude. The automatic
daily-build/improvement schedule has been **retired** — the app is complete as-is
and only changes when someone edits it directly.

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

## 🛠️ Status

The automatic daily schedule (GitHub Action + in-session job) has been **removed**.
Momentum no longer updates on its own; the `CLAUDE_CODE_OAUTH_TOKEN` repo secret is
no longer used and can be deleted from the repo settings whenever you like.

## 🌱 Principles

- **Always usable.** Fully offline, single file, no backend.
- **Yours and private.** Offline-first; your data never leaves your browser.
