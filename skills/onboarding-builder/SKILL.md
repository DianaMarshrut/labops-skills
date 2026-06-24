---
name: onboarding-builder
description: Use when user needs to create an onboarding plan for a new employee, contractor, or role. Applies when user provides role name, team context, or asks "how do we onboard this person."
---

# Onboarding Builder

## Overview

Takes role + company context and produces a structured 30/60/90-day onboarding plan with milestones, tasks, and an FAQ for the new person.

## When to Use

- Hiring someone and need an onboarding structure
- Existing onboarding is ad-hoc or verbal
- User asks "what should a new [role] do in first 3 months"
- Onboarding a contractor or freelancer on a project

## Core Pattern

### Step 1 — Gather input

Ask for (if not provided):
- Role name and primary responsibilities
- Team size and reporting structure
- Key tools/systems they'll use
- Main deliverable expected by end of month 1, 3
- Any must-know company rules or culture notes

### Step 2 — Build 30/60/90 plan

```markdown
## 30/60/90 Onboarding Plan — [Role]

### Days 1-30: Orient & Learn
Goal: understand context, meet team, no deliverables yet

**Week 1:**
- [ ] Meet [key people]
- [ ] Get access to [tools]
- [ ] Read [key docs]

**Weeks 2-4:**
- [ ] Shadow [process]
- [ ] Complete [training]
- [ ] First small task: [specific]

Milestone: [what signals readiness to move to phase 2]

### Days 31-60: Contribute
Goal: first independent work, feedback loop

- [ ] Owns [task/area]
- [ ] Weekly sync with manager
- [ ] First deliverable: [specific]

Milestone: [what signals readiness for phase 3]

### Days 61-90: Own
Goal: full productivity, handles role independently

- [ ] Owns [full scope]
- [ ] Proposes improvements
- [ ] Reviews own first 3 months

Milestone: performance review / probation end
```

### Step 3 — Build FAQ

Top 10 questions a new person typically has:
- Where do I find X?
- Who do I ask about Y?
- What's the process for Z?
- What's the communication norm?

Format as Q&A.

### Step 4 — Map to real adaptation periods

The 30/60/90 frame is a default. For a fuller plan use the three real adaptation periods:
- **Онбординг (1–2 недели)** — документы, рабочее место, корпоративные правила, знакомство с руководителем.
- **Активное погружение (2–3 месяца)** — обучение, первые самостоятельные задачи, обратная связь.
- **Адаптация (6–9 месяцев)** — выход на полную продуктивность, погружение в культуру.

### Step 5 — Legal layer (РФ)

Always include the legal essentials:
- **Испытательный срок (ст. 70 ТК РФ):** макс. 3 месяца для рядовых, 6 месяцев для руководителей. НЕ устанавливается для беременных, лиц до 18 лет, выпускников первого года по специальности.
- **Трудовой договор** письменный (срочный/бессрочный/ГПХ), при необходимости NDA.
- За «нарушение корпоративной культуры» уволить нельзя (Глава 13 ТК РФ) — решается в разговоре.

### Step 6 — Align to business goals + grades

- Tie the plan to the company situation: быстрый рост → ускорять выход на продуктивность; трансформация → снижать сопротивление; массовый наём → стандартизировать онбординг; редкие специалисты → строить вокруг качества опыта новичка.
- **Система грейдов** нормирует зарплату и показывает карьерные перспективы — руководитель оценивает компетенции и ставит цели на испытательный срок.
- Метрика результата адаптации — не «прошёл курс», а **время выхода на план** и снижение ошибок.

## Output Format

1. 30/60/90 plan with checkboxes
2. FAQ (10 items)
3. Quick-start checklist for Day 1 (top 5 actions)

## Common Mistakes

- Don't fill Day 1 with 20 tasks — overwhelm kills motivation
- Don't skip the FAQ — it reduces manager load the most
- Don't make milestones vague ("feeling comfortable") — make them observable
