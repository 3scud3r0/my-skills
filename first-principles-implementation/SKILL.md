---
name: first-principles-implementation
description: Build a reduced system from fundamental mechanisms for learning, control, or architectural understanding instead of hiding the concept behind a high-level framework. Use for educational engines, runtimes, algorithms, renderers, ML internals, or systems research. Do not reinvent infrastructure when the task is ordinary product delivery.
---

# First-Principles Implementation

## Purpose
Rebuild enough of a system to expose the mechanism, not to imitate every production feature.

## Procedure
1. Define the phenomenon or abstraction to understand.
2. List the irreducible primitives required.
3. State what production concerns are intentionally omitted.
4. Implement the smallest end-to-end version with observable internal state.
5. Compare behavior against a known implementation/reference where possible.
6. Add experiments that reveal why each primitive exists.
7. Only then add optimization or abstraction layers.

## Examples
- allocator before memory framework;
- raster/compute pass before full rendering engine;
- tokenizer/attention component before orchestration framework;
- parser/interpreter core before language tooling;
- numerical integrator before flight/game polish.

## Guardrails
- Do not call the reduced implementation production-equivalent.
- Preserve references to standards/papers/known algorithms.
- Avoid replacing understanding with copied code.
- Keep correctness tests close to the primitive being taught.

## Completion
The implementation should make the hidden mechanism inspectable enough that a reader can explain, modify and experimentally break it.
