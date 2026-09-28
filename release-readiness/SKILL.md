---
name: release-readiness
description: Determine whether one exact source revision is ready to publish or deploy, including tests, packaging, compatibility, provenance, security, documentation, artifacts, and rollback. Use before tagging or shipping.
---

# Release Readiness

Pin the exact SHA being evaluated. A moving branch is not a release candidate.

## Gate
Check only what applies:
- clean build from a fresh environment;
- unit/integration/E2E/numerical/browser/GPU tests;
- installer/package creation and installation test;
- supported-platform compatibility;
- dependency and license changes;
- security-sensitive changes;
- migrations and rollback;
- configuration defaults;
- documentation/changelog/version;
- artifact provenance and checksums;
- hosted CI status at the same SHA;
- smoke test of the packaged artifact, not just source.

## Claims
Review release notes with claim-calibration. New “support”, “performance”, “accuracy” or “production” claims require their own evidence.

## Failure rule
Do not waive a failing gate by averaging it against successful gates. Either resolve it or explicitly declare the release scope/known issue.

## Output
For the pinned SHA: passed gates, failed gates, unavailable gates, residual risk, artifact identifiers and rollback instructions. Tag only the state actually evaluated.
