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
- Verify supported MariaDB version and Laravel driver compatibility when the environment is established.

## Code quality and architecture

- Apply SOLID principles pragmatically, not mechanically.
- Follow [Coding Standards](coding-standards.md).
- Keep code easy to navigate: predictable naming, cohesive responsibilities, explicit dependencies, and a traceable path from route to view, application logic, persistence, and tests.
- Prefer the simplest Laravel-native solution that keeps responsibilities clear.
- Avoid both monolithic controllers/models and excessive abstraction layers.

## Decisions intentionally left open

Do not assume or independently lock:
- Laravel and PHP versions.
- MariaDB version.
- Hotwire Turbo package and Laravel integration strategy.
- CSS framework and component library.
- Asset bundler/build tooling.
- Queue, cache, search, file storage, and realtime infrastructure.
- Hosting and deployment topology.
- Whether PWA install/offline capability is required for the first release.

## Implementation guardrails

1. Inspect the repository before scaffolding or installing dependencies.
2. Prefer Laravel conventions and server-side capabilities.
3. Keep the frontend progressively enhanced; essential flows should not depend on complex client-side state.
4. Use Turbo only where it improves navigation or partial updates.
5. Ensure forms, validation errors, redirects, browser history, loading states, and accessibility work correctly with Turbo.
6. Avoid duplicate sources of truth between server and client.
7. Record deviations from this stack in an architecture decision record before implementation.

“Turbo” means **Hotwire Turbo** (Drive, Frames, Streams). Correct this document before implementation if a different Turbo technology was intended.
