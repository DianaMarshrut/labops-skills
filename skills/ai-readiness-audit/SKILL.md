---
name: ai-readiness-audit
description: Use when user explicitly wants to audit or assess AI readiness of a company, team, or department. Applies when user asks for a structured evaluation with scoring, or says "are we ready for AI", "what's our AI maturity level", "where do we start with AI implementation". Do NOT trigger on general AI questions or single tool recommendations.
---

# AI Readiness Audit

## Overview

Takes a company/team description and produces an AI readiness assessment across 4 criteria with a readiness score and priority actions.

## When to Use

- Consulting engagement: client wants to know if they're ready for AI
- User asks "can we use AI for X" or "where should we start with AI"
- Internal review before investing in AI tools
- Proposal preparation for AI implementation

## Core Pattern

### Step 1 — Gather input

Ask for (if not provided):
- Company/team size and industry
- Main processes (list top 3-5)
- Current tools and tech stack
- Data situation: what data do they have, where it lives
- Budget range (optional)
- Main pain: time, cost, quality, or growth

### Step 2 — Score 4 criteria

Rate each 1-5 with brief rationale:

| Criterion | Score | What it means |
|-----------|-------|---------------|
| **Data readiness** | 1-5 | Is relevant data collected, structured, accessible? |
| **Process maturity** | 1-5 | Are processes documented and stable enough to automate? |
| **Team adoption** | 1-5 | Will people use new tools? Change resistance level? |
| **Technical base** | 1-5 | Existing integrations, APIs, software quality |

Scoring guide:
- 1 = not ready, foundational work needed
- 3 = partially ready, gaps to fix
- 5 = ready to implement

### Step 3 — Overall readiness level

Average score → readiness tier:
- 1.0-2.5: Pre-readiness — fix foundations first
- 2.6-3.5: Basic readiness — start with low-risk experiments
- 3.6-4.5: Good readiness — systematic rollout possible
- 4.6-5.0: High readiness — full AI integration viable

### Step 4 — Priority actions

For each criterion scoring <4, provide 1 specific fix:
```
Data readiness (2/5): Start logging [X process] outcomes in a spreadsheet daily.
Process maturity (3/5): Document [top 3 processes] before automating them.
```

### Step 5 — Quick wins

List 2-3 AI use cases they can start this month with minimal risk:
- Tool suggestion + use case + expected benefit

### Step 6 — Flag risks of uncontrolled AI use

Always surface the risks of ad-hoc AI adoption (the #1 hidden problem):
- **Утечка конфиденциальных данных** — данные в публичных нейросетях могут попасть к третьим лицам.
- **Авторские права** — контент от AI может нарушать чужие права.
- **Галлюцинации** — AI выдумывает факты; обязателен фактчекинг.
- **Деградация навыков** — атрофия критического мышления у сотрудников.
Принцип: «AI предлагает, человек утверждает» — финальное решение всегда за специалистом.

### Step 7 — Legal & support context (РФ)

- **ФЗ-152** — персональные данные. Принцип минимальной достаточности: доступ только к нужным данным.
- **Прозрачность AI на сайте** — правила рекомендательных алгоритмов на русском, информировать пользователей (контроль — Роскомнадзор).
- **Статус малой технологической компании (МТК):** выручка до 4 млрд ₽/год + использование ИИ/ИТ → льготы: кредит 3–8%, поручительство Корпорации МСП, приоритет в госзакупках. Подсказать клиенту, если он подходит.

## Output Format

1. Readiness table (4 criteria + scores)
2. Overall tier with 1-line explanation
3. Priority fixes per low-scoring criterion
4. 2-3 quick win recommendations

## Common Mistakes

- Don't recommend complex AI without first checking data readiness
- Don't score 5/5 to be encouraging — honest assessment is the value
- Don't suggest expensive tools if technical base is low
- Don't skip process maturity — it's the most common blocker
