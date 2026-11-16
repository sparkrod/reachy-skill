# Setup and Testing

Use this reference for an app's local environment and verification. Read the linked project guidance for current commands and hardware-specific details.

## Setup

- Read `agents.local.md` first and reuse a completed setup when documented.
- If it is absent, Python work must follow the project setup guide. JS/Web work may skip full environment setup; create a concise `agents.local.md` with known robot type and relevant preferences, without guessing unknown details.
- Before setup, tell the user what resources are needed and confirm a permanent absolute path. Clone only the SDK or example apps relevant to the task.
- Check for missing tools before proceeding. Explain all missing tools and ask once before installing any of them. Adapt commands to the user's OS.
- For Python setup, use the project's setup guide; prefer `uv` when appropriate. Verify the SDK import before recording setup as complete.
- If a documented command fails, show the error and ask the user to run it or decide how to proceed. Do not attempt complex workarounds without approval.

## Testing

- Ask before starting a daemon. Use simulation by default. Physical hardware requires explicit user authorization, and wait for the user to confirm readiness before any physical test.
- Check the user's robot type and existing daemon state before proposing a test. Avoid starting a second daemon.
- Run the app's documented local checks. Check startup, requested behavior, clean exit, and relevant error output; repeat after fixes.
- Simulation cannot verify camera tracking, audio I/O, physical button presses, or real motor behavior. State those limitations rather than claiming hardware validation.
- Do not install daemon branches or run daemon-development test loops as part of ordinary app authoring.

## Canonical sources

- [Project agent guidance (`AGENTS.md`)](https://github.com/pollen-robotics/reachy_mini/blob/main/AGENTS.md)
- [Environment setup](https://github.com/pollen-robotics/reachy_mini/blob/main/skills/setup-environment.md)
- [App testing](https://github.com/pollen-robotics/reachy_mini/blob/main/skills/testing-apps.md)
- [Troubleshooting](https://github.com/pollen-robotics/reachy_mini/blob/main/docs/source/troubleshooting.md)

Reviewed 2026-11-16; source snapshot at commit `0f21887aad6dfed44dd2d6a7c6f2a7ede84c7360`.
