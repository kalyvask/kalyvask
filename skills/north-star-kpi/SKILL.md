---
name: north-star-kpi
description: Use when picking, defending, or critiquing a product's north star KPI — especially when the team is debating a simple adoption/retention metric (MAU, WAU, active accounts) against a value or revenue metric (ARR, GMV, revenue per account). Forces the explainability test, the adoption-plus-retention test, and the lagging-indicator check before a metric gets named the north star.
---

# North Star KPI

## Core principle

**A north star KPI must do two jobs at once: capture whether the product is being adopted and retained, AND be simple enough that every person on the team can recite it and act on it.**

When those two jobs are in tension, simplicity wins. A revenue or value metric that the team can't move week-to-week is worse than a usage metric that everyone can.

## The debate this skill resolves

The recurring fight is **MAU vs. revenue/value**:

- **MAU (or WAU, DAU, active accounts)** — tracks adoption (did people start?) and retention (did they come back?). Simple. Explainable. Movable.
- **Revenue / value generated** — feels more "real" because it ties to outcomes. But it's a lagging indicator, contaminated by pricing, sales motion, and seasonality, and individual ICs rarely know what moved it.

The decision in our discussion was **MAU**, because it tracks adoption and retention while staying simple to explain. That is the default for early- and mid-stage products. Revenue becomes the right north star only after the product is clearly retained AND the team's daily work has a direct line to revenue (pricing, packaging, sales-led growth).

## Three tests a candidate north star must pass

Run any proposed north star through these three filters. If it fails even one, push back.

### 1. The adoption + retention test
Does the metric move only when **new users start AND existing users come back**? A metric that can go up purely from acquisition (e.g., signups, downloads, registered accounts) fails. A metric that can go up purely from squeezing existing users (e.g., ARPU) also fails. MAU passes because it requires both.

### 2. The explainability test
Can a new engineer on day one explain the metric in one sentence, without a glossary? "Monthly active users" passes. "Revenue-weighted retained value per cohort-adjusted account" fails.

If the team needs a wiki page to define it, the team will not rally around it.

### 3. The lagging-indicator test
If the team ships a great week, does the metric move this week — or next quarter? Revenue typically moves next quarter (contracts, renewals, billing cycles). MAU moves this week. A north star should be close enough to the work that the team feels the feedback loop.

## When to override and pick a value/revenue metric

Pick revenue or value-generated as the north star only when **all three** are true:

1. The product is already retained — you have proof (cohort retention curves flatten) that users come back without intervention.
2. The team's daily work directly moves revenue — pricing changes, packaging, conversion funnel, sales enablement. Not just "build features and hope."
3. You have a usage **guardrail** alongside it. Revenue as north star without a usage guardrail invites short-term extraction (raise prices, squeeze trials) at the cost of long-term adoption.

If any one of those is false, stay on the usage metric.

## Common failure modes to call out

- **Vanity proxies.** Signups, downloads, page views, GitHub stars. These measure marketing, not product.
- **Composite scores.** "Engagement score = 0.4 × sessions + 0.3 × actions + 0.3 × retention." Nobody knows what moves it. Fails the explainability test.
- **Stacking too many north stars.** If you have three, you have none. Pick one. Use the others as guardrails or input metrics.
- **Choosing the metric the dashboard already shows.** The metric you already track is not automatically the right north star. Decide first, then build the dashboard.
- **Switching the north star every quarter.** The point of a north star is that it survives roadmap changes. If it's moving quarterly, it's a roadmap metric, not a north star.

## Output when applying this skill

When asked to help define a north star KPI, return:

1. **The recommended metric** (one sentence, no jargon).
2. **Why it passes all three tests** — adoption+retention, explainability, lagging-indicator.
3. **One or two guardrail metrics** that protect against gaming the north star (e.g., if MAU is north star, guardrail on retention curve shape so you don't paper over churn with acquisition).
4. **The trigger to revisit** — what would have to be true for the team to graduate to a revenue-based north star.

Keep the answer short. A north star that needs more than a page to defend is already failing the explainability test.
