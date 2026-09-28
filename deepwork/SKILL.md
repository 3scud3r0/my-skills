---
name: deepwork
description: Orchestrate large, risky, multi-phase work with dependencies, persistent state, explicit gates, and adversarial review. Do not activate merely because multiple files change.
---

# Deepwork

Use only for architectural migrations, cross-cutting changes, complex GPU/ML/system work, unsafe-to-partially-ship changes, or tasks requiring several dependent phases.

## Contract
When active, manage the work as an orchestrator rather than immediately editing everything.

Maintain local task state in an ignored file such as:
```text
.agent/deepwork/<task>.md
```

Track:
- goal and non-goals;
- verified repository facts;
- assumptions and unresolved questions;
- phases and dependencies;
- important decisions and rejected alternatives;
- verification evidence;
- risks and rollback points.

## Execution
1. Map the system before planning.
2. Split work into independently verifiable phases.
3. Define a success claim and evidence path for each phase.
4. Implement one dependency layer at a time.
5. Re-run affected verification after each material change.
6. Use an adversarial review before declaring a phase complete.
7. Stop scope creep: defer unrelated improvements.

## Do not use
Typos, localized bugs, small refactors, straightforward documentation, or routine features with obvious verification.
