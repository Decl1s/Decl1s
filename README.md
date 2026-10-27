<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Decl1s/Decl1s/main/assets/header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Decl1s/Decl1s/main/assets/header-light.svg">
  <img alt="Decl1s — Data Engineering. Я строю проверяемые конвейеры данных: файлы, контроль, витрины." src="https://raw.githubusercontent.com/Decl1s/Decl1s/main/assets/header-light.svg" width="100%">
</picture>

Я развиваюсь как дата-инженер: пишу на **Python и SQL**, загружаю и проверяю данные,
строю витрины и разбираю повторы, поздние события и восстановление после сбоев.
Для меня результат — это данные, происхождение и правила расчёта которых можно объяснить.

**Мой фокус:** Junior Data Engineer · Python · PostgreSQL · dbt · Polars · оркестрация.

[Флагман: CommerceGuard](https://github.com/Decl1s/commerceguard/tree/v1.0.0) ·
[Разбор проекта](https://github.com/Decl1s/Decl1s/blob/main/COMMERCEGUARD.md) ·
[Каталог работ](https://github.com/Decl1s/Decl1s/blob/main/PROJECTS.md)

## Мой главный проект — CommerceGuard

Я реализовал систему сверки **заказов, платежей и возвратов**: от файлов OMS/PSP
до объяснимого расхождения и решения специалиста с историей действий.

| Что я сделал | Что это позволяет проверить |
| --- | --- |
| Приём CSV/JSONL, контракты, immutable raw и PostgreSQL | Я сохраняю происхождение данных и обрабатываю повтор без двойных фактов |
| Сверка, settlement, поздние корректировки и backfill | Я отделяю исправленный расчёт от уже опубликованного результата |
| 9 dbt-витрин и Prefect run/resume | Я связываю модели, проверяю качество и продолжаю работу после отказа |
| Рабочее место с ролями, разбором и аудитом | Я довожу результат конвейера до понятного действия в интерфейсе |
| Docker Compose, backup/restore и CI | Я проверяю поставку и восстановление на синтетическом сценарии |

**[Полный код v1.0.0](https://github.com/Decl1s/commerceguard/tree/v1.0.0)** ·
[Демонстрация](https://github.com/Decl1s/commerceguard/blob/v1.0.0/docs/DEMO.md) ·
[Установка](https://github.com/Decl1s/commerceguard/blob/v1.0.0/docs/DEPLOYMENT.md) ·
[Проверенный CI](https://github.com/Decl1s/commerceguard/actions/runs/40409886361)

## Где я показываю конкретный навык

| Направление | Мой проект | Что я могу разобрать в коде |
| --- | --- | --- |
| SQL и моделирование | [dbt-order-marts](https://github.com/Decl1s/dbt-order-marts) | Зерно модели, `ref`, тесты данных и защита от задвоения выручки |
| Транзакции PostgreSQL | [postgres-stock-ledger](https://github.com/Decl1s/postgres-stock-ledger) | COPY → staging → атомарная партия, дубли и конкурентная загрузка |
| Табличная обработка | [polars-stock-diff](https://github.com/Decl1s/polars-stock-diff) | Full join по составному ключу, NULL/0, полнота снимка и Parquet |
| Оркестрация и качество | [dagster-delivery-assets](https://github.com/Decl1s/dagster-delivery-assets) | Assets, blocking checks, история запусков и восстановление публикации |
| События и отказы | [sqlite-event-queue](https://github.com/Decl1s/sqlite-event-queue) | Lease, fencing, retry/DLQ и атомарные результат + ACK |

Дополнительно я практикую [потоковую обработку на Go](https://github.com/Decl1s/go-stream-metrics),
[SQL-окна и Parquet в DuckDB](https://github.com/Decl1s/duckdb-meter-rollups)
и [историю SCD Type 2](https://github.com/Decl1s/sqlite-catalog-history).
Полный маршрут по направлениям, релизам и конспектам — в [каталоге](https://github.com/Decl1s/Decl1s/blob/main/PROJECTS.md).

## Как я работаю

- Я начинаю с контракта, ключей, единицы строки и смысла времени.
- Я проверяю повтор, неправильный вход и сбой между этапами вместе с основным сценарием.
- Я фиксирую зависимости, публикую исходники с проверками и описываю границы гарантий.
- Я документирую решения по-русски: карта кода, причины выбора, ошибки и задания с ответами.

Это мои **учебные и портфельные проекты на синтетических данных**. Я показываю
проверяемые результаты и ограничения каждого выпуска. Для CommerceGuard подтверждён
локальный профиль Linux x86_64 / Docker Compose; внешний сервер пока не разворачивал.
