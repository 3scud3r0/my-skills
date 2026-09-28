---
name: scientific-validation
description: Evaluate scientific or research claims by separating hypothesis, model, measurement, statistical evidence, causality, external validation, and uncertainty. Use for research prototypes, physics-informed systems, causal claims, medical/biological work, or discovery systems.
---

# Scientific Validation

## Separate layers
Never merge:
- hypothesis;
- mathematical/computational model;
- implementation;
- synthetic experiment;
- observational data;
- intervention/causal evidence;
- external validation;
- replicated scientific conclusion.

## Protocol
1. Write the hypothesis before interpreting results.
2. Define measurable outcomes and falsification criteria.
3. Identify confounders, selection effects and data-generating assumptions.
4. Establish an appropriate baseline/null model.
5. Use a held-out or prospective evaluation when retrospective fitting can bias the result.
6. Quantify uncertainty and sample/population limits.
7. Compare against independent references or measurements.
8. Record negative and inconclusive results, not only successes.

## Causality
Correlation, predictive accuracy, counterfactual simulation and true intervention are different evidence classes. State which one exists.

## Scientific software
A correct implementation of an equation validates the implementation against that equation; it does not validate the equation against nature.

## Output
For every major conclusion: evidence class, protocol, population, uncertainty, competing explanations, limitations and next experiment needed.
