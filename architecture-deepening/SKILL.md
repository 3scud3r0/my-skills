---
name: architecture-deepening
description: Find architectural improvements that strengthen boundaries, invariants, testability, extensibility, and agent navigability. Use when modules are tightly coupled, responsibilities drift, or important behavior is hard to reason about. Do not use as an excuse for speculative rewrites.
---

# Architecture Deepening

## Objective
Improve the system's ability to preserve important rules while making future change cheaper and safer.

## Investigate first
- Identify domain concepts and the files that currently own them.
- Find duplicated policy, implicit global state, cyclic dependencies, hidden side effects and unstable interfaces.
- Identify invariants that are enforced in multiple places or nowhere.
- Trace the cost of testing one behavior in isolation.
- Inspect architecture decisions and neighboring conventions before proposing a new pattern.

## Prefer changes that
- give each invariant a clear owner;
- move unstable details behind stable interfaces;
- separate policy from mechanism;
- make state transitions explicit;
- reduce cross-layer knowledge;
- make important paths directly testable;
- improve discoverability for humans and agents.

## Reject
- “clean architecture” by diagram alone;
- extra abstractions without a concrete pressure;
- large rewrites where an incremental seam is available;
- changing architecture and product behavior simultaneously unless unavoidable.

## Deliverable
For each proposal: current pain, evidence, proposed boundary, migration path, verification strategy, compatibility risk and expected payoff.
