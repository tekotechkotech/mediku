# Coding Standards — Mediku

These standards keep the codebase clean, consistent, easy to navigate, and maintainable by humans and AI agents.

## 1. Core principles

- **Clarity over cleverness:** prefer straightforward code.
- **Consistency over personal preference:** follow repository conventions.
- **Cohesion over fragmentation:** one clear responsibility per class/module, without splitting trivial logic into many files.
- **Explicit over implicit:** make dependencies, side effects, and business rules easy to identify.
- **Traceability:** make it possible to follow a feature from route to response, view, application logic, persistence, and tests.
- **Pragmatic SOLID:** use the principles to solve real coupling and maintenance problems; do not create an interface for every class.

## 2. SOLID in practice

### S — Single Responsibility Principle
- Give each class/module one cohesive reason to change.
- Controllers handle HTTP concerns: request input, authorization coordination, invoking an application operation, and returning a response.
- Application Actions/Use Cases coordinate a meaningful user operation.
- Domain services hold business rules that do not naturally belong to one entity/value object.
- Models represent persistence and cohesive model behavior; do not turn them into unrelated workflow containers.
- Blade views render presentation; they do not contain business workflows or database queries.

### O — Open/Closed Principle
- Extend behavior through composition, policies, strategies, or events when variation is real.
- Avoid giant conditional blocks when new variants are expected.
- Do not build generic extension systems for hypothetical requirements.

### L — Liskov Substitution Principle
- Subtypes and implementations must honor the contracts of their parent type/interface.
- Do not use inheritance merely to share a few lines; prefer composition when substitutability is not real.

### I — Interface Segregation Principle
- Keep interfaces small and specific to their consumers.
- Do not force implementations to provide methods they do not need.
- Avoid broad catch-all interfaces.

### D — Dependency Inversion Principle
- Keep high-level business rules independent from volatile infrastructure when that separation provides real value.
- Use constructor injection for genuine dependencies.
- Introduce interfaces at boundaries that need substitution, isolation, or independent testing; avoid interfaces that merely mirror a concrete class.

## 3. Recommended Laravel responsibility flow

Use this as a guide, not a mandatory architecture for every endpoint:

```text
Route
  -> Middleware / Policy / Form Request
  -> Controller (HTTP orchestration)
  -> Action / Use Case (application workflow)
  -> Domain rule / Service (when needed)
  -> Eloquent Model / Query (persistence)
  -> Resource / View Model / Blade View (response)
```

For simple CRUD, a controller may use Eloquent directly if the logic remains small and clear. Do not add an Action class just to wrap one trivial query.

For multi-step operations—such as submitting a case attempt, evaluating an answer, updating mastery, and awarding XP—use a clearly named Action/Use Case and a database transaction when atomic consistency is required.

## 4. Laravel conventions

- Follow Laravel conventions for routes, controllers, Form Requests, Policies, migrations, models, jobs, events, and tests.
- Keep route files declarative. Use named routes and route model binding where appropriate.
- Use Form Requests when validation is non-trivial or reused.
- Put authorization in Policies/Gates or another clear authorization boundary, not only in view conditions.
- Use transactions for multi-write operations that must succeed or fail together.
- Use Eloquent relationships/scopes for reusable queries; prevent hidden expensive queries and N+1 behavior.
- Add query classes only when complexity or reuse justifies them.
- Use Jobs for work that should be queued, not as a generic wrapper for every operation.
- Keep configuration in config files and environment-specific values in environment variables. Never hardcode secrets.

## 5. Naming and code navigation

- Name classes by business intent: `SubmitCaseAttempt`, `CalculateTopicMastery`, `AwardLearningXp`; avoid vague names such as `Helper`, `Manager`, or `Processor`.
- Keep file names and namespaces aligned with class names and responsibilities.
- Start with Laravel's conventional structure. Introduce feature/domain grouping only when it improves discoverability at the project's actual scale.
- Avoid unexplained abbreviations.
- Keep methods focused. Extract methods when the name clarifies a distinct operation, not merely to reduce line count.
- Avoid ambiguous boolean parameters; use explicit methods/options where appropriate.
- Keep public APIs and method signatures intentional.

## 6. Data and database discipline

- Use migrations for schema changes.
- Name tables, columns, indexes, and foreign keys consistently.
- Add database constraints for invariants that must hold regardless of application code.
- Store canonical data once; duplicate state only for documented performance or historical reasons.
- Be explicit about units, time zones, precision, and nullable values.
- Use factories/seeders for synthetic development and test data only. Never seed real patient data.

## 7. Testing

- Test behavior and business outcomes, not private implementation details.
- Unit-test isolated domain rules when they have meaningful complexity.
- Feature-test HTTP behavior, authorization, validation, persistence, and important workflows.
- Cover edge cases, failure paths, and transaction behavior for critical operations.
- Name tests so the behavior they protect is obvious.
- Do not mock everything; use real framework/database behavior where practical.

## 8. Frontend and Turbo

- Keep Blade templates focused on semantic markup and presentation.
- Extract reusable Blade components when a pattern is repeated or has a meaningful contract.
- Use Turbo Drive, Frames, and Streams only where they simplify navigation or partial updates.
- Preserve standard form behavior, validation, redirects, browser history, and accessibility.
- Keep JavaScript modules small and scoped to a specific interaction.
- Do not move business rules into JavaScript or rely on client-side validation as the only validation.
- Avoid frontend state-management layers unless demonstrated complexity requires them.

## 9. Refactoring and dependencies

- Avoid unrelated large refactors in scoped feature work.
- Refactor when it reduces real duplication, coupling, or cognitive load.
- Add dependencies only when native Laravel/PHP/browser capabilities are insufficient or the dependency provides clear value.
- Explain architectural trade-offs in the implementation summary.
- Update documentation when a durable convention or architecture decision changes.

## 10. Review checklist

- Can another developer locate the entry point quickly?
- Is each class responsible for one cohesive concern?
- Are dependencies explicit and limited?
- Is there unnecessary abstraction or indirection?
- Are business rules testable outside the HTTP presentation layer?
- Can the feature's data flow be traced?
- Are names and file placement predictable?
- Are important edge cases and authorization rules tested?
- Does the implementation follow the documented Laravel/Turbo stack?
