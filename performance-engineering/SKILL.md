---
name: performance-engineering
description: Optimize latency, throughput, CPU, GPU, memory, I/O, startup, or frame time using measurement-driven experiments. Use when performance is a requirement or measured problem. Do not optimize based on intuition alone.
---

# Performance Engineering

## Rule zero
No optimization without a baseline.

## Workflow
1. Define the user-visible metric and target: frame time, p95 latency, throughput, memory peak, VRAM, startup, package size, power/thermal envelope.
2. Reproduce under controlled hardware/software/configuration.
3. Profile to locate the dominant bottleneck.
4. Form one mechanism-based hypothesis.
5. Change the smallest thing that tests that hypothesis.
6. Re-measure with the same benchmark.
7. Check correctness and quality regressions.
8. Keep the change only if improvement is material and repeatable.

## GPU work
Separate CPU submission time, GPU pass time, synchronization stalls, bandwidth, occupancy/resource pressure, shader cost, upload cost and allocation churn.

## Statistics
Use warmups and repeated samples. Report median and tail behavior where relevant. Avoid one-shot timings.

## Anti-patterns
- micro-optimizing cold code;
- trading correctness for benchmark score without saying so;
- changing benchmark and implementation together;
- claiming percentage gains from incomparable runs;
- ignoring startup, memory or worst-case behavior while optimizing average throughput.

## Deliverable
Baseline, environment, profiler evidence, change, after measurement, variance, trade-offs and remaining bottleneck.
