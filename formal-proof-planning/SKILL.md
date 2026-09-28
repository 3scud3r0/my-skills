---
name: formal-proof-planning
description: Plan and structure machine-checked proofs in Lean/Mathlib or similar systems by making assumptions, theorem scope, reusable lemmas, domains, and the gap between computation and proof explicit. Use when a universal mathematical claim needs formal verification.
---

# Formal Proof Planning

## Start from the theorem
Write the intended proposition with explicit quantifiers, types, hypotheses and domain restrictions before trying tactics.

## Decompose
1. Normalize definitions and notation.
2. Identify existing library theorems before reproving fundamentals.
3. Split the target into reusable lemmas with clear mathematical meaning.
4. Isolate side conditions: nonzero denominators, positivity, finite bounds, continuity, measurability, etc.
5. Decide which parts are definitional reduction, algebraic normalization, decision procedure, rewriting, induction or domain-specific reasoning.

## Proof hygiene
- Prefer stable lemmas over brittle tactic scripts.
- Do not use a numeric instance proof as evidence for the universal theorem.
- Keep computational tests separate from formal proof.
- Record trusted axioms and noncomputable assumptions.
- Minimize custom axioms.

## Verification
Build from a clean environment with pinned Lean/Mathlib versions. Ensure the theorem, not merely an example file, is imported by the checked target.

## Output
Provide theorem statement, assumptions, lemma graph, relevant library search targets, proof strategy, unresolved obligations and what the final machine-checked result would establish.
