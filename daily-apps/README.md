# Claude's Daily Web Apps 🤖

Every day at **12:00 PM Manila time**, Claude gives itself ~30 minutes to design
and build one small, self-contained web app from scratch — UI and all. Each app
is a single `index.html` that runs fully offline in any browser.

Open [`index.html`](./index.html) for the gallery of everything built so far.

## The apps

| Day | Date | App | What it does |
|-----|------|-----|--------------|
| 2 | 2026-07-26 | [Huely](./2026-07-26-huely/) | Color-palette generator with harmony modes, locking, and saved palettes |
| 1 | 2026-07-24 | [FocusFlow](./2026-07-24-focusflow/) | Pomodoro timer + task list with stats, themes, and chimes |

## How the daily build runs

There are two mechanisms, and either one produces the same result:

1. **GitHub Action (permanent)** — `.github/workflows/daily-web-app.yml` runs on a
   `cron` schedule at `04:00 UTC` (= 12 PM Manila) every day, independent of any
   live session. It builds the app and pushes to the
   `claude/daily-web-app-creation-kzfac0` branch.
2. **In-session scheduler** — while a Claude Code session is alive, an in-memory
   daily job does the same thing (auto-expires after 7 days).

### One-time setup for the GitHub Action (no paid API needed)

The workflow runs on your existing **Claude Pro/Max subscription** via an OAuth
token — there is **no pay-per-use API billing**. Set it up once:

1. In a terminal with Claude Code installed, run:
   ```
   claude setup-token
   ```
   Log in with your Claude account and copy the token it prints.
2. Go to the repo's **Settings → Secrets and variables → Actions**.
3. Add a new repository secret named **`CLAUDE_CODE_OAUTH_TOKEN`** and paste the
   token.

That's it. GitHub Actions minutes are free on public repos (and private repos
get 2,000 free minutes/month — this job uses well under that). You can also
trigger a build on demand from the **Actions** tab via **Run workflow**
(`workflow_dispatch`), and adjust the time by editing the `cron` line in the
workflow (it's in UTC — Manila is always UTC+8, no DST).

> **Costs, in plain terms:** the pay-per-use Anthropic **API** costs money; a
> Claude **Pro/Max subscription** does not charge per run. This workflow uses
> the subscription path, so if you already have Pro or Max, the daily build is
> covered with no extra charge.
