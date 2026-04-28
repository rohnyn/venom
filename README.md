# Mobile Play

Working repo for exploring an AI-native mobile OS.

## Current thesis

We are building a mobile OS where the primary abstraction is not apps alone, but a persistent personal operator that can observe, remember, decide, and act across the device under user-defined policy.

The near-term design problem is how to bridge:

- today's app-first phone UX
- tomorrow's operator-first model

without breaking the habits and trust model users already expect from mobile.

## Read this first

- [docs/vision.md](/Users/james/mobile-play/docs/vision.md)
- [docs/thesis.md](/Users/james/mobile-play/docs/thesis.md)
- [docs/ux-transition.md](/Users/james/mobile-play/docs/ux-transition.md)
- [docs/architecture.md](/Users/james/mobile-play/docs/architecture.md)
- [docs/landscape.md](/Users/james/mobile-play/docs/landscape.md)

## Repo structure

- `docs/`: synthesized thinking and working docs
- `research/`: source index plus company/project notes
- `decisions/`: ADR-style decision records
- `notes/`: raw notes and meeting captures
- `diagrams/`: Mermaid source for system and product diagrams

## Current working beliefs

- The right long-term object is a persistent personal operator, not a chatbot app.
- The OS should own memory, policy, capability brokering, audit, and delegation.
- Apps remain the compatibility layer even if the operator becomes the primary control plane.
- Trust depends on bounded autonomy, explicit policy, and reversible actions.
- The market is crowded at the assistant layer but still open at the user-owned OS-native layer.
