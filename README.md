# Дмитрий Никульшин

**Fullstack-разработчик.** TypeScript, Node.js, React, PostgreSQL, Python. AI-интеграции — усиление, а не вывеска.

[Портфолио](https://dnikulshin.github.io) · [Telegram](https://t.me/nikulshin_dev) · d.nikulshin.dev@gmail.com

---

## Коротко

Полтора года в найме и два года своих систем. Собираю сервисы целиком: схема данных, API, интерфейс, деплой.
Проверяемое: **12 публичных репозиториев с GitHub Actions, 8 из них с CI-проверками, в 11 есть тесты**.

| Проект | Что это | Проверка |
| --- | --- | --- |
| [**corporate-transport**](https://github.com/DNikulshin/corporate-transport) | Диспетчерская автопарка: координаты с телефона по WebSocket, у диспетчера карта по SSE, офлайн-очередь в IndexedDB. Fastify, React, Expo, PostgreSQL, Redis | 3 workflow · vitest · MIT |
| [**scan-agent**](https://github.com/DNikulshin/scan-agent) | Агент мониторинга фриланс-бирж: Playwright обходит пять площадок, LLM оценивает заказы, PWA-дашборд с push и Telegram-уведомлениями | 3 workflow · MIT |
| [**docbrain**](https://github.com/DNikulshin/docbrain) | RAG по внутренним документам: FastAPI, pgvector, парсеры PDF/DOCX/Markdown/URL, MinIO, импорт из Google Drive через n8n | 2 workflow (CI + CD) · pytest · MIT |
| [**pc-remote**](https://github.com/DNikulshin/pc-remote) | Управление парком Windows-машин: агент-служба, очередь команд, релизы. Fastify, Prisma, Expo | 5 workflow · 8 spec-файлов · релизы |
| [**support-ticketing-system**](https://github.com/DNikulshin/support-ticketing-system) | Helpdesk: NestJS 11, Prisma, JWT + RBAC, Swagger, React 19 на Vite | 2 workflow · unit + e2e |
| [**AnyWhereDesk**](https://github.com/DNikulshin/AnyWhereDesk) | Self-hosted удалённый доступ к Windows: Guacamole, Caddy, HTTPS, 2FA | MIT |

---

## Опыт

**ООО «Связь Стандарт»** · июль 2023 — декабрь 2024 · Fullstack-разработчик

Собрал с нуля внутренний helpdesk для сервисной службы. React PWA с Яндекс.Картами для распределения
выездов, Node.js/Express и PostgreSQL на сервере, роли диспетчер / инженер / руководитель, уведомления
о критических инцидентах. Переписал тяжёлые выборки и индексы — списки заявок с фильтрами перестали тормозить.

**Свои системы** · декабрь 2024 — сейчас

Проектирую и пишу сервисы целиком, от схемы БД до деплоя. Код открыт, на каждый пуш — CI.

---

## Стек

| | |
| --- | --- |
| **Backend** | TypeScript, Node.js, NestJS, Fastify, Python, FastAPI, SQLAlchemy + Alembic |
| **Данные** | PostgreSQL, pgvector, Redis Pub/Sub, Prisma, SQLite, MinIO |
| **Frontend** | React, Next.js, TanStack Query, Zustand, Tailwind CSS, React Native (Expo), PWA |
| **AI** | RAG на pgvector, эмбеддинги и LLM через OpenRouter / DeepSeek, разбор и скоринг текста моделью |
| **Инфраструктура** | Docker Compose, GitHub Actions, Caddy, Cloudflare, Linux VPS |
| **Тесты** | Vitest, Jest, pytest, Playwright |

---

## Как я раскладываю код

- **Внутри сервиса** — слои `app → features → services → shared`, зависимости в одну сторону,
  без циклов. Так устроены `corporate-transport` и этот [сайт](https://github.com/DNikulshin/dnikulshin.github.io).
- **Монорепо** — `pnpm` workspaces: `apps/{agent,backend,mobile}` + `packages/shared` в
  [`pc-remote`](https://github.com/DNikulshin/pc-remote). Общий код уезжает в `packages`
  только после третьего повторения.
- **Разбор границ ответственности** — в [вики профиля](https://github.com/DNikulshin/DNikulshin/wiki):
  16 страниц про владение данными, направление зависимостей и анти-паттерны. Это рабочая методика,
  а не готовый фреймворк: Turborepo там описан как следующий шаг, в проектах пока не применяется.

---

## Открыт к работе

Продуктовые команды, где нужно довести продукт до продакшена и держать его: бэкенд, realtime,
интеграции с LLM. Москва — офис, гибрид или удалёнка. Отвечаю в тот же день.

- Telegram: [@nikulshin_dev](https://t.me/nikulshin_dev)
- Почта: d.nikulshin.dev@gmail.com
- Портфолио: [dnikulshin.github.io](https://dnikulshin.github.io)
