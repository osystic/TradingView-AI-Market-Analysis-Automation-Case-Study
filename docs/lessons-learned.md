# Engineering Lessons Learned

## Representative data comes before model sophistication

A technically correct classifier can still be irrelevant if the historical universe is too narrow. The research ultimately required dynamic daily universe construction so model evidence represented the intended small-cap momentum regime rather than a convenient subset of symbols.

## Point-in-time alignment is a first-class feature requirement

Price eligibility, VWAP, relative volume, and volatility context must be computed as they would have been known at the interaction timestamp. Distribution-level sanity checks are not enough; event-level chart validation is necessary to catch alignment defects.

## Time-of-day normalization matters in intraday volume

Open-session volume has a strong natural intraday pattern. Relative-volume features should account for time-of-day baselines rather than treating an ordinary opening-volume surge as exceptional participation.

## Do not destroy useful tail information prematurely

For extreme-volume/exhaustion research, retaining a raw feature alongside a capped/model-stability version preserves information without forcing the estimator to absorb unbounded outliers directly.

## Dataset heuristics can introduce structural bias

Top-N zones, first-touch-only rules, or aggressive proximity deduplication may make a dataset visually cleaner while deleting meaningful market behavior. Structural completeness should be validated before introducing heuristic reduction.

## Labels must match the trading question

A rejection/fade problem is not equivalent to a breakout classifier with the labels reversed. Path-dependent targets, order of threshold hits, forward horizon, and zone-boundary anchoring can materially change what the model is learning.

## Raw EV is not executable EV

Large tail moves can dominate excursion-based expectancy. A realistic evaluation should distinguish unconstrained movement from tradeable TP/SL/time-stop behavior and should test outlier dependence explicitly.

## Aggregate metrics can hide regime mixing

Liquidity, premarket gain, session, and structural-zone conditions may describe materially different market archetypes. A global average can therefore hide opposing behaviors that only become visible after conditional/regime decomposition.

## Stop before production when methodology is not settled

The final research review identified issues that warranted further stabilization rather than deployment. Treating those findings as limitations—and closing the engagement at a research milestone—was a stronger engineering outcome than turning exploratory statistics into unsupported production claims.

## Public evidence should be sanitized, not mirrored

A portfolio case study can demonstrate architecture, validation discipline, and lessons without shipping private implementation, licensed data, credentials, client identity, or copied private Git history.
