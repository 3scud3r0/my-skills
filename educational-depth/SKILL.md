---
name: educational-depth
description: Design technical learning material that builds genuine understanding from motivation and mental models through formalization, implementation, tests, laboratories, and integrative projects.
---

# Educational Depth

Use for courses, chapters, tutorials, labs and explanatory repositories.

## Learning sequence
Prefer:
```text
problem → motivation → intuition/model → precise definitions
→ formalization → minimal implementation → tests
→ experiment/lab → failure modes → integrative project
```

## Requirements
- Explain why a concept exists before presenting its interface.
- Derive important formulas or algorithms instead of only naming them.
- Include executable examples and observable failure cases.
- Separate pedagogical simplification from production implementation.
- Use tests to demonstrate invariants, not merely syntax.
- Connect each abstraction to at least one lower layer and one higher-level use.
- End major topics with a task that requires transfer, not repetition.

## Avoid
- encyclopedic dumping;
- code without a mental model;
- definitions that depend on undefined jargon;
- “magic” framework calls replacing the concept being taught;
- claiming completeness beyond the declared curriculum.

## Quality check
A learner should be able to predict behavior, explain trade-offs, implement a reduced version, debug a failure, and identify what the simplified model omits.
