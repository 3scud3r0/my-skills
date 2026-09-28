---
name: claim-calibration
description: Audit README, documentation, reports, release notes, demos, and technical explanations so claims do not exceed the evidence. Use especially for ambitious AI, scientific, simulation, performance, security, or production-readiness statements.
---

# Claim Calibration

## Maturity ladder
Do not collapse these levels:
1. **designed** — architecture or plan exists;
2. **implemented** — code path exists;
3. **executed** — code ran in at least one environment;
4. **tested** — defined cases pass;
5. **benchmarked** — measured under a disclosed protocol;
6. **externally validated** — compared against independent reference/data;
7. **production-hardened** — operated under real reliability/security load;
8. **scientifically established** — supported by appropriate replicated empirical evidence.

## Audit each strong statement
Ask:
- What exact evidence supports this wording?
- Is the evidence direct or inferred?
- Does it establish existence, correctness, performance, causality, generality or only one example?
- Is the population/environment stated?
- What known limitation would change a reasonable reader's interpretation?

Replace absolute words only when evidence requires narrower wording. Preserve ambition; remove false certainty.

## Special rules
- “CI green” ≠ production readiness.
- “Unit tests pass” ≠ scientific validation.
- “High accuracy” ≠ clinically useful.
- “Uses causal testing” ≠ causal discovery established.
- “Runs locally” ≠ efficient on representative hardware.
- “Deterministic” requires controlled sources of nondeterminism.

## Output
Return calibrated wording plus the missing evidence needed to justify the stronger version.
