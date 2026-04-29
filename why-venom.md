# Why Venom Exists

This repo raises a fair question:

> "Couldn't OpenClaw already do this?"

Short answer:

- OpenClaw runs assistants.
- Venom forms, governs, and preserves a user-owned symbiote.

The difference is architectural, not cosmetic.

## The few differences that actually matter

### 1. OpenClaw is built around the wrong native objects

OpenClaw is built around:

- `agent`
- `workspace`
- `session`
- `channel account`
- `binding`

OpenClaw's own multi-agent model defines an agent as its own workspace, state directory, auth profiles, and session store.

Venom needs different native objects:

- `symbiote`
- `ideas`
- `self-model`
- `rules`
- `trust graph`
- `representation modes`
- `activity ledger`

Venom needs to store, route, and reason around those directly.

If they only exist as prompt text, markdown files, or plugin-owned metadata inside OpenClaw, they are not first-class. They are conventions layered on top of an assistant runtime.

### 2. OpenClaw's extension surface is too narrow

OpenClaw's core plugin kinds are:

- `memory`
- `context-engine`

Its main plugin slots are also exclusive:

- one active `plugins.slots.memory`
- one active `plugins.slots.contextEngine`

That tells you where OpenClaw expects customization to happen:

- retrieval
- memory behavior
- prompt assembly
- compaction
- some runtime hooks

That is enough to change how an assistant behaves.
It is not enough to replace the system's routing and storage model.

A context engine can decide what goes into a run.
A memory plugin can change recall behavior.
Neither one turns `symbiote`, `ideas`, `trust graph`, or `activity ledger` into gateway-level objects.

That is why Venom is not a normal OpenClaw plugin or extension.

### 3. OpenClaw persists continuity as gateway-owned sessions

OpenClaw is explicit about this: all session state is owned by the gateway and stored per agent under `~/.openclaw/agents/<agentId>/sessions`.

That means the thing OpenClaw naturally persists is a session:

- session keys
- session transcripts
- session lifecycle
- per-agent workspace state

That is the right model for assistant conversations.

It is the wrong model for Venom if live ideas and evolving relationships need to exist as first-class objects rather than being emulated through sessions, files, and conventions.

In OpenClaw, those things would be emulated through sessions, files, and conventions.
In Venom, they need to be native.

### 4. OpenClaw scales by adding more isolated agents

OpenClaw's multi-agent model is also explicit: each agent gets its own isolated workspace, auth, and session history.

That is the right move for multiple assistants, personas, or people.

Venom wants one symbiote that can appear across many surfaces and contexts while keeping one deeper identity model.

OpenClaw's native move is another agent.
Venom's native move is another embodiment of the same symbiote.

That is a real architectural difference.

## What this means

This is not "OpenClaw is weak."
It is "OpenClaw is centered on different primitives."

Could you build Venom as a deep OpenClaw fork?

Yes, but only by replacing more and more of what OpenClaw is centered on:

- its primary objects
- its session-first continuity model
- its isolated-agent scaling model

That is not a normal customization.
That is a new system wearing some OpenClaw parts.

## What OpenClaw can still be

OpenClaw can still be useful below Venom as an executor, worker, or embodiment on some surfaces.

It just should not be the system that defines the symbiote.
