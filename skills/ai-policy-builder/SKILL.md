---
name: ai-policy-builder
description: Use when a company needs an internal policy/regulation for using AI — a white-list of tools, confidential-data rules, fact-checking, roles, and rollout. Triggers on "регламент по работе с ИИ", "правила использования AI", "политика ИИ в компании", "белый список нейросетей", "как безопасно внедрить AI", "AI governance".
---

# AI Policy Builder

## Overview

Takes a company context and produces a ready-to-adopt AI usage policy (регламент): scope, white-list of approved tools, confidential-data rules, copyright & fact-checking, roles & responsibility, consequences, and a 4-stage rollout plan. Strong B2B consulting deliverable.

## When to Use

- A company uses AI ad-hoc and needs rules before it causes damage
- Consulting engagement: client wants a safe AI adoption framework
- Preparing an internal LNA (локальный нормативный акт) for AI
- After an incident (data leak, bad AI output) — formalize the rules

## Core Pattern

### Step 1 — Gather input

Ask for (if not provided):
- Company size, industry, departments using AI
- What AI tools are already in use (officially or not)
- Data sensitivity: personal data (ФЗ-152)? trade secrets? client data?
- Who would own the policy (IT / legal / HR / ops)

### Step 2 — Name the risks (the "why")

Ground the policy in concrete risks of stихийное use:
- Утечка конфиденциальных данных в публичные нейросети.
- Нарушение авторских прав сгенерированным контентом.
- Галлюцинации — фактические ошибки.
- Профессиональная деградация — атрофия критического мышления.

### Step 3 — Build the regulation (6 sections)

1. **Общие положения** — цель, область применения, термины.
2. **«Белый список»** разрешённых инструментов (по задачам и отделам).
3. **Правила работы с конфиденциальными данными** — что НЕЛЬЗЯ вводить в публичные сервисы; принцип минимальной достаточности (ФЗ-152).
4. **Авторское право и обязательный фактчекинг** — всё, что от AI, проверяет человек.
5. **Роли и ответственность** — IT (инструменты/доступы), юристы (право), HR (обучение), руководители (контроль).
6. **Последствия нарушений.**

### Step 4 — Three ethical principles

- Не вводить в заблуждение — чат-боты представляются как виртуальные помощники.
- Финальное слово за специалистом — «AI предлагает, человек утверждает».
- Проверка алгоритмов на предвзятость — регулярный аудит.

### Step 5 — Rollout plan (4 stages)

1. Подготовка запуска — план коммуникации, обучающие материалы.
2. Обучение — общая встреча + отдельные встречи для каждого отдела.
3. Отработка сопротивления.
4. Поддержка и обновление раз в полгода.

### Step 6 — Legal & responsibility frame (РФ)

- Конечный пользователь несёт ответственность за последствия применения AI.
- ФЗ-152 (персональные данные), требования к прозрачности AI на сайте (Роскомнадзор).
- Кодекс этики РФ в сфере ИИ как ориентир.

## Output Format

1. Risk summary (the case for the policy)
2. Full регламент — 6 sections, ready to paste into an LNA
3. White-list table (tool → allowed tasks → restrictions)
4. Roles & responsibility matrix
5. 4-stage rollout plan with owners and dates

## Common Mistakes

- Don't write an abstract policy — name specific tools in the white-list
- Don't forget the confidential-data section — it's the highest-risk part
- Don't skip roles — a policy without owners is not enforced
- Don't make it one-time — schedule a review every 6 months
