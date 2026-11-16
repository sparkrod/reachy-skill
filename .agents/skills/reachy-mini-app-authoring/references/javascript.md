# JavaScript/Web Apps

Choose this path by default for a new app, especially a shareable browser app or UI. Confirm the language choice in `plan.md`. For existing apps, preserve the working architecture unless the user approves a migration.

## Build and verify locally

- Start with the project's [JS app workflow](https://github.com/pollen-robotics/reachy_mini/blob/main/skills/create-js-app.md) and its [single-source app creation guide](https://github.com/pollen-robotics/reachy_mini/blob/main/ts/APP_CREATION_GUIDE.md). Use those docs for scaffolding, host integration, SDK version, and current deployment metadata.
- The default new-app path is TypeScript + Vite. A simple bare HTML/CDN app or a server/Docker app has different tradeoffs; ask before using a server/Docker path.
- Use the Reachy host shell for authentication, robot selection, and session lifecycle. Do not implement those flows yourself or use private SDK internals.
- Register the documented safe return behavior on leave. Validate external configuration before use, mirror the host theme, and use a mobile-first UI unless the user approves otherwise.
- Ask before enabling the user's microphone or adding npm dependencies beyond the Reachy SDK.
- Use public SDK APIs. Follow the current animation and lifecycle guidance for gestures, continuous loops, media, and teardown.
- Keep secrets out of source control. For local token-based development, use the documented ignored `.env.local` workflow and never commit tokens.
- Run the documented local build and relevant lifecycle/mobile checks. Do not claim the hosted sign-in/picker/app flow passed unless the user requested deployment and that flow was actually verified.

## Deploy only on request

Deployment is optional and user-authorized only. If requested, explain the target and visibility, get final confirmation before publishing, then follow the upstream deployment guide and verify the hosted flow. Do not push source, create a public Space, or publish artifacts without that confirmation.

## Canonical sources

- [JS app workflow](https://github.com/pollen-robotics/reachy_mini/blob/main/skills/create-js-app.md)
- [App Creation Guide](https://github.com/pollen-robotics/reachy_mini/blob/main/ts/APP_CREATION_GUIDE.md)
- [JavaScript SDK reference](https://github.com/pollen-robotics/reachy_mini/blob/main/docs/source/SDK/javascript-sdk.md)

Reviewed 2026-11-16; source snapshot at commit `0f21887aad6dfed44dd2d6a7c6f2a7ede84c7360`.
