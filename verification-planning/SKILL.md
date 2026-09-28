---
name: verification-planning
description: Design a project-specific evidence path before non-trivial implementation. Use for features, bug fixes, refactors, simulations, ML changes, integrations, or behavior claims that need credible proof.
---

# Verification Planning

## Frame the claim
State exactly what must become true, what must remain true, and what observation would falsify success.

## Build the evidence path
Derive verification from the system:
- controllable inputs;
- observable outputs/state;
- invariants;
- boundaries crossed;
- repeatability/reset capability;
- meaningful failure modes.

Generate at least one cheap path and, when stakes justify it, one stronger independent path.

## Evidence hierarchy
Prefer the most direct feasible evidence:
1. deterministic unit/property test;
2. integration test across the real boundary;
3. numerical/reference comparison;
4. browser/GPU/runtime proof;
5. reproducible benchmark;
6. independent external validation;
7. manual observation only when automation cannot establish the claim.

A green generic test suite is evidence only for what those tests cover.

## Verification affordance
If decisive state is invisible, add the smallest temporary or durable affordance that makes it observable and diagnosable.

## Final report
For each claim record:
- claim;
- evidence executed;
- result;
- limitations;
- remaining uncertainty.

Never convert “tests passed” into a broader claim than the tests establish.
