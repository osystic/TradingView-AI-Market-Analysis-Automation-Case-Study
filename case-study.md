# Case Study — TradingView AI Market-Analysis Automation

## Context

A milestone-based quantitative research workflow accumulated interactive notebooks, historical market-data preparation steps, engineered features, classification experiments, zone/regime studies, execution-oriented analysis, and generated reports.

The final engineering problem was broader than model training. The workflow needed a clear source-of-truth, explicit temporal validation, reproducible checks, stronger secret handling, a defensible boundary between historical research evidence and live-trading claims, and a disciplined method for deciding which historical delivery artifacts still belonged in maintained Git.

## Engineering challenges

1. **Temporal leakage control** — training and evaluation periods needed explicit chronological separation.
2. **Market-data integrity** — OHLC relationships, timestamps, ordering, duplicates, missing values, and required columns needed deterministic checks.
3. **Notebook state** — useful research logic had to be distinguishable from transient interactive state and generated output.
4. **Model interpretation** — classification performance needed to be reported as validation evidence rather than a profitability guarantee.
5. **Layer separation** — model research, zone/regime research, and execution-oriented analysis needed independent review boundaries.
6. **Credential safety** — market-data credentials and machine-specific paths could not remain embedded in maintained engineering artifacts.
7. **Artifact provenance** — recovered files needed duplicate, supersession, significance, bulk-data, and security review before any restoration to maintained source.
8. **Portfolio publication** — public proof had to demonstrate engineering capability without exposing private source, datasets, client information, or delivery history.

## Solution pattern

The governed engineering pattern separates input validation, deterministic feature generation, chronological splitting, model evaluation, research overlays, evidence handling, and post-closure provenance review.

```text
Input data contract
      ↓
Deterministic validation
      ↓
Reusable feature transformations
      ↓
Chronological train / validation split
      ↓
Classification evaluation
      ↓
Independent zone / regime research
      ↓
Execution-oriented analysis
      ↓
Evidence + limitation boundary
      ↓
Closure + artifact provenance review
```

## Data discipline

The maintained approach treats market data as an external dependency rather than trusted input. Before model work, the pipeline verifies required OHLCV fields, timestamp usability, logical high/low relationships, chronological ordering, and obvious missing-data conditions.

This matters because a model can appear technically successful while simply learning from malformed data, duplicated observations, or accidental future information.

## Temporal model validation

For time-series market research, random-only train/test splitting can create misleading evidence. The engineering pattern therefore makes chronological separation visible and testable.

The public case study intentionally does not publish private thresholds, datasets, coefficients, or model binaries. The important capability is the validation architecture: future-period evaluation is treated as a separate evidence boundary rather than another shuffled sample from the same history.

## Feature and model boundary

Feature engineering is organized into reproducible families such as momentum, volatility, relative volume, and price-structure transformations. Classification research is then evaluated using reviewable metrics appropriate to the historical test design.

Model outputs are not interpreted as autonomous trading instructions in this public showcase. They are one research layer that may inform downstream analysis when combined with independent risk, regime, and execution controls.

## Zone and regime research

The workflow also examined market behavior through zone/regime-oriented analysis. This research layer is intentionally separated from the classifier because it answers a different question: whether behavior changes meaningfully across market contexts rather than whether a single prediction model scores well overall.

Keeping these layers separate reduces the risk of presenting one aggregate metric as proof that every market condition behaves similarly.

## Repository hardening

The legacy workflow contained a large amount of generated research material and environment-specific notebook state. Standardization introduced a maintained-source boundary, deterministic tests, synthetic offline validation, explicit documentation, and stricter secret controls.

A particularly important lesson was that trading-research repositories require strong credential hygiene because market-data access material is commonly embedded in exploratory notebooks. Future integrations should inject sensitive configuration through environment variables or a secret manager rather than embedding it in source.

## Post-closure artifact recovery

A later evidence-recovery pass demonstrated that restoring historical files is itself an engineering-governance problem. The recovered private-delivery set contained multiple classes of material that should not automatically return to `main`: exact duplicates, earlier revisions, intermediate reports, very large generated datasets, commercial documents, archives, and legacy source with embedded access material.

The controlled recovery process therefore used five filters:

1. **Hash deduplication** to reject byte-identical copies.
2. **Chronology and supersession** to prefer the later authoritative implementation state over earlier revisions.
3. **Significance** to retain only artifacts that materially improve the engineering source-of-truth.
4. **Repository fitness** to keep bulk generated datasets and package exports out of ordinary Git history.
5. **Security quarantine** to prevent secret-bearing legacy source from being recommitted.

The private repository retained only a small authoritative implementation/evidence subset. This public showcase retained **none** of the recovered private artifacts; it documents only the sanitized governance pattern and resulting engineering lessons.

## Validation strategy

The maintained private engineering baseline uses several levels of validation:

- repository governance and structure invariants;
- secret-pattern validation;
- Python syntax validation;
- unit tests for data-contract and temporal-split behavior;
- synthetic offline smoke validation;
- explicit documentation of what GitHub CI can and cannot prove;
- post-closure artifact provenance and deduplication review.

This public repository separately validates that the showcase remains disclosure-safe and contains the required documentation artifacts without confidential implementation source.

## Outcome

The key outcome is a cleaner engineering lifecycle: research evidence remains reviewable, reusable logic is tested, confidential material stays private, historical artifacts are retained only when they remain authoritative and useful, and the public artifact demonstrates architecture and methodology without claiming more than the evidence supports.

## Lessons

- A large number of notebooks and generated reports is not a substitute for a maintained engineering source-of-truth.
- Notebook output should be treated as research evidence unless promoted into tested reusable logic.
- Temporal separation should be visible in code, tests, and documentation.
- Market-data repositories need explicit credential controls in addition to generic secret scanning.
- Historical artifact recovery requires hash-based deduplication and supersession-aware review, not bulk re-import.
- Large generated datasets and package exports should not be committed merely because they once formed part of a client delivery.
- Model metrics and trading profitability are different claims and should never be conflated.
- Public portfolio repositories should use independent sanitized history instead of mirroring private delivery repositories.
