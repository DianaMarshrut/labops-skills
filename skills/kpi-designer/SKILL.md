---
name: kpi-designer
description: Use when user needs to create or redesign a KPI system for a role, team, or department. Applies when user has a position description, goals, or asks "how do we measure this person's work."
---

# KPI Designer

## Overview

Takes role + goals and produces a KPI system: metrics, weights, calculation formula, and measurement frequency.

## When to Use

- Hiring a new role and need performance metrics
- Current metrics feel wrong or unmeasurable
- User asks "how do I evaluate [role/team]"
- Preparing for performance reviews or bonus calculation

## Core Pattern

### Step 1 — Gather input

Ask for (if not provided):
- Role name and primary function
- 2-3 main goals for this role (outcomes, not activities)
- Time horizon: monthly / quarterly / annual
- Measurement data available (CRM, spreadsheets, manual count)

### Step 2 — Design metric set

Rule: 5-7 KPIs max per role. More = noise.

Categorize by type:
- **Result metrics** — what they achieve (revenue, deals closed, tickets resolved)
- **Process metrics** — how they work (response time, completion rate)
- **Quality metrics** — how well (error rate, CSAT, rework rate)

### Step 3 — Assign weights

Weights sum to 100%. Prioritize result metrics.

```
| KPI | Type | Target | Weight | Measurement source |
|-----|------|--------|--------|-------------------|
```

### Step 4 — Calculation formula

```
Performance score = Σ (actual / target × weight)
Example: (45/50 × 30%) + (98%/95% × 20%) + ... = X%
```

Bonus thresholds (if applicable):
- <70% — below expectations
- 70-90% — meets expectations
- >90% — exceeds expectations

### Step 5 — Measurement plan

For each KPI: who measures, when, where data comes from.

### Step 6 — Classify each KPI (beyond type)

Tag every KPI on three more axes so the set stays balanced:
- **Lead vs lag** — leading (predicts the future, e.g. pipeline created) vs lagging (shows past results, e.g. revenue). A good set has both.
- **Operational vs strategic** — current-process metric vs long-term-goal metric.
- **Quantitative vs qualitative** — numbers vs hard-to-measure (reputation, engagement; use a proxy or expert score).

### Step 7 — Cascade from strategy

Every KPI must trace up to a strategic goal. Cascade: Company goal → Department KPI → Individual KPI. If a KPI doesn't ladder up to a strategic goal, drop it.

### When KPI don't work (adapt or refuse)

Do NOT force a KPI system in these cases — recommend expert/qualitative assessment instead:
- **Startups** — building processes matters more than measuring them.
- **Creative roles** — quality, not quantity; counting output corrupts the work.
- **Non-standardized processes** — no stable baseline to measure against.

## Output Format

1. KPI table (5-7 rows max)
2. Calculation formula with example
3. Measurement plan
4. Review frequency recommendation

## Common Mistakes

- Don't include activity KPIs as primary metrics (calls made ≠ calls closed)
- Don't exceed 7 KPIs — reduces focus
- Don't set targets without knowing current baseline — mark as [TBD, set after first month] if unknown
- Don't mix time horizons in one system
