# AGENTS.md

## What this project is

Mindaloy is a standalone spaced repetition web app. It owns its own data and exposes an API, so external clients such as agents can create cards, run reviews, and read progress through the same operations the web app uses. The current plan is `docs/plans/0001-plan-mindaloy-2026-10-21.md`.

## Build and test

There is no application code yet, so there is no build or test command. Add the commands here when the stack is set up.

## What an agent must not do

- Do not commit unless the prompt asks for it.
- Do not add a runtime dependency on the external learning repository or its Markdown formats.
- Do not build UI before the owner approves a visual reference.

## Docs artifact naming

- An artifact under `docs/<type>/` (a plan, a QA plan, a review, research) is named `NNNN-<type>-<slug>-YYYY-MM-DD.md`.
- `NNNN` is a four-digit serial, per directory, assigned in creation order and never reused. To get it, take the highest serial in that directory across this worktree, every other worktree that `git worktree list` names, and `origin/HEAD` (`git ls-tree --name-only origin/HEAD <dir>` after `git fetch origin`), and add one. Scan all three, because parallel worktrees otherwise take the same serial. Skip a source that fails, such as no remote, and without git list the directory only. An empty directory starts at `0001`.
- `YYYY-MM-DD` is the creation date. The whole name stays fixed after edits.
- An ADR uses its decision number as the serial: `docs/adr/NNNN-adr-<slug>-YYYY-MM-DD.md`.
- Reader-facing pages (`docs/wiki/`, how-to guides, runbooks) stay unnumbered.
