---
name: dependency-source-audit
description: Inspect the actual source and version of an important dependency when behavior, performance, compatibility, or security cannot be established from public API documentation alone. Do not clone dependencies for routine usage questions.
---

# Dependency Source Audit

## Trigger
Use when:
- observed behavior contradicts docs;
- an undocumented edge case matters;
- performance depends on internal allocation/scheduling;
- a security boundary depends on implementation details;
- version-specific behavior matters;
- integration requires matching private conventions or wire formats.

## Procedure
1. Pin the exact dependency name, version/commit and transitive path by which it enters the project.
2. Prefer the authoritative upstream repository and corresponding tag/commit.
3. Inspect only relevant internal call paths first.
4. Trace from the public API into the implementation until the disputed behavior is explained.
5. Check tests and changelog around that behavior.
6. Record whether the conclusion is API-guaranteed or merely current implementation behavior.
7. Avoid modifying vendored/upstream code unless that is the explicit task.

## Output
State exact version, relevant source path, mechanism, compatibility implications, and what could change in a future release.
