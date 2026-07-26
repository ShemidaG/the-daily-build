# the-daily-build

**One small web app, built from scratch, every day — by Claude.**

Every day at **12:00 PM Manila time**, Claude gives itself about thirty minutes to
design and build one small, self-contained web app of its own choosing — the
idea, the code, and the UI. No frameworks to install, no backend: each app is a
single `index.html` that runs fully offline in any browser.

This repo is the home of that habit and the growing collection it produces.

## 🎨 See the apps

- Browse the gallery: [`daily-apps/index.html`](daily-apps/index.html)
- Details & how it runs: [`daily-apps/README.md`](daily-apps/README.md)

| Day | Date | App | What it does |
|-----|------|-----|--------------|
| ★ | 2026-07-26 | [**Momentum**](daily-apps/2026-07-26-momentum/) | **Flagship productivity command center** — projects, priorities, due dates, subtasks, Kanban board, focus timer, and an analytics dashboard |
| 3 | 2026-07-26 | [Pulse](daily-apps/2026-07-26-pulse/) | 16-step drum machine with live-synthesized sounds, swing, and random patterns |
| 2 | 2026-07-26 | [Huely](daily-apps/2026-07-26-huely/) | Color-palette generator with harmony modes, locking, and saved palettes |
| 1 | 2026-07-24 | [FocusFlow](daily-apps/2026-07-24-focusflow/) | Pomodoro timer + task list with stats, themes, and chimes |

## ⚙️ How the daily build runs

Two mechanisms, same result:

1. **GitHub Action (permanent)** — [`.github/workflows/daily-web-app.yml`](.github/workflows/daily-web-app.yml)
   runs on a `cron` at `04:00 UTC` (= 12 PM Manila) every day. It runs Claude on
   a **Claude Pro/Max subscription** via a `CLAUDE_CODE_OAUTH_TOKEN` secret — no
   pay-per-use API billing.
2. **In-session scheduler** — while a Claude Code session is live, an in-memory
   daily job does the same thing (auto-expires after 7 days).

See [`daily-apps/README.md`](daily-apps/README.md) for the one-time token setup.

## 🌱 Principles

- **Self-contained.** Every app is one HTML file, works offline, saves to your
  own browser — nothing phones home.
- **Small and finished.** Scoped to roughly thirty minutes, but complete: a real,
  usable thing each day, not a stub.
- **Designed, not just coded.** The UI is part of the build — responsive, with a
  considered light/dark look where it fits.

---

*A daily building habit, kept by Claude.*
