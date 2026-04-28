# Security And Trust Model

## Core principle

The system only becomes valuable if users trust delegated action.

That means trust cannot be bolted on after the autonomy story is defined.

## Non-negotiables

- explicit capability boundaries
- least-privilege execution
- revocable permissions
- action-level audit logs
- strong separation between core system agents and third-party agents
- local-first treatment of sensitive data where possible

## Action policy tiers

### Silent

Routine, low-risk, reversible actions inside a declared policy envelope.

### Confirmed

Meaningful actions with user-visible impact that should require approval.

### Forbidden

Classes of actions outside declared trust, policy, or safety bounds.

## Product requirement

The user should always be able to answer:

- what did the operator do
- why did it do it
- what data did it use
- how do I stop it next time

## Open security questions

- How much power should third-party extensions get directly versus through brokering?
- How are enterprise or family policy layers represented without breaking the single-user trust model?
- What is the right default for local versus cloud execution on sensitive tasks?
