# Python Apps

Choose Python when the user requests it or when the app needs unattended/on-robot operation, offline or LAN access, heavy local compute, or deterministic real-time loops. Confirm the choice in `plan.md`.

## Create and verify

- Read the [Python app workflow](https://github.com/pollen-robotics/reachy_mini/blob/main/skills/create-app.md), [app documentation](https://github.com/pollen-robotics/reachy_mini/blob/main/docs/source/SDK/apps.md), and [Python SDK reference](https://github.com/pollen-robotics/reachy_mini/blob/main/docs/source/SDK/python-sdk.md). Inspect the relevant examples before implementation.
- Use `reachy-mini-app-assistant` to create the app. Never create its app folders manually. The repository documents the assistant's CLI contract, not its implementation.
- If the assistant is unavailable, explain the prerequisite and pause or let the user choose JS/Web. If the command fails, surface the failure and ask the user to run it; do not work around the assistant by manually scaffolding.
- The upstream guide recommends `--publish` by default. This skill intentionally overrides that recommendation: never publish by default. For local work, use the assistant's local-only path. Only use publishing options after the user requests deployment and confirms the destination and visibility.
- Use the documented SDK APIs and examples. Prefer `goto_target()` for interpolated movement; use `set_target()` for high-frequency control. Follow the SDK's coordinate and safety-limit guidance.
- Run the assistant's documented validation and appropriate local app checks. Ask before starting a daemon; use simulation by default. Physical testing requires explicit authorization.
- A Python app may include a `static/` web UI. Keep app work distinct from SDK/daemon development.

## Canonical sources

- [Python app workflow](https://github.com/pollen-robotics/reachy_mini/blob/main/skills/create-app.md)
- [Python app documentation](https://github.com/pollen-robotics/reachy_mini/blob/main/docs/source/SDK/apps.md)
- [Python SDK reference](https://github.com/pollen-robotics/reachy_mini/blob/main/docs/source/SDK/python-sdk.md)
- [Core concepts and safety limits](https://github.com/pollen-robotics/reachy_mini/blob/main/docs/source/SDK/core-concept.md)
- [App testing](https://github.com/pollen-robotics/reachy_mini/blob/main/skills/testing-apps.md)

Reviewed 2026-11-16; source snapshot at commit `0f21887aad6dfed44dd2d6a7c6f2a7ede84c7360`.
