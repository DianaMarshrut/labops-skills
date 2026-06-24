---
name: process-auditor
description: Use when user wants to analyze a business process, find inefficiencies, map current state (AS IS), or plan an improved version (TO BE). Applies to operations, sales, HR, logistics, or any repeatable workflow.
---

# Process Auditor

## Overview

Takes a process description and produces: AS IS map, top-5 loss points, TO BE improvement plan.

## When to Use

- User describes how a process works now and wants analysis
- User asks "where are we losing time/money/people"
- User wants to optimize or redesign a workflow
- Preparing for automation or delegation

## Core Pattern

### Step 1 — Gather input

Ask for (if not provided):
- Process name and purpose
- Who is involved (roles, not names)
- Approximate steps in order
- Known pain points (optional)
- Scope: one team or cross-departmental

### Step 2 — Build AS IS map

Output a numbered step list:
```
AS IS: [Process Name]
1. [Step] → Actor: [Role] | Time: [estimate] | Tool: [if known]
2. ...
Bottlenecks flagged with ⚠
Handoffs flagged with →
```

### Step 3 — Top-5 losses

Identify top losses in table form:
```
| # | Loss type | Where | Impact | Root cause |
|---|-----------|-------|--------|------------|
```

Loss types: time, money, quality, people, information.

### Step 4 — TO BE plan

For each top loss, one concrete fix:
```
TO BE fixes:
1. [Problem] → [Solution] | Who implements | Effort: S/M/L
```

End with priority order: quick wins first.

### Step 5 — Choose a notation (when formal mapping is needed)

If the user needs a formal model (for regulations, automation, or audit), pick the right notation:
- **BPMN 2.0** — how a process is executed, many participants. Best for automation. Elements: pool, lanes (actors), tasks, events (start/intermediate/end), gateways (exclusive/inclusive/parallel).
- **IDEF0** — overall structure and functions. Best for strategy/architecture. Elements: function blocks + input/control/mechanism/output arrows.
- **EPC** — event→function logic with responsibility per actor. Best for writing regulations. Operators: AND, OR, XOR.
Always model two states: AS IS («как есть») and TO BE («как будет»).

### Step 6 — Apply an improvement methodology

Match the loss pattern to a method:
- **Lean (бережливое производство)** — eliminate waste. Hunt the 7 wastes: motion, waiting, transport, defects, inventory, overproduction, over-processing. Tools: Just-in-Time, 5S, Kanban, PDCA.
- **5S** — sort, set in order, shine, standardize, sustain. For messy/manual workplaces.
- **Six Sigma (DMAIC)** — Define → Measure → Analyze → Improve → Control. For defect/variance reduction with data.
- **Kaizen** — small continuous improvements with full team involvement.
- **PDCA** — Plan → Do → Check → Act. The default loop for any incremental change.

### Step 7 — Process Excellence rollout (PEX)

When deploying a TO BE process, follow 4 steps:
1. Investigate the current process (find bottlenecks).
2. Design the new process.
3. Test the prototype on ONE object/team first (with real users).
4. Roll out to the whole business.

## Output Format

1. AS IS map (numbered steps)
2. Top-5 loss table
3. TO BE plan with effort estimates
4. Priority order: quick wins first, then systemic changes

## Common Mistakes

- Don't invent steps the user didn't mention — ask if unclear
- Don't recommend software tools without knowing the budget/context
- Don't skip the loss table — it's the actionable core
