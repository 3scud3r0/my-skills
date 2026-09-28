---
name: multiagent-systems-audit
description: Audit multi-agent and tool-using AI systems for orchestration correctness, authority boundaries, prompt/data injection, loops, memory contamination, task routing, retries, RBAC, human approval, cost budgets, and failure containment.
---

# Multiagent Systems Audit

## Model the system
List:
- agent roles and who can create whom;
- tools and side effects;
- memory stores and write/read authority;
- channels and external services;
- task/workflow state machine;
- trust boundaries;
- escalation/human approval points.

## Authority
Apply least privilege. An agent's role text is not an authorization mechanism by itself. Verify enforcement in code at the tool/action boundary.

## Injection boundary
Treat user content, webpages, retrieved documents, tool output, agent messages and stored memory as untrusted data unless explicitly trusted by design.

## Loop safety
Every autonomous loop needs:
- objective;
- measurable stop condition;
- attempt/time/token/cost budget;
- failure classification;
- escalation path;
- cancellation;
- idempotency or transaction strategy for side effects.

## Memory
Check provenance, stale/conflicting facts, deletion/retention, cross-user isolation and whether one compromised observation can become durable instruction.

## Evaluation
Test partial failures: tool timeout, duplicate delivery, malformed result, permission denial, agent crash, retry storm and conflicting agents.

## Output
Report authority graph, failure modes, exploit paths, observability gaps and containment changes.
