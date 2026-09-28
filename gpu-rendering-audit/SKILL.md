---
name: gpu-rendering-audit
description: Review GPU/rendering systems using wgpu/WebGPU/Three.js or similar APIs for pipeline correctness, resource lifetime, synchronization, frame-graph design, shader cost, compatibility, memory, LOD/streaming, and measurable frame budgets.
---

# GPU Rendering Audit

## Correctness first
Trace one frame:
CPU update → resource preparation → passes → synchronization → presentation.

Check:
- bind group/layout compatibility;
- texture/buffer formats and usage flags;
- lifetime of transient/persistent resources;
- resize/recreate behavior;
- command ordering and dependencies;
- coordinate/depth conventions;
- shader interface consistency;
- device-lost/error handling.

## Performance
Measure before changing:
- CPU frame/submission time;
- GPU pass timings when available;
- draw/dispatch count;
- buffer/texture upload volume;
- allocation churn;
- render target bandwidth;
- shader complexity;
- overdraw;
- LOD/culling efficiency;
- transient memory/VRAM pressure.

## Streaming/procedural systems
Make residency, budgets, fallback behavior and asynchronous failure visible. Avoid stalls disguised as visual quality problems.

## Compatibility
Test realistic adapter/browser/OS tiers and explicit fallback paths. Feature detection is not proof that a feature path works.

## Output
Prioritize by frame impact and correctness risk; include measurable target, evidence, fix and regression method.
