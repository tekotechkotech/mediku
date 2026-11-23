# Mediku

**Working product name:** Mediku  
**Product category:** Gamified clinical learning platform for medical students  
**Status:** Product discovery and design foundation

Mediku helps clinical-year medical students turn clinical exposure into deeper understanding and stronger clinical reasoning through short, interactive, case-based learning experiences.

> The hospital gives students clinical exposure. Mediku turns that exposure into deeper understanding and stronger clinical reasoning.

## Start here

1. [Product brief](docs/product/product-brief.md)
2. [UI/UX design direction](docs/ui-ux/design-direction.md)
3. [Design system foundation](docs/ui-ux/design-system.md)
4. [Information architecture and user flows](docs/ui-ux/information-architecture.md)
5. [Technology stack](docs/architecture/tech-stack.md)
6. [Agent instructions](AGENTS.md)
7. [Visual reference](docs/assets/references/home-mobile-concept.svg)

## Current decisions

- **Backend:** Laravel.
- **Database:** MariaDB.
- **Frontend interaction/navigation:** Turbo (assuming Hotwire Turbo); confirm exact package and integration approach before implementation.
- Mobile-first responsive web app / PWA direction.
- Playful, friendly, modern, polished visual language; playful but not childish.
- Four primary navigation areas: Home, Campaign, Learn, Progress.
- MVP learning experiences: Clinical Investigation, DOPS Simulator, Knowledge Challenge, Exam Arena.
- Anatomy, diagnostic interpretation, and emergency decision-making are content domains integrated into those experiences, not separate top-level modules.
- Initial learning campaigns: THT-KL (active campaign) and Anesthesiology (preparation campaign).
- Mediku is the current working brand name. Trademark, domain, app-store, and market-conflict checks are not yet complete.

## Repository principles

- Product and design decisions belong in documentation before implementation.
- Keep tasks small, independently verifiable, and linked to acceptance criteria.
- Do not invent clinical facts, references, or procedural guidance.
- Never use real patient-identifiable information in examples or fixtures.
