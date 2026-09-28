---
name: reflect
description: Review recent engineering/research sessions to find repeated friction, recurring checks, duplicated prompts, weak quality gates, and procedures that should become new or improved reusable skills.
---

# Reflect

Use after several substantial tasks, after a difficult incident, or when the same instructions keep being repeated.

## Inspect
Look for:
- repeated manual instructions;
- bugs caused by missing process steps;
- verification that was rediscovered from scratch;
- recurring project-specific domain checks;
- tools/scripts repeatedly invoked in the same order;
- skills that overlap or trigger too broadly;
- expensive skill behavior that rarely changes the result.

## Candidate test
A new skill is justified when the workflow is:
- repeated;
- non-trivial;
- error-prone or expensive when omitted;
- general enough to reuse;
- concrete enough to define triggers and completion criteria.

## Refactor the skill set
Prefer improving/merging an existing skill over adding a near-duplicate.
Delete obsolete rules.
Move deterministic repeated work into scripts only when that is safer and more reproducible.

## Output
Return:
1. candidate skill changes;
2. evidence from repeated workflow;
3. proposed trigger/non-trigger;
4. expected benefit;
5. whether to add, modify, merge or delete.
