---
name: financial-report-skill
description: Use when user needs to create a financial report, analyze revenue and costs, compare plan vs actual, or prepare P&L for a period. Triggers on "финансовый отчёт", "P&L", "план-факт", "прибыль и убытки", "анализ расходов", "финансовые результаты", "где мы теряем деньги".
---

# Financial Report Skill

## Overview

Takes raw financial data (revenue, costs, periods) and produces a structured financial report: P&L statement, cost breakdown, plan vs. actual comparison, variance analysis, and actionable recommendations.

## When to Use

- User has revenue and cost data and needs a structured report
- User says "сделай финансовый отчёт", "покажи план-факт", "разбери расходы"
- User is preparing for a board meeting, investor call, or monthly review
- User wants to understand where money is being lost or where to cut

## Core Pattern

### Step 1 — Gather financial input

Ask for (if not provided):
- Period: month / quarter / year (and comparison period if doing plan-fact)
- Revenue data: by product line or in total
- Cost data: ideally split into fixed and variable
- Plan/budget numbers (if doing plan vs. actual)
- Currency

Accept data in any format: table, text, bullet list, rough numbers. Don't ask for clean spreadsheets — work with what's given.

If data is incomplete, proceed with available data and flag what's missing.

### Step 2 — P&L Statement

```markdown
## Отчёт о прибылях и убытках
**Период:** [Месяц/Квартал/Год]

| Статья | Факт | План | Отклонение | % |
|--------|------|------|------------|---|
| **Выручка** | | | | |
| [Продукт/канал 1] | | | | |
| [Продукт/канал 2] | | | | |
| **Итого выручка** | | | | |
| | | | | |
| **Переменные расходы** | | | | |
| [Статья] | | | | |
| **Итого переменные** | | | | |
| | | | | |
| **Валовая прибыль** | | | | |
| **Маржа валовой прибыли** | | | | |
| | | | | |
| **Постоянные расходы** | | | | |
| [Статья] | | | | |
| **Итого постоянные** | | | | |
| | | | | |
| **EBITDA** | | | | |
| **Чистая прибыль** | | | | |
| **Чистая маржа** | | | | |
```

### Step 3 — Cost Breakdown

Visualize cost structure:

```markdown
## Структура расходов

| Категория | Сумма | Доля от выручки | Динамика vs [период] |
|-----------|-------|----------------|---------------------|
| Фонд оплаты труда | | | |
| Маркетинг | | | |
| Аренда/инфраструктура | | | |
| Подрядчики | | | |
| Прочее | | | |
| **Итого** | | | |
```

Flag any cost category exceeding 30% of revenue as HIGH. Flag categories growing faster than revenue as WATCH.

### Step 4 — Variance Analysis

For each significant deviation (>10% from plan):

```markdown
## Анализ отклонений

### Выручка: [+/-X% от плана]
- **Факт:** [сумма]
- **План:** [сумма]
- **Причина отклонения:** [конкретная причина, не "рыночные условия"]
- **Что это значит:** [последствие]

### [Статья расходов]: [+/-X% от плана]
- **Факт:** [сумма]
- **План:** [сумма]
- **Причина:** [конкретная причина]
```

Rule: don't accept "рыночные условия" or "сезонность" as explanations without data. Ask what specifically changed.

### Step 5 — Analysis & Recommendations

```markdown
## Ключевые выводы

**Позитивные сигналы:**
- [факт 1]
- [факт 2]

**Тревожные сигналы:**
- [факт 1 — с конкретным числом]
- [факт 2 — с конкретным числом]

## Рекомендации

| # | Действие | Ожидаемый эффект | Срок | Приоритет |
|---|----------|-----------------|------|-----------|
| 1 | [Конкретное действие] | [Экономия/рост X руб.] | [Дата] | ВЫСОКИЙ |
| 2 | [Конкретное действие] | [Экономия/рост X руб.] | [Дата] | СРЕДНИЙ |

## Прогноз на [следующий период]

При сохранении текущих тенденций:
- Выручка: [прогноз]
- Расходы: [прогноз]
- Прибыль: [прогноз]

Для достижения плана необходимо: [конкретные условия]
```

### Step 6 — Точка безубыточности (break-even)

Когда нужно понять, какая выручка покрывает все затраты:
- Маржинальная прибыль = Выручка − Переменные затраты
- Маржинальность = Маржинальная прибыль / Выручка
- **Точка безубыточности = Постоянные затраты / Маржинальность**
- Запас прочности = (Выручка − BEP) / Выручка
Пересчитывать при: изменении постоянных расходов, скидках (маржа ↓ → точка ↑), повышении цен (маржа ↑ → точка ↓). Работает на стабильном рынке.

### Step 7 — Бюджеты и финансовая структура (ЦФО)

Три главных бюджета:
- **ББЛ (бюджет по балансовому листу)** — откуда пришли деньги и где заморожены.
- **БДР (бюджет доходов и расходов)** — маржинальность направлений, чистая прибыль (метод начисления).
- **БДДС (бюджет движения денежных средств)** — предотвращение кассовых разрывов (реальные деньги).
Дорожная карта внедрения ЦФО (6–12 мес): 1) пересобрать оргструктуру (реальные полномочия руководителям ЦФО) → 2) автоматизировать учёт (1С/ERP) до масштабирования → 3) короткие план-факт совещания с конкретными цифрами.

### Step 8 — Какой стандарт учёта (не путать)

- **МСФО** — для инвесторов/банков, активы по рыночной цене.
- **РСБУ** — для ФНС, активы по цене покупки, по каждому юрлицу отдельно.
- **Управленческий учёт** — для собственника, методологию определяет сам бизнес, детализация по отделам/каналам.
**Принцип соответствия:** доходы и расходы признаются в одном периоде независимо от движения денег. БДР может показывать прибыль, пока БДДС показывает нехватку денег — контролируй оба отчёта вместе.

## Output Format

Deliver in this order:
1. P&L Statement (with plan vs. actual if data available)
2. Cost Breakdown with flags
3. Variance Analysis for significant deviations
4. Key Findings and Recommendations table
5. Forward-looking Forecast

## Common Mistakes

- Don't skip P&L even if data is incomplete — build it with what's available, mark blanks
- Don't write "нужно сократить расходы" without naming the specific category and amount
- Don't give more than 5 recommendations — prioritize ruthlessly
- Don't confuse revenue and gross profit — always show margin %
- Don't skip the forecast — the past is descriptive, the future is actionable
