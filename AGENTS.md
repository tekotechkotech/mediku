# Agent Instructions — Mediku

These instructions apply to every AI coding agent and contributor working in this repository.

## 1. Read before acting

Before implementing a task, read:
- `README.md`
- `docs/product/product-brief.md`
- `docs/ui-ux/design-direction.md`
- `docs/ui-ux/design-system.md`
- `docs/ui-ux/information-architecture.md`
- The task specification and its acceptance criteria

If a task conflicts with an established decision, do not silently choose. Explain the conflict and request a product decision.

## 2. Product intent

Mediku is a gamified clinical learning platform for medical students, especially students in clinical rotations. It is not a hospital task manager, conventional LMS, patient-facing diagnostic product, or replacement for supervised clinical training.

Optimize for repeated practice, varied case exposure, safe mistakes, clinical reasoning, procedural conceptual practice, and exam readiness.

## 3. UX rules

- Mobile-first is mandatory. Design and implement the narrow viewport experience first, then enhance for tablet and desktop.
- Use the playful, friendly, modern, polished visual direction. Playful does not mean childish or visually noisy.
- Keep the experience low-friction and low-cognitive-load. Prefer one clear next action over large menus and dense dashboards.
- Keep primary navigation to four areas: Home, Campaign, Learn, Progress.
- AI assistance should be contextual within learning activities, not automatically a separate primary navigation item.
- Aim for no more than 2–3 interactions between Home and starting a learning activity.
- Support short learning sessions, typically 5–20 minutes.
- Save progress automatically where the feature requires it.
- Do not use guilt-inducing streak warnings, punitive hearts, or penalties for incorrect answers.
- Reward meaningful learning, not clicks or time spent alone.
- Use progressive disclosure. Do not expose every advanced control at once.
- Desktop is an expanded responsive experience, not a stretched mobile screen.

## 4. Visual system

- Use design tokens from `docs/ui-ux/design-system.md`; do not introduce arbitrary colors, spacing, radii, or shadows without a documented reason.
- Reuse existing components before creating new ones.
- Keep typography readable and hierarchy consistent.
- Illustrations should support comprehension or emotional tone, not obscure medical information.
- Avoid stereotypes in character design. The intended audience includes a female pilot user, but the product should feel inclusive and should not equate femininity with pink or childish styling.
- Medical illustrations and procedure depictions must be clinically reviewed before being presented as authoritative.

## 5. Medical safety and content integrity

- This is an educational simulation, not a diagnostic or treatment tool for real patients.
- Do not invent clinical recommendations, dosages, contraindications, references, or procedural steps.
- Clearly distinguish established facts, educational simplifications, recommendations, and uncertainty.
- Use curated, traceable sources with publication/update metadata for clinical content.
- Use synthetic or properly de-identified case data only.
- DOPS Simulator is practice support; it does not certify competence or replace supervised practice or official DOPS assessment.
- Include an appropriate educational-use disclaimer in relevant experiences.

## 6. Engineering behavior

- Inspect the existing codebase and conventions before editing.
- Do not assume a framework, library, directory structure, or architecture until verified in the repository.
- Keep changes scoped to the requested task.
- Do not add dependencies without explaining why they are needed.
- Preserve accessibility: semantic structure, keyboard support, visible focus, sufficient contrast, and touch-friendly controls.
- Handle loading, empty, error, success, and disabled states where relevant.
- Avoid duplicate components and one-off styling when a shared pattern is appropriate.
- Do not add mock data that could be mistaken for real clinical data.
- Never commit secrets, credentials, tokens, or patient-identifiable data.

## 7. Task execution protocol

For each task:
1. Read the task and linked product/design references.
2. Inspect relevant existing code and tests.
3. Summarize the intended change and affected areas.
4. Implement the smallest coherent change.
5. Run relevant tests, linting, type checks, and build commands available in the project.
6. Verify the mobile layout and responsive behavior.
7. Report files changed, checks run, results, known limitations, and any product decisions needed.

Do not claim a check passed unless it was actually run.

## 8. Definition of done

A UI task is complete only when:
- It matches the documented product intent and design direction.
- The mobile experience is usable and verified.
- Responsive behavior is considered for larger screens.
- Interactive states are implemented, not merely drawn.
- Accessibility basics are addressed.
- Relevant tests/checks have been run or explicitly reported as not available.
- Documentation is updated when a durable design or behavior decision changes.
