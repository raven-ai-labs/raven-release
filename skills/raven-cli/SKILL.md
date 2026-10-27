---
name: raven-cli
description: >-
  Operate Raven-managed worktrees, folder contexts, terminals, repos, automations, artifacts,
  skill sharing, worktree comments, and Raven's embedded browser through the `raven` CLI. Use
  when the user says "$raven-cli", "Raven worktree", "child worktree", "spawn codex/claude in a
  worktree", "read/wait/send Raven terminal", "handoff" / "handover" / "give this to another
  agent", "Raven browser", "raven artifacts", or "share skills". Prefer it over raw git
  worktree, ad hoc PTYs, or Computer Use when Raven state is involved. Use Computer Use only
  when a visible window needs GUI control that a CLI, filesystem, or API cannot do.
---

# Raven CLI

This discovery stub loads the version-matched guide from the Raven executable used for this session.

## Resolve the CLI for this session

Choose the executable once and reuse it for every later command:

- If the `RAVEN_CLI_COMMAND` environment variable is set, use its value. Raven exports this
  for managed WSL sessions.
- Otherwise, in a dev checkout whose session exposes `RAVEN_DEV_REPO_ROOT`, use `raven-dev`.
- Otherwise, use `raven`.

Below, `RAVEN` is a placeholder for the executable you resolved. Substitute it before
running anything; do not create a shell variable or run `RAVEN` literally. This works the
same way in POSIX shells, PowerShell, and cmd.exe.

If the selected executable cannot run, report its exact error and stop. Do not fall through
to another executable, which could silently target a different Raven build.

## Load the version-matched guide before running Raven commands

```text
RAVEN skills get raven-cli
```

Prefer `--json`. Use the selected executable's `--help` for commands or flags the guide does
not cover. If a command reports that Raven is not running, start it with `RAVEN open --json`
and retry. If `skills get` is unknown, explain that updating Raven restores the guide; use
`--help` for read-only discovery and do not guess unsupported commands.
