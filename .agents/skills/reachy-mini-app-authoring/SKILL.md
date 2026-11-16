---
name: reachy-mini-app-authoring
description: Create, modify, debug, and locally verify Reachy Mini apps using the documented JavaScript/Web and Python workflows. Use for user-facing Reachy Mini apps, not SDK or daemon development.
---

# Reachy Mini App Authoring

Use this skill to route app work through the Reachy Mini project guidance. Read the relevant bundled reference before acting, and consult its linked upstream docs when available. Upstream documentation retrieved on 2026-11-16 was reviewed at commit `0f21887aad6dfed44dd2d6a7c6f2a7ede84c7360`; it may change.

See [GLOSSARY.md](GLOSSARY.md) for the terms used here.

## Scope

This skill covers creating, modifying, debugging, setting up, and locally verifying or launching Reachy Mini apps. It does not cover SDK or daemon engineering, CI, or releases.

Deployment guidance is in the language references, but deploy only when the user requests it. Before publishing, confirm the exact destination and visibility. Do not operate physical hardware without explicit authorization.

## Workflow

1. **Inspect local context.** Read `agents.local.md` in the app's working directory if it exists. If it is absent, Python work must follow [setup and testing](references/setup-and-testing.md); JS/Web work may skip full setup and should create a concise local note with known robot type and relevant preferences. Check for an existing app before choosing a creation workflow.
2. **Choose the app path.** JS/Web is the default; confirm the choice with the user in the plan. Prefer Python when requested or when the app needs unattended/on-robot operation, offline or LAN access, heavy local compute, or deterministic real-time loops. Do not force an existing app through a migration.
3. **Plan before changing the app.** Create `plan.md` in the app directory before implementation or scaffolding. Record the request, proposed app path and approach, setup/testing actions, any deployment or hardware actions, and clarifying questions with answer fields. Wait for answers and explicit plan approval before coding or scaffolding.
4. **Respect action boundaries.** Ask before installing missing tools, using the user's microphone, adding non-SDK npm dependencies, choosing a desktop-only UI, or using a server/Docker path. Confirm the permanent resource-folder location before cloning resources, and clone only what this app needs. Surface command failures; do not attempt complex or unapproved workarounds.
5. **Follow the matching workflow.** Use [JavaScript/Web](references/javascript.md) or [Python](references/python.md), plus [setup and testing](references/setup-and-testing.md) as needed.
6. **Verify the requested outcome.** Run the appropriate local checks and report what actually passed. A deployed-flow check is required only for a deployment task. Do not imply physical-hardware behavior was tested when it was not.

## Source precedence

The linked, current upstream docs are authoritative when accessible. If they conflict with a bundled reference or an explicit user constraint, call out the difference and honor the user's scope and authorization boundaries. If upstream docs are unavailable, use bundled guidance for stable workflow details and flag uncertainty before consequential actions.
