# TradingView AI Market-Analysis Automation — Case Study

> **PUBLIC SHOWCASE · SANITIZED · PORTFOLIO-SAFE**
>
> This repository is a public engineering proof artifact. It contains **no client identity, no confidential implementation source, no private datasets, no serialized private models, no credentials, no account details, no commercial terms, and no private conversations**.

![Architecture](assets/architecture.svg)

## What this repository is

An anonymized case study of a small-cap intraday market-analysis engagement that evolved from a statistically grounded TradingView resistance/rejection indicator into a broader research framework for dynamic universe construction, point-in-time features, structural zones, path-dependent outcomes, execution-aware evaluation, and early regime analysis.

The strongest engineering lesson was that model sophistication is not enough: the universe, timestamps, labels, normalization, execution assumptions, and research/production boundary all have to survive independent review.

## Engagement outcome

The initial indicator stage was completed and accepted, including a practical signal-state fix that required current zone interaction and a wick-aware interaction refinement.

The later research stage expanded substantially. It rebuilt the market universe dynamically, tightened point-in-time data construction, explored PMH and deterministic FIBO-style exhaustion structures, introduced path-dependent forward labeling, and separated raw statistical movement from constrained execution-oriented evaluation.

The final research package was **not promoted to production**. An independent methodological review identified additional stabilization work around possible leakage in part of the EV methodology, normalization consistency, and interpretation of some zone/regime relationships. The engagement was therefore closed at a research-validation milestone rather than turning exploratory evidence into an unsupported production-trading claim.

## Public vs. private repository boundary

| Area | This public showcase | Confidential engineering repository |
|---|---|---|
| Visibility | **Public** | **Private** |
| Purpose | Portfolio, proposals, capability proof | Retained engineering source/history |
| Implementation notebooks/source | **Not included** | Controlled/private |
| Raw or licensed datasets | **Not included** | Controlled/private/history |
| Serialized delivery models | **Not included** | Controlled/private/history |
| Client identity / conversations | **Not included** | Controlled/private |
| Commercial information | **Not included** | Controlled/private |
| Safe to share publicly | **Yes** | **No** |

This repository is not a fork, mirror, or source-code export. It has **independent Git history** and contains only sanitized documentation and diagrams.

## Research architecture

```text
Dynamic / historical OHLCV universe
              ↓
Point-in-time data validation
              ↓
Momentum / liquidity feature engineering
              ↓
Structural zone construction
              ↓
Path-dependent event outcomes
              ↓
Chronological model validation
              ↓
Continuation vs rejection analysis
              ↓
Execution approximation / outlier checks
              ↓
Regime-oriented research
              ↓
Evidence + explicit limitation boundary
```

## Engineering highlights

- **Representative-universe correction:** the workflow moved from a narrow symbol set toward day-by-day momentum-universe reconstruction.
- **Point-in-time discipline:** event price, ATR context, VWAP, and time-normalized relative volume were reviewed against what was knowable at the interaction timestamp.
- **Structure-aware zones:** Premarket High remained a primary liquidity level while later work tested a deterministic exhaustion/retracement zone with explicit anchoring/activation rules.
- **Path-dependent labels:** outcomes were evaluated by threshold order and paired with MFE/MAE and time-to-event measures rather than relying only on static direction labels.
- **Execution boundary:** raw excursion/EV findings were separated from constrained TP/SL-style approximation and outlier sensitivity.
- **Regime awareness:** large behavioral differences across liquidity/momentum groups motivated conditional analysis rather than one global average.
- **Research integrity:** unresolved methodology was documented as a limitation instead of being marketed as production alpha.
- **Repository hardening:** secret-bearing and machine-specific research surfaces were removed from maintained source; public material is independently sanitized.

## Technology

`Python` · `pandas` · `NumPy` · `scikit-learn` · `OHLCV validation` · `time-series validation` · `TradingView / Pine research` · `GitHub Actions`

## Validation boundary

The private engineering archive contains the confidential research history and controlled implementation material. The public repository validates only its disclosure-safe documentation boundary.

> This showcase does not reproduce confidential historical results and does not independently validate live trading performance.

## What is intentionally not claimed

This showcase does **not** claim:

- guaranteed profitability, alpha, ROI, win rate, or loss prevention;
- production trading readiness;
- live broker execution equivalence;
- that every historical research output survived later methodology review;
- future performance from historical classification metrics;
- redistribution rights for private/licensed market data;
- that this public repository reproduces the confidential implementation;
- that TradingView alert delivery or brokerage automation is validated here.

## Read more

- [Full case study](case-study.md)
- [Research evolution](docs/research-evolution.md)
- [Engineering lessons learned](docs/lessons-learned.md)
- [Technical overview](docs/technical-overview.md)
- [Validation evidence](docs/validation-evidence.md)
- [Disclosure boundary](docs/disclosure-boundary.md)
- [Standardization acceptance](docs/standardization-acceptance.md)

## Disclosure boundary

Only sanitized architecture, methodology, validation approach, repository-hardening practices, research limitations, and engineering lessons are published here. Confidential implementation source, raw datasets, private model artifacts, client information, credentials, private infrastructure, contract details, and private repository history are intentionally excluded.
