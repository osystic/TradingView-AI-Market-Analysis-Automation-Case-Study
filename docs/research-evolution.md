# Research Evolution

This public-safe timeline explains how the engineering problem evolved without exposing private implementation, datasets, coefficients, client identity, or commercial details.

## Stage 1 — statistically grounded indicator

The engagement began with a short-side TradingView resistance/rejection concept backed by external historical analysis. The architecture separated offline research from the chart runtime: Python handled data preparation, event labeling, feature/model research, and validation; Pine Script consumed fixed logic for deterministic chart behavior.

A usable indicator was delivered with resistance zones, real-time probability context, relative-volume confirmation, configurable risk/alert behavior, and a later signal-state correction that tied signals strictly to current zone interaction. Wick-based zone interaction became an important practical refinement.

## Stage 2 — distribution and data-representativeness audit

Review of the initial modeling workflow exposed a key lesson: classifier quality is secondary if the training universe does not represent the actual market regime being traded.

The research therefore moved toward a dynamic day-by-day small-cap momentum universe rather than a pre-selected ticker list. This forced stricter definitions for premarket momentum, daily ATR expansion, event-time price eligibility, time-of-day normalized relative volume, and point-in-time VWAP/ATR construction.

## Stage 3 — structural zones and path-dependent outcomes

The project explored PMH and intraday structural resistance, then reduced the later research focus toward a smaller set of structurally explicit levels including Premarket High and a deterministic 78–88% retracement/exhaustion zone.

Simple labels were replaced by path-dependent event evaluation. Rather than treating any small down move as rejection, the research tracked which threshold was reached first, alongside MFE/MAE, time-to-threshold, and unresolved outcomes over multiple forward horizons.

## Stage 4 — from prediction to executable-edge research

The framework expanded beyond classification into questions such as:

- continuation versus rejection/fade behavior;
- raw excursion-based expectancy versus constrained TP/SL behavior;
- session and zone dependence;
- outlier contribution;
- liquidity/momentum regime differences;
- whether a single global directional hypothesis was appropriate for every zone type.

This was a valuable shift because it separated statistical movement from realistically executable trading edge.

## Stage 5 — methodological review and closure

The final research package was intentionally positioned as a research-grade structural-validation framework, not a production trading engine. A later independent review identified areas that would require another stabilization phase before deployment, including possible target/label leakage in part of the EV analysis, normalization consistency, and ambiguity in some zone/regime relationships.

The engagement was closed at that research milestone rather than promoting an insufficiently audited framework into production.

## Stage 6 — post-closure artifact and provenance audit

After closure, original delivery material was recovered and compared against the maintained engineering archive. This produced a second kind of validation: not model validation, but **artifact-authority validation**.

Recovered items were evaluated by content hash, chronology, supersession state, significance, repository size/fitness, and security risk. The resulting private-repository policy was deliberately selective:

- exact duplicates were rejected;
- earlier revisions were not restored when a later authoritative state was available;
- bulk generated datasets and archive exports remained outside the clean maintained tree;
- commercial/legal artifacts were treated as provenance rather than engineering source;
- legacy source containing embedded access material was quarantined rather than recommitted;
- only a compact authoritative implementation/evidence subset was retained privately.

The public showcase was re-reviewed after that audit and remained source-free. No recovered private code, dataset, model, report binary, archive, credential, or commercial document was imported here.

## Engineering takeaway

The most important result was not a headline accuracy number. It was the validation process itself: progressively better data-universe construction, point-in-time features, path-aware labels, execution-aware evaluation, the willingness to stop when research evidence was not yet strong enough for a production claim, and the discipline to treat historical artifact recovery as a provenance/security exercise rather than a bulk restore.
