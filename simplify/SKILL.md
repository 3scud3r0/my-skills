---
name: simplify
description: Reduce code complexity and cognitive load while preserving exact behavior. Use after behavior is understood and verified. Do not simplify unknown or performance-critical code without evidence.
---

# Simplify

Optimize for comprehension, not line count.

Before each change ask:
- same inputs and outputs?
- same side effects and ordering?
- same errors and edge cases?
- same numerical precision?
- same performance constraints that matter?
- same public/API compatibility?

Prefer:
- clear names over clever expressions;
- explicit control flow over dense nesting;
- one owner for an invariant;
- smaller coherent interfaces;
- removal of duplicated policy;
- project conventions over personal style.

Do not:
- inline away meaningful concepts;
- merge unrelated responsibilities;
- remove abstractions that preserve testability or isolation;
- rewrite working subsystems merely for aesthetic consistency.

Run the relevant evidence path after simplification. If proving equivalence is expensive, reduce the scope.
