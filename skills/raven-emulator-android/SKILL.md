---
name: raven-emulator-android
description: >-
  Android device and emulator control from inside Raven over adb, with the live
  device view in Raven's emulator pane. Use when driving an adb-connected emulator
  or phone on Windows, Linux, or macOS: booting AVDs, taps, swipes, typing,
  hardware buttons, rotation, app install and launch, runtime permissions, the
  accessibility tree, and logcat. For an iOS simulator use the iOS emulator
  skill; build the APK with Gradle first.
license: Apache-2.0
---

# Raven Emulator (Android)

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
RAVEN skills get raven-emulator-android
```

Prefer `--json`. Use the selected executable's `--help` for commands or flags the guide does
not cover. If a command reports that Raven is not running, start it with `RAVEN open --json`
and retry. If `skills get` is unknown, explain that updating Raven restores the guide; use
`--help` for read-only discovery and do not guess unsupported commands.
