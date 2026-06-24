---
name: strategy-bsc-skill
description: Use when user wants to create a strategy, define company or department goals, build a Balanced Scorecard, or create an OKR tree. Triggers on "стратегия", "BSC", "сбалансированная система показателей", "OKR", "цели компании на год", "как нам вырасти", "стратегическое планирование".
---

# Strategy & BSC Skill

## Overview

Takes business goals and context, then produces a complete strategy package: Balanced Scorecard (4 perspectives), OKR tree, and a strategy defense plan for stakeholder presentations.

## When to Use

- Annual planning: user needs to set company or department goals
- User says "давай сделаем стратегию", "нужен BSC", "помоги с OKRs"
- User has a vision but no structured plan to get there
- User needs to present strategy to investors, board, or team

## Core Pattern

### Step 1 — Gather strategic context

Ask for (if not provided):
- What business are we in? (продукт, клиент, рынок — 2-3 предложения)
- Time horizon: 1 year / 3 years / 5 years
- Top 3 strategic goals in plain language (не формулировки, а намерения)
- Key constraints: budget, team size, market limitations
- Current state vs. desired state — what's the gap?

If the user gives goals in business language ("хочу удвоить выручку"), accept them and build from there. Don't ask them to reformulate.

### Step 2 — Balanced Scorecard (4 perspectives)

BSC maps goals across 4 perspectives. Each perspective gets 2-4 metrics.

```markdown
## Сбалансированная система показателей

### 1. Финансы (Finance)
*Как выглядит успех для инвесторов/собственника?*
| Цель | Метрика | Целевое значение | Частота |
|------|---------|-----------------|---------|
| [Цель] | [KPI] | [Значение] | [Квартал/Год] |

### 2. Клиенты (Customer)
*Как нас видят клиенты? Что им важно?*
| Цель | Метрика | Целевое значение | Частота |
|------|---------|-----------------|---------|

### 3. Процессы (Internal)
*Какие процессы должны работать отлично, чтобы выполнить цели клиентов и финансов?*
| Цель | Метрика | Целевое значение | Частота |
|------|---------|-----------------|---------|

### 4. Обучение и рост (Learning & Growth)
*Как команда и инфраструктура должны развиваться?*
| Цель | Метрика | Целевое значение | Частота |
|------|---------|-----------------|---------|
```

Rule: финансы — результат, остальное — драйверы. Если финансы не достигаются, ищи причину в процессах и людях, не в финансовых метриках.

### Step 3 — OKR Tree

Map strategic goals into 3-level OKR structure: Company → Department → Individual.

```markdown
## OKR-дерево

### Уровень 1: Компания (Год)
**Objective:** [Амбициозная цель — куда идём]
- KR1: [Измеримый результат с дедлайном]
- KR2: [Измеримый результат с дедлайном]
- KR3: [Измеримый результат с дедлайном]

### Уровень 2: Отдел/Команда (Квартал)
*(вытекает из Company Objective)*

**Objective:** [Что делает этот отдел для достижения компанейской цели]
- KR1: [Метрика + значение + дата]
- KR2: [Метрика + значение + дата]

### Уровень 3: Индивидуальный (Месяц/Спринт)
*(вытекает из Department Objective)*

**Objective:** [Конкретный вклад конкретного человека]
- KR1: [Задача с измеримым результатом]
- KR2: [Задача с измеримым результатом]
```

OKR rules:
- Objectives are inspiring, not metric-based ("стать лидером рынка", not "вырасти на 30%")
- Key Results are numeric, verifiable, and have deadlines
- Max 3 Objectives per level, max 4 KRs per Objective

### Step 4 — Strategy Defense Plan

For presenting strategy to stakeholders (investors, board, team):

```markdown
## Стратегическая защита

### Ситуация (1 слайд)
Где мы сейчас: [3 факта о текущем состоянии]

### Проблема (1 слайд)
Почему нельзя остаться на месте: [угроза или упущенная возможность]

### Решение (1-2 слайда)
Наш стратегический выбор: [что мы будем делать и чего делать не будем]

### Доказательства (1 слайд)
Почему это сработает: [данные, аналоги, тесты]

### План (1 слайд)
Ключевые инициативы и сроки (из BSC)

### Ресурсы (1 слайд)
Что нужно для реализации: деньги, люди, время

### Риски (1 слайд)
Топ-3 риска и как мы их снижаем

### Призыв к действию (1 слайд)
Что мы просим от аудитории (одобрить, выделить бюджет, поддержать)
```

### Step 5 — Choose the strategic direction (frameworks)

Before BSC/OKR, help the user pick WHERE to grow using these frameworks:

**Матрица Ансоффа** — growth direction by product × market:
| | Существующий продукт | Новый продукт |
|---|---|---|
| **Существующий рынок** | Проникновение (наименьший риск) | Развитие продукта |
| **Новый рынок** | Развитие рынка | Диверсификация (наибольший риск/выгода) |

**Цепочка создания ценности** — decompose to find where value and cost sit. Основные: входящая логистика, производство, исходящая логистика, маркетинг и продажи, сервис. Вспомогательные: инфраструктура, HR, снабжение, R&D. Порядок: ключевые виды деятельности → декомпозиция работ → расходы → ценность → план трансформации.

**Матрица McKinsey (GE)** — where to invest. Оси: привлекательность отрасли × конкурентоспособность. 9 квадратов → инвестировать и развивать / удерживать / уходить.

**Модель консолидации рынка** — what stage the market is in: открытие (1 игрок, 100%) → масштабирование (агрессивная консолидация, 15–45%) → фокусирование → баланс и альянс (лидеры 70–90%).

### Step 6 — Strategy implementation & control

Strategy without control stays on paper. Build a control loop:
- Реализация = стратегические изменения + управление реализацией (планирование, ресурсы, контроль).
- Стратегический контроль: текущий результат → анализ внешних/внутренних факторов → корректирующие мероприятия при отклонении.
- Три шага: разработка стратегической программы → внедрение изменений → стратегический контроль.

## Output Format

Deliver in this order:
1. Strategic direction (Ansoff / McKinsey / value chain) — when the user is choosing WHERE to grow
2. Balanced Scorecard (all 4 perspectives)
3. OKR Tree (company → department → individual)
4. Strategy Defense Plan (outline for presentation)
5. Implementation & control loop

## Common Mistakes

- Don't put financial metrics in Learning & Growth — that's where you put skills, tools, culture
- Don't make KRs vague ("улучшить сервис") — they must be measurable ("NPS вырастет с 45 до 60 к Q4")
- Don't create more than 3 Company Objectives — strategic focus requires saying no
- Don't skip the defense plan — strategy without a communication plan stays in a spreadsheet
