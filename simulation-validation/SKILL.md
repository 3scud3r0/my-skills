---
name: simulation-validation
description: Validate physical, numerical, geometric, or dynamical simulations using invariants, analytic reference cases, convergence checks, deterministic reproduction, and independent data where available.
---

# Simulation Validation

## Establish the model
Document:
- state variables and units;
- equations and approximations;
- coordinate/frame conventions;
- timestep/integrator;
- boundary/initial conditions;
- randomness and seeds;
- collision/contact rules;
- known omitted physics.

## Verification: did we solve the equations correctly?
Use:
- dimensional checks;
- exact/analytic cases;
- conserved quantities where applicable;
- monotonicity and symmetry properties;
- timestep/grid refinement;
- deterministic replay;
- regression snapshots/tolerances.

## Validation: are the equations adequate for reality?
When making real-world claims, compare outputs to independent experimental/reference data with uncertainty. Keep verification and validation separate.

## Real-time simulations
Test multiple frame rates and substep schedules. Detect instability hidden by one machine's timing.

## Graphics/game simulations
Arcade behavior is allowed but must be explicitly separated from physical modeling.

## Output
List validated regimes, failed regimes, numerical error bounds or tolerances, omitted effects and conditions where the model should not be trusted.
