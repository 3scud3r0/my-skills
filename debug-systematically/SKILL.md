---
name: debug-systematically
description: Diagnose reproducible or intermittent failures through controlled experiments and root-cause analysis. Use when behavior is wrong or unexplained. Do not start with broad rewrites or speculative fixes.
---

# Debug Systematically

1. **Reproduce.** Capture the smallest known failing input, environment, logs, versions and frequency.
2. **Define expected behavior.** Separate specification from assumption.
3. **Localize.** Trace data/state until the first point where actual diverges from expected.
4. **Hypothesize.** Write concrete falsifiable causes; rank by evidence, not familiarity.
5. **Experiment.** Change one relevant variable at a time. Instrument instead of guessing.
6. **Fix the cause.** Avoid suppressing the visible symptom unless containment is explicitly temporary.
7. **Regress.** Add a test that fails before the fix and passes after it.
8. **Broaden carefully.** Search for the same defect class in neighboring paths only after the mechanism is understood.

## Intermittent/concurrent bugs
Record timing, seed, thread/task ordering, retries, timeouts and shared state. Seek a deterministic reproducer or stress harness.

## Stop conditions
Do not claim root cause when the proposed mechanism does not explain all known observations.
