# Standardization Acceptance — Public Showcase

This repository is standardized against the OSYSTIC sanitized `public-showcase` pattern.

## Acceptance points

- repository visibility confirmed public;
- Git history is independent from the confidential engineering repository;
- `.osystic/repository.yml` classifies the repository as a public showcase;
- no confidential implementation source is included;
- no client identity, private conversations, credentials, account information, commercial details, private datasets, serialized delivery models, or recovered private delivery binaries are included;
- architecture, technical overview, full case study, research evolution, engineering lessons, repository-hardening review, validation evidence, disclosure boundary, security notice, and publication notice are present;
- automated CI validates disclosure-safety invariants on pull requests and pushes to `main`;
- profitability and live-execution claims are explicitly excluded;
- public documentation is suitable for capability demonstration without functioning as a delivery-code mirror.

## Publication reviews

- Initial publication review: **2026-08-22**.
- Full lifecycle/conversation reconciliation: **2026-08-22**.
- Post-closure recovered-artifact/public-boundary review: **2026-08-23**.

The 2026-08-23 review followed a private-repository recovery audit that used deduplication, chronology/supersession, significance, repository-fitness, and security controls. The public repository was then re-checked to confirm that the new private evidence work did not introduce confidential material here.

## Lifecycle

Current lifecycle: **maintenance**. Future changes must preserve the same public/private disclosure boundary and pass the repository's public-safety workflow before merge.
