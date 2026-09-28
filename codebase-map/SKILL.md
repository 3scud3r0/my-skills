---
name: codebase-map
description: Build a high-confidence map of an unfamiliar repository before non-trivial changes. Use when architecture, entry points, data flow, tests, build, or runtime behavior are not yet understood. Do not use for tiny isolated edits in already-familiar code.
---

# Codebase Map

## Objective
Create the minimum accurate model of the repository needed to modify it safely.

## Workflow
1. Read trusted project instructions, README, manifests, build files, CI and architecture docs.
2. Inventory languages, entry points, packages, generated code, persistence, external services and deployment surfaces.
3. Trace the main runtime path from input to observable output.
4. Identify module boundaries, shared state, concurrency, error paths and ownership of important invariants.
5. Locate tests by layer: unit, integration, end-to-end, numerical, browser, GPU, packaging.
6. Record which files are source-of-truth versus generated/build artifacts.
7. Produce a concise map: components, responsibilities, dependencies, data flow, risk zones, verification commands and unknowns.

## Rules
- Do not infer behavior from filenames alone.
- Distinguish current implementation from roadmap or aspirational docs.
- Prefer direct code evidence when docs and code disagree.
- Do not read the entire repository indiscriminately; follow dependency and execution paths.

## Complete when
A new engineer or agent could explain where a requested change belongs, what it can break, and how to verify it.
