---
name: benchmark-design
description: Design fair, reproducible benchmarks for algorithms, models, rendering paths, agent workflows, or system implementations. Use before publishing comparative performance or quality claims.
---

# Benchmark Design

## Define the question
A benchmark must answer one narrow comparison question. State:
- metric;
- population/workload;
- hardware/software environment;
- controlled variables;
- allowed tuning;
- failure/timeout policy.

## Protocol
- pin versions and configuration;
- isolate warmup from measurement;
- use deterministic seeds where meaningful;
- repeat enough times to expose variance;
- record raw results, not only aggregates;
- include correctness/quality gates before comparing speed;
- use representative and adversarial workloads;
- avoid choosing cases after seeing results.

## ML/agent benchmarks
Separate model quality, token/cost usage, latency and failure rate. Do not combine them into a custom score without documenting the formula and sensitivity.

## Rendering/system benchmarks
Measure realistic frame or workload distributions, not only synthetic best cases.

## Report
Publish commands/config, environment, sample count, aggregation method, variance/error bars when useful, exclusions and known sources of bias.

A ranking is valid only for the tested protocol and population.
