---
name: reproducible-research
description: Turn computational experiments, numerical studies, benchmarks, and research prototypes into re-runnable, auditable artifacts with pinned inputs, code, environment, configuration, seeds, and result provenance.
---

# Reproducible Research

A result without a reproducible provenance chain is an observation, not a durable artifact.

## Capture
- exact source commit;
- dataset/input identifiers and hashes;
- preprocessing/transformation versions;
- environment and dependency versions;
- hardware when it affects results;
- configuration/hyperparameters;
- random seeds and nondeterminism;
- exact command;
- output files and checksums;
- timestamp and relevant external service versions.

## Separate
Keep raw inputs immutable where possible. Distinguish:
raw → cleaned → transformed → trained/simulated → analyzed → published.

## Re-run
Provide one documented entry point that can recreate the important result or explicitly state which external dependencies prevent full reproduction.

## Results
Store machine-readable outputs in addition to screenshots/plots. A plot is a view of data, not the source of truth.

## Drift
When external data, APIs or models can change, pin snapshots or record immutable identifiers.

## Output
A third party should be able to determine exactly what produced a result, rerun it within documented limits, and detect if inputs changed.
