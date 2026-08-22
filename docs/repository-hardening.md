# Repository Hardening & Artifact Recovery

This document records the public-safe governance outcome of a post-closure artifact recovery review. It intentionally omits private filenames, hashes, implementation source, datasets, client information, commercial material, and credential values.

## Why the audit was needed

Historical quantitative-research deliveries often contain more than maintained source: notebooks, datasets, exports, reports, package copies, screenshots, binaries, contracts, and multiple revisions of the same logic. Re-importing all of that into a cleaned repository would recreate the original disorder and can also reintroduce security risk.

The recovery review therefore treated every supplied artifact as **untrusted historical input** until it passed provenance, supersession, significance, repository-fitness, and security checks.

## Review controls

### 1. Content-hash deduplication

Files were compared by cryptographic content hash so identical copies could be rejected even when filenames differed.

### 2. Chronology and supersession

Earlier implementation states and intermediate reports were compared with later delivery states. The goal was to retain an authoritative state, not every historical revision.

### 3. Significant-only retention

An artifact qualified for maintained private Git only when it materially improved at least one of:

- source-of-truth implementation;
- final research evidence;
- reproducibility;
- auditability;
- governance provenance.

### 4. Repository fitness

Large generated datasets, package archives, presentation duplicates, and intermediate exports were kept out of the clean maintained tree. Their existence can be recorded privately without turning Git into a delivery-storage system.

### 5. Security quarantine

Legacy source containing embedded access material was treated as exposed and was not recommitted. Maintained code must rely on environment-based configuration or an appropriate secret-management system.

## Resulting private-repository policy

The private engineering archive retained only a small authoritative implementation/evidence subset from the recovered delivery set. Duplicate, superseded, bulk, commercial, and security-risk artifacts remained excluded from maintained `main`.

This was a deliberate quality decision: a smaller repository with clear authority boundaries is more useful than a complete but ambiguous attachment dump.

## Public-showcase boundary

No recovered private artifact was copied into this repository. The public showcase contains only sanitized documentation and diagrams describing:

- the engineering problem;
- validation methodology;
- research evolution;
- provenance and deduplication controls;
- repository-hardening lessons;
- known limitations and non-claims.

The public repository remains independently versioned and cannot reproduce the confidential delivery implementation or research datasets.

## Governance takeaway

Repository cleanup is not complete when files are merely deleted. A robust cleanup also defines **which artifacts are authoritative, why they are retained, what is intentionally excluded, and how future recovery work avoids reintroducing duplicates, stale revisions, bulk generated data, or secret-bearing legacy material**.
