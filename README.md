# Architecture Decision Records

A small, reusable starter kit for recording software architecture decisions. ADRs preserve the context behind a choice so future contributors can understand what was considered and when a decision should be revisited.

## Using this kit

1. Copy `template.md` for each significant decision and name it `NNNN-short-title.md` (for example, `0001-modular-monolith.md`).
2. Write the context and constraints before describing the decision.
3. Record realistic alternatives and consequences, including trade-offs.
4. Mark the ADR `Proposed`, `Accepted`, `Superseded`, or `Deprecated`; link a newer ADR when replacing one.

## Template

Create a file named `template.md` with this content:

```markdown
# NNNN. Decision title

- Status: Proposed
- Date: YYYY-MM-DD

## Context
What problem are we solving? Include relevant constraints.

## Decision
What are we choosing, and why?

## Alternatives considered
- Option A — benefits and drawbacks
- Option B — benefits and drawbacks

## Consequences
What becomes easier or harder? Include operational and migration costs.
```

## Example: start with a modular monolith

**Status:** Accepted

**Context:** A small team needs to ship a product quickly, and the domain boundaries are still changing. There is no demonstrated need for independent deployment or scaling.

**Decision:** Keep the application in one deployable unit, with modules organized around business capabilities and explicit interfaces between them.

**Consequences:** Local development and deployment stay simple; module boundaries can evolve. Teams must enforce those boundaries, and a future extraction into services will require additional operational work.

## Contributing

Open an issue or pull request with improvements, examples, or translations. Keep templates technology-neutral and explain trade-offs rather than presenting one architecture as universally best.