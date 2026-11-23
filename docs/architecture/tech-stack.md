# Technology Stack — Mediku

**Status:** Initial stack decision  
**Decision date:** 2026-11-23

## Selected stack

| Layer | Technology | Decision |
|---|---|---|
| Backend / application framework | Laravel | Selected |
| Database | MariaDB | Selected |
| Frontend navigation and progressive enhancement | Turbo (Hotwire Turbo) | Selected direction; verify exact package/integration before implementation |

## Frontend approach

The current direction is a Laravel-rendered web application enhanced with Hotwire Turbo:
- Use Laravel routes, controllers, validation, authorization, and server-rendered Blade views as the default application foundation.
- Use Turbo Drive for faster page navigation without making the application a client-rendered SPA.
- Use Turbo Frames for independently navigable or replaceable page regions when they improve the interaction.
- Use Turbo Streams for server-driven partial updates when a feature genuinely needs them.
- Keep JavaScript focused on interactions that cannot be handled cleanly by standard HTML and Turbo.
- Do not introduce React, Vue, Inertia, or another SPA layer by default. A future exception requires a concrete product/technical reason and an explicit decision.

## Database

- MariaDB is the selected relational database.
- Use Laravel migrations as the source of truth for schema changes.
- Use Eloquent where it fits; use explicit queries for complex reporting or performance-sensitive operations when justified.
- Design indexes and constraints around real access patterns and data integrity.
- Verify the supported MariaDB version and Laravel database-driver compatibility when the project environment is established.

## Decisions intentionally left open

Do not assume or independently lock these choices:
- Laravel and PHP versions.
- MariaDB version.
- Hotwire Turbo package and Laravel integration strategy.
- CSS framework and component library.
- Asset bundler/build tooling.
- Queue, cache, search, file storage, and realtime infrastructure.
- Hosting and deployment topology.
- Whether a PWA install/offline capability is required for the first release.

## Implementation guardrails

1. Inspect the repository before scaffolding or installing dependencies. Preserve an existing working setup unless there is a documented reason to change it.
2. Prefer Laravel's conventional structure and server-side capabilities.
3. Keep the frontend progressively enhanced: core navigation and essential learning flows should remain robust without relying on complex client-side state.
4. Use Turbo only where it improves navigation or partial updates; do not force every interaction into a Turbo abstraction.
5. Ensure forms, validation errors, redirects, browser history, loading states, and accessibility work correctly with Turbo.
6. Avoid duplicate sources of truth between server state and client state.
7. Record any deviation from this stack in an architecture decision record before implementation.

## Important clarification

“Turbo” is recorded as **Hotwire Turbo** (Turbo Drive, Frames, and Streams). If the intended Turbo technology is different, correct this document before implementation.
