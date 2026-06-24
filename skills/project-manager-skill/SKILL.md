---
name: project-manager-skill
description: Use when user needs to launch a project or structure an existing one. Triggers on "открой проект", "запусти проект", "нужен план проекта", "составь устав", "оформи WBS", or any request to structure a new initiative with a goal, team, and deadline.
---

# Project Manager Skill

## Overview

Takes a project idea or initiative and produces a full project launch package: charter, WBS, risk matrix, milestone plan, and weekly status template.

## When to Use

- User has a new initiative and needs structure before starting
- User says "запусти проект", "нужен план", "оформи как проект"
- Team is about to start something and needs a shared framework
- User needs to present a project plan to management or stakeholders

## Core Pattern

### Step 1 — Gather project input

Ask for (if not provided):
- Project name and one-sentence goal (что должно произойти в результате)
- Deadline or target date
- Team: roles involved (can be just names or positions)
- Budget range (if known)
- Key constraints or blockers known upfront

If the user gives a vague description, ask ONE clarifying question: "Какой конкретный результат должен быть на выходе?"

### Step 2 — Project Charter

```markdown
## Устав проекта: [Название]

**Цель:** [Конкретный измеримый результат]
**Срок:** [Дата завершения]
**Спонсор/заказчик:** [Кто принимает результат]
**Руководитель проекта:** [ФИО или роль]

**Успех выглядит так:** [3 конкретных критерия]
**Провал выглядит так:** [3 признака неудачи]

**Бюджет:** [Сумма или диапазон]
**Команда:**
| Роль | Ответственность |
|------|----------------|
| [Роль] | [Что делает] |

**Ключевые заинтересованные стороны:**
| Stakeholder | Интерес | Как вовлекать |
|------------|---------|--------------|
```

### Step 3 — WBS (Work Breakdown Structure)

Break the project into 3-5 phases. Each phase has 3-7 deliverables.

```markdown
## WBS: [Название проекта]

### Фаза 1: [Название] (срок: [дата])
- 1.1 [Deliverable]
- 1.2 [Deliverable]
- 1.3 [Deliverable]

### Фаза 2: [Название] (срок: [дата])
- 2.1 [Deliverable]
...
```

Rule: deliverables are nouns (что создаётся), not verbs (что делается). "Отчёт об анализе", not "Провести анализ".

### Step 4 — Risk Matrix

Identify top 5-7 risks. Rate each by probability (1-3) and impact (1-3).

```markdown
## Матрица рисков

| # | Риск | Вероятность | Влияние | Оценка | Меры |
|---|------|------------|---------|--------|------|
| 1 | [Риск] | Высокая | Высокое | 9 | [Что делаем] |
| 2 | [Риск] | Средняя | Высокое | 6 | [Что делаем] |
```

Flag risks with score ≥ 6 as CRITICAL. These need a named owner and a specific action.

### Step 5 — Milestone Plan

```markdown
## Ключевые вехи

| Дата | Веха | Как проверяем | Ответственный |
|------|------|--------------|--------------|
| [дата] | [Что готово] | [Критерий] | [Кто] |
```

### Step 6 — Weekly Status Template

Provide a reusable template for weekly project check-ins:

```markdown
## Статус проекта — неделя [N] ([дата])

**Статус:** 🟢 По плану / 🟡 Под угрозой / 🔴 Задержка

**Что сделано за неделю:**
- [пункт]

**Что запланировано на следующую неделю:**
- [пункт]

**Риски и блокеры:**
- [пункт]

**Решения, нужные от спонсора:**
- [пункт]
```

## Output Format

Deliver in this order:
1. Project Charter
2. WBS
3. Risk Matrix (with flagged CRITICAL risks)
4. Milestone Plan
5. Weekly Status Template

## Common Mistakes

- Don't make the goal a process ("провести аудит") — make it an outcome ("получить список из 10 улучшений с ROI")
- Don't skip risks — even a simple project has at least 3 real risks
- Don't list more than 5 phases in WBS — more = noise
- Don't create milestones without owners — they become decorative
