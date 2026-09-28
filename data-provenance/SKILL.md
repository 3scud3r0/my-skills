---
name: data-provenance
description: Track origin, licensing, integrity, transformation, consent/rights, and redistribution constraints for datasets, models, binaries, media, scientific files, map/terrain assets, and other external inputs.
---

# Data Provenance

## Before use
For every material external asset record:
- canonical source and owner;
- exact version/commit/date;
- license/terms and required attribution;
- whether commercial use, modification and redistribution are allowed;
- retrieval method;
- cryptographic hash when practical;
- original filename/identifier;
- privacy/consent constraints.

## Transformation chain
Keep a traceable record:
```text
source → downloaded artifact → cleaned → filtered → converted → derived output
```

Each irreversible transform should be documented well enough to reproduce or audit it.

## Special cases
- Publicly downloadable does not mean freely redistributable.
- A model's license does not automatically cover its training data.
- Derived datasets can retain upstream restrictions.
- Map, satellite, medical and scientific data often have domain-specific attribution or usage constraints.
- API keys, auth tokens and user-provided credentials never belong in committed provenance files.

## Release gate
Before publishing derived assets, verify license compatibility, required notices, personal/sensitive data handling, and whether the repository itself is allowed to redistribute the bytes.

## Output
Produce a provenance ledger with source, version, hash, rights, transformations, attribution and unresolved legal/data-governance questions.
