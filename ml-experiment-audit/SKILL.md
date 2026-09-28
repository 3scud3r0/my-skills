---
name: ml-experiment-audit
description: Audit machine-learning experiments for leakage, invalid splits, weak baselines, class imbalance, misleading metrics, calibration errors, overfitting, unreproducible training, and unsupported deployment claims.
---

# ML Experiment Audit

## Data first
Record dataset origin, license, unit of observation, labels, duplicates, missingness, preprocessing and known biases.

Check for leakage through:
- duplicate/near-duplicate samples across splits;
- subject/patient/entity overlap;
- preprocessing fitted on all data;
- temporal leakage;
- label-derived features;
- augmentation before splitting.

## Evaluation
- justify the split strategy;
- preserve a true final holdout when possible;
- include simple baselines;
- choose metrics based on actual error costs;
- show per-class precision/recall and confusion matrix for imbalanced classification;
- report uncertainty across seeds/folds when material;
- distinguish probability confidence from empirical calibration.

## Medical/high-stakes work
Do not translate benchmark accuracy into diagnostic utility without external clinical validation, representative cohorts, calibration, workflow analysis and appropriate oversight.

## Training
Pin seeds, code, data version, hyperparameters, library versions and hardware where reproducibility matters.

## Output
Separate what the experiment demonstrates from what would require a larger, external, prospective or domain-specific validation.
