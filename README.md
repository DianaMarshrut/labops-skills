# Labops — навыки для AI-помощника руководителя

Набор готовых навыков (skills) для Claude Code, собранных под курс **AI LAB** —
о том, как руководитель малого и среднего бизнеса применяет AI в операционном
управлении: найм, мотивация, регламенты, финансы, стратегия, контент, отчётность.

---

## Что такое навык (skill)

Навык — это готовая инструкция для AI-помощника. Представьте регламент, который
новый сотрудник получает в первый рабочий день: пошаговый порядок действий,
шаблоны документов, примеры «как правильно». Навык — то же самое, только для
AI-помощника.

Когда вы формулируете задачу обычными словами («сделай финансовый отчёт за
месяц»), помощник сам находит подходящий навык и работает по проверенной
методике — не выдумывает каждый раз заново и не упускает шаги. Один навык — это
компактная папка с инструкцией, при необходимости с шаблонами и вспомогательными
скриптами.

---

## Что внутри

- **`skills/`** — 14 авторских навыков. Публикуются здесь файлами, готовы к установке.
- **`topics/`** — 10 тематических направлений навыков. Для каждого — какой навык под какую задачу.
- **`CATALOG.md`** — полный каталог: 14 авторских навыков + проверенные навыки из открытых
  источников (со ссылками на установку, без перезаливки чужих файлов).

---

## 10 тематических направлений навыков

| Направление | Файл | О чём |
|---|---|---|
| 1. Операционка и HR | [topics/operations-hr.md](topics/operations-hr.md) | найм, онбординг, мотивация, оценка, KPI, аудит процессов |
| 2. Финансы | [topics/finance.md](topics/finance.md) | P&L, план-факт, анализ расходов |
| 3. Стратегия | [topics/strategy.md](topics/strategy.md) | BSC/OKR, операционный план, запуск проектов |
| 4. Внедрение AI | [topics/ai-adoption.md](topics/ai-adoption.md) | регламент по AI, аудит готовности |
| 5. Маркетинг | [topics/marketing.md](topics/marketing.md) | копирайтинг, конверсия, контент-стратегия, запуски |
| 6. Исследования | [topics/research.md](topics/research.md) | веб-ресёрч, конкуренты, соцсети, расшифровки |
| 7. Контент и видео | [topics/content-video.md](topics/content-video.md) | Reels, озвучка, презентации, изображения |
| 8. Документы и отчёты | [topics/documents-reports.md](topics/documents-reports.md) | отчёты, протоколы встреч, Word/PPT/PDF/Excel |
| 9. Разработка | [topics/development.md](topics/development.md) | MCP, создание навыков, дизайн интерфейсов |
| 10. Инфраструктура помощника | [topics/agent-infra.md](topics/agent-infra.md) | Telegram, браузер, поиск навыков, совет AI |

---

## Установка

Навыки лежат в `~/.claude/skills/`. После установки Claude Code подхватывает их на
следующей сессии.

**Весь каталог сразу:**

```bash
git clone https://github.com/DianaMarshrut/labops-skills.git ~/labops-skills
```

**Подключить один навык** (например, `hiring-kit`):

```bash
# Симлинк (рекомендуется — обновляется через git pull каталога):
ln -s ~/labops-skills/skills/hiring-kit ~/.claude/skills/hiring-kit

# Либо копией:
cp -r ~/labops-skills/skills/hiring-kit ~/.claude/skills/
```

После установки просто сформулируйте задачу обычными словами — помощник сам
выберет навык.

---

## Структура репозитория

```
labops-skills/
├── README.md            # этот файл
├── LICENSE              # MIT
├── CATALOG.md           # полный каталог навыков с триггерами
├── topics/              # 10 тематических направлений
│   └── <topic>.md
└── skills/
    └── <skill-name>/
        ├── SKILL.md         # главная инструкция (с frontmatter)
        ├── scripts/         # вспомогательные скрипты (по необходимости)
        └── assets/          # шаблоны выходных файлов (по необходимости)
```

Каждый навык — самодостаточная папка. Можно поставить один, несколько или весь набор.

---

## Дополнительные источники навыков

Кроме авторских навыков AI LAB есть проверенные открытые наборы. Полный список —
в [CATALOG.md](CATALOG.md). Основные источники:

| Источник | Что внутри | Установка |
|---|---|---|
| [anthropics/skills](https://github.com/anthropics/skills) | Официальные навыки Anthropic: `skill-creator`, `docx`, `pptx`, `pdf`, `xlsx` | `git clone https://github.com/anthropics/skills.git ~/.claude/skills/anthropics` |
| [obra/superpowers](https://github.com/obra/superpowers) | Универсальные рабочие процессы: TDD, отладка, планирование | `git clone https://github.com/obra/superpowers.git ~/.claude/skills/superpowers` |
| [supabase/agent-skills](https://github.com/supabase/agent-skills) | Best practices для Supabase + Postgres | `git clone https://github.com/supabase/agent-skills.git ~/.claude/skills/supabase` |
| [qwwiwi/agentos-skills-public](https://github.com/qwwiwi/agentos-skills-public) | Ресёрч, контент, соцсети, AI-генерация, визуализация | `git clone https://github.com/qwwiwi/agentos-skills-public.git ~/.claude/skills/agentos` |
| [qwwiwi/public-gbrain-agentos](https://github.com/qwwiwi/public-gbrain-agentos) | Базовые навыки + долгосрочная память для агентов | см. репозиторий, папка `skills/` |
| [skills.sh](https://skills.sh) | Открытый реестр навыков — поиск по имени | через навык `skill-finder` |

---

## Создание своего навыка

Чтобы собрать собственный навык, поставьте официальный `skill-creator` от Anthropic —
это навык для создания навыков. Он проведёт через короткое интервью, поможет
написать инструкцию `SKILL.md`, протестировать и улучшить.

```bash
git clone https://github.com/anthropics/skills.git ~/.claude/skills/anthropics
```

После установки в Claude Code: «Создай навык для <ваша задача>» — активируется
`skill-creator`.

---

## Лицензия

14 авторских навыков (папки в `skills/`) — под [MIT](LICENSE).
Сторонние навыки в `CATALOG.md` здесь **не перезаливаются** — они остаются под своими
лицензиями у первоисточников. Ставьте их по ссылкам из каталога.
