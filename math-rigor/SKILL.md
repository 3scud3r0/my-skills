---
name: math-rigor
description: Audit mathematical formulas, algorithms, derivations, assumptions, domains, units, numerical stability, and edge cases. Use whenever correctness depends on mathematics rather than syntax alone.
---

# Math Rigor

## Contract
A formula is not accepted because it looks familiar or produces plausible numbers.

## Check in order
1. **Definitions.** Every symbol, variable, coordinate system, convention and unit must be explicit.
2. **Domain.** Record conditions such as nonzero denominators, positivity, continuity, valid ranges and boundary conditions.
3. **Dimensions.** For physical quantities, verify dimensional consistency before numerical testing.
4. **Derivation.** Reconstruct the transformation or cite the exact theorem/identity used.
5. **Special cases.** Test zeros, signs, extrema, singularities, degenerate geometry and limiting behavior.
6. **Numerics.** Examine cancellation, overflow/underflow, conditioning, discretization error, precision and tolerance choice.
7. **Independent check.** Compare against a second derivation, symbolic tool, exact arithmetic, trusted reference or analytic case when stakes justify it.

## Formal proof
Distinguish:
- example verification;
- property-based evidence;
- symbolic simplification under assumptions;
- machine-checked formal proof.

Never describe a finite set of examples as a universal proof.

## Output
State assumptions, derivation/evidence, counterexamples searched, numerical limitations and confidence boundaries.
