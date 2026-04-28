# Architecture

## System shape

The AI layer should not live only as an app. It spans:

- user-facing surfaces
- framework APIs
- system services
- native runtimes
- hardware-facing capability layers

## Core subsystems

### Personal operator

Long-lived execution runtime that can observe, decide, act, and report.

### Memory layer

Stores:

- preferences
- routines
- history
- semantic recall
- task state

### Policy engine

Defines what may happen:

- silently
- with confirmation
- never

### Capability broker

Mediates access to:

- apps
- notifications
- messaging
- files
- sensors
- camera and mic
- location
- settings and system services

### Model router

Chooses among:

- local models
- cloud models
- specialized models
- fallback strategies

### Audit and replay

Every meaningful action should be:

- logged
- attributable
- reviewable
- reversible where possible

### Extension sandbox

Lets third parties add capabilities without giving them unconstrained system power.

## AOSP placement

The OS-native AI layer likely spans:

- framework APIs
- System Server services
- native indexing and inference components
- UI surfaces such as lock screen, voice, overlays, and share actions

## Related diagrams

- [aosp-stack.mmd](/Users/james/mobile-play/diagrams/aosp-stack.mmd)
- [operator-layer.mmd](/Users/james/mobile-play/diagrams/operator-layer.mmd)
- [app-control-boundaries.mmd](/Users/james/mobile-play/diagrams/app-control-boundaries.mmd)
