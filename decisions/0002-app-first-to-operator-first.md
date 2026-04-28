# ADR 0002: Preserve Familiar UX While Building Operator Substrate

## Status

Accepted

## Context

The long-term product abstraction is a persistent personal operator. However, current mobile users still think and behave through app-centric workflows, and current models still need bounded authority.

## Decision

The product should preserve familiar mobile surfaces while building the operator substrate underneath them.

Stated another way:

- near term: app-first, operator-assisted
- long term: operator-first, app-backed

## Consequences

- the OS core should prioritize memory, policy, capability brokering, and audit
- familiar surfaces remain central to onboarding and trust
- the authority model can expand without forcing a radically new UX at the start
