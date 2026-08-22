# Standardization Acceptance — Public Showcase

This repository is standardized against the OSYSTIC sanitized `public-showcase` pattern.

## Acceptance points

- repository visibility confirmed public;
- Git history is independent from the confidential engineering repository;
- `.osystic/repository.yml` classifies the repository as a public showcase;
- no confidential implementation source is included;
- no client identity, private conversations, credentials, account information, commercial details, private datasets, or serialized delivery models are included;
- architecture, technical overview, case study, validation evidence, disclosure boundary, security notice, and publication notice are present;
- automated CI validates disclosure-safety invariants on pull requests and pushes to `main`;
- profitability and live-execution claims are explicitly excluded;
- public documentation is suitable for capability demonstration without functioning as a delivery-code mirror.

## Publication review

Initial publication review date: 2026-08-22.

## Lifecycle

Current lifecycle: **maintenance**. Future changes must preserve the same public/private disclosure boundary and pass the repository's public-safety workflow before merge.
