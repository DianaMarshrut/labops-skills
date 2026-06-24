---
name: ops-plan-builder
description: Use when user needs to build an operational plan for a quarter, month, or sprint. Applies when user says "plan the quarter", "build a monthly plan", "structure our Q3 priorities", or has a list of goals and needs tasks/owners/deadlines. Do NOT trigger on single-task requests or process analysis questions.
---

# Ops Plan Builder

## Overview

Takes goals + available data and produces a draft operational plan: priorities, initiatives, tasks, owners, and milestones.

## When to Use

- Start of quarter/month: user needs a structured plan
- User has a list of goals but no execution structure
- User asks "how do we get from here to there"
- Team planning session needs a starting document

## Core Pattern

### Step 1 — Gather input

Ask for (if not provided):
- Time horizon: quarter / month / sprint
- Top 3-5 goals (outcome-level, not activities)
- Available resources: team size, budget range
- Known constraints: deadlines, dependencies, blockers
- Current state vs. desired state (gap description)

### Step 2 — Prioritize goals

Use impact/effort matrix:
```
| Goal | Impact (1-5) | Effort (1-5) | Priority |
|------|-------------|-------------|----------|
```

Priority order:
1. High impact, low effort (do first)
2. High impact, high effort (plan carefully)
3. Low impact, low effort (do if capacity allows)
4. Low impact, high effort (defer or drop)

### Step 3 — Build plan structure

```markdown
## Operational Plan — [Period]

**Goal:** [Primary outcome for the period]
**Owner:** [Lead]
**Review cadence:** [weekly/biweekly]

### Priority 1: [Initiative name]
- **Goal:** [specific measurable outcome]
- **Deadline:** [date]
- **Owner:** [name/role]
- Tasks:
  - [ ] [Task 1] — [owner] — [date]
  - [ ] [Task 2] — [owner] — [date]
- Success metric: [how we know it's done]

### Priority 2: [Initiative name]
[same structure]

### Risks
| Risk | Probability | Impact | Mitigation |
|------|------------|--------|-----------|

### Milestones
| Date | Milestone | Signal |
|------|-----------|--------|
```

### Step 4 — Sanity check

Before finalizing:
- Do the tasks actually lead to the goals?
- Is total workload realistic for team size and time?
- Is every goal owned by someone specific?

Flag overloaded owners or missing owners explicitly.

## Output Format

1. Priority table (impact/effort matrix)
2. Full plan with initiatives, tasks, owners, dates
3. Risk table
4. Milestone timeline

## Common Mistakes

- Don't list activities as goals ("hold 5 meetings" is not a goal)
- Don't create a plan without owners — unowned tasks don't happen
- Don't skip the risk table — it's what separates a plan from a wishlist
- Don't over-plan: max 3 priorities per period, 5-7 tasks per priority
