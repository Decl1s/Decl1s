# Каталог моего портфолио

Я разделил работы по задачам дата-инженера. Каждый проект ниже — законченный учебный сценарий на синтетических данных; код, конспект, CI и архив доступны отдельно.

## Мой флагман

[CommerceGuard — система сверки заказов и платежей](https://github.com/Decl1s/commerceguard/tree/v1.0.0): я связал приём данных, PostgreSQL, сверку, dbt/Prefect, рабочее место и проверенную локальную поставку. [Разбор решений](COMMERCEGUARD.md) · [CI](https://github.com/Decl1s/commerceguard/actions/runs/40409886361) · [Релиз](https://github.com/Decl1s/commerceguard/releases/tag/v1.0.0).

## SQL и хранилища

| Проект | Что я показываю | Проверки и поставка |
| --- | --- | --- |
| [Лаборатория индексов PostgreSQL](https://github.com/Decl1s/postgres-index-lab) | Я сравниваю один SELECT до и после partial/INCLUDE индекса: равенство строк, JSON EXPLAIN, buffers и прогретые измерения. [Конспект](https://github.com/Decl1s/postgres-index-lab/blob/v0.1.0/NOTES.md) | [CI: PostgreSQL Linux; unit/ZIP Windows](https://github.com/Decl1s/postgres-index-lab/actions/runs/40707804868) · [релиз v0.1.0](https://github.com/Decl1s/postgres-index-lab/releases/tag/v0.1.0) |
| [Мини-склад PostgreSQL](https://github.com/Decl1s/postgres-stock-ledger) | Я принимаю партию через COPY/staging одной транзакцией; разбираю дубли, конфликт и откат. [Конспект](https://github.com/Decl1s/postgres-stock-ledger/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/postgres-stock-ledger/actions/runs/39501807132) · [релиз v0.1.0](https://github.com/Decl1s/postgres-stock-ledger/releases/tag/v0.1.0) |
| [Заказы и возвраты на dbt](https://github.com/Decl1s/dbt-order-marts) | Я задаю зерно SQL-моделей, связываю ref/DAG, проверяю данные и исключаю fan-out. [Конспект](https://github.com/Decl1s/dbt-order-marts/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/dbt-order-marts/actions/runs/39766066365) · [релиз v0.1.0](https://github.com/Decl1s/dbt-order-marts/releases/tag/v0.1.0) |
| [История товаров SCD Type 2](https://github.com/Decl1s/sqlite-catalog-history) | Я сохраняю версии полного снимка и выбираю состояние на дату. [Конспект](https://github.com/Decl1s/sqlite-catalog-history/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/sqlite-catalog-history/actions/runs/38932582274) · [релиз v0.1.0](https://github.com/Decl1s/sqlite-catalog-history/releases/tag/v0.1.0) |
| [Почасовая энергия DuckDB](https://github.com/Decl1s/duckdb-meter-rollups) | Я разбираю SQL-окна, поздние пакеты, повтор и витрину Parquet. [Конспект](https://github.com/Decl1s/duckdb-meter-rollups/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/duckdb-meter-rollups/actions/runs/40307252089) · [релиз v0.1.0](https://github.com/Decl1s/duckdb-meter-rollups/releases/tag/v0.1.0) |

## Файлы и качество

| Проект | Что я показываю | Проверки и поставка |
| --- | --- | --- |
| [Разница складских снимков](https://github.com/Decl1s/polars-stock-diff) | Я сравниваю составные ключи, различаю NULL/0 и блокирую неполный снимок до DELETE. [Конспект](https://github.com/Decl1s/polars-stock-diff/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/polars-stock-diff/actions/runs/40519497627) · [релиз v0.1.0](https://github.com/Decl1s/polars-stock-diff/releases/tag/v0.1.0) |
| [Журналы сервисов Polars](https://github.com/Decl1s/polars-service-logs) | Я очищаю JSONL, сохраняю разделы Parquet и считаю почасовые метрики. [Конспект](https://github.com/Decl1s/polars-service-logs/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/polars-service-logs/actions/runs/38793161613) · [релиз v0.1.0](https://github.com/Decl1s/polars-service-logs/releases/tag/v0.1.0) |
| [Конвейер продаж DuckDB](https://github.com/Decl1s/junior-retail-pipeline) | Я превращаю синтетический CSV в проверенные SQL-витрины и отчёт. [Конспект](https://github.com/Decl1s/junior-retail-pipeline/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/junior-retail-pipeline/actions/runs/38793128450) · [релиз v0.1.0](https://github.com/Decl1s/junior-retail-pipeline/releases/tag/v0.1.0) |
| [Контроль CSV на Go](https://github.com/Decl1s/go-csv-quality) | Я проверяю контракт, дубли и порог брака, публикую согласованный набор файлов. [Конспект](https://github.com/Decl1s/go-csv-quality/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/go-csv-quality/actions/runs/40223981376) · [релиз v0.1.0](https://github.com/Decl1s/go-csv-quality/releases/tag/v0.1.0) |

## Оркестрация и события

| Проект | Что я показываю | Проверки и поставка |
| --- | --- | --- |
| [Витрина доставок Dagster](https://github.com/Decl1s/dagster-delivery-assets) | Я связываю assets, blocking checks и восстановление публикации. [Конспект](https://github.com/Decl1s/dagster-delivery-assets/blob/v0.1.1/NOTES.md) | [CI](https://github.com/Decl1s/dagster-delivery-assets/actions/runs/40469630563) · [релиз v0.1.1](https://github.com/Decl1s/dagster-delivery-assets/releases/tag/v0.1.1) |
| [Оркестрация продаж Prefect](https://github.com/Decl1s/prefect-sales-flow) | Я организую задачи, повтор после отказа и проверяемый результат flow. [Конспект](https://github.com/Decl1s/prefect-sales-flow/blob/v0.1.1/NOTES.md) | [CI](https://github.com/Decl1s/prefect-sales-flow/actions/runs/39501733462) · [релиз v0.1.1](https://github.com/Decl1s/prefect-sales-flow/releases/tag/v0.1.1) |
| [Очередь событий SQLite](https://github.com/Decl1s/sqlite-event-queue) | Я разбираю lease, fencing, retry/DLQ и реальное падение процесса до COMMIT. [Конспект](https://github.com/Decl1s/sqlite-event-queue/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/sqlite-event-queue/actions/runs/40091515321) · [релиз v0.1.0](https://github.com/Decl1s/sqlite-event-queue/releases/tag/v0.1.0) |
| [Потоковые метрики Go](https://github.com/Decl1s/go-stream-metrics) | Я агрегирую JSONL с ограничением памяти и интервальной оценкой p95. [Конспект](https://github.com/Decl1s/go-stream-metrics/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/go-stream-metrics/actions/runs/39501830247) · [релиз v0.1.0](https://github.com/Decl1s/go-stream-metrics/releases/tag/v0.1.0) |

## Дополнительная практика тестирования

- В [graphql-helpdesk-lab](https://github.com/Decl1s/graphql-helpdesk-lab) я тестирую GraphQL с минимумом кода: 22 запроса Bruno, 83 декларативных Assert, демо-роли, частичные ошибки и обнаружение контролируемого дефекта прав. Я прошёл [CI Linux/Windows](https://github.com/Decl1s/graphql-helpdesk-lab/actions/runs/40726720072); [маршрут в интерфейсе](https://github.com/Decl1s/graphql-helpdesk-lab/blob/v0.1.0/GUIDE.md), [конспект и 5 заданий](https://github.com/Decl1s/graphql-helpdesk-lab/blob/v0.1.0/NOTES.md), [релиз и ZIP](https://github.com/Decl1s/graphql-helpdesk-lab/releases/tag/v0.1.0).
- В [refund-api-quality](https://github.com/Decl1s/refund-api-quality) я проверяю частичные возвраты: pytest, Hypothesis, идемпотентность и реальную SQLite-конкуренцию. Я прошёл 42 случая и обнаружил 3/3 контролируемых мутаций; [конспект и задания](https://github.com/Decl1s/refund-api-quality/blob/v0.1.0/NOTES.md), [успешный CI Linux/Windows](https://github.com/Decl1s/refund-api-quality/actions/runs/40562931554), [релиз и ZIP](https://github.com/Decl1s/refund-api-quality/releases/tag/v0.1.0).
- В [java-api-testing-lab](https://github.com/Decl1s/java-api-testing-lab) я разбираю REST API, HTTP и автотесты Java/JUnit.
- В [support-qa-case-study](https://github.com/Decl1s/support-qa-case-study) я документирую синтетическое обращение, проверки и SQL-диагностику.

## Как я предлагаю смотреть работы

Я начинаю с README выбранного проекта, затем открываю START_HERE или NOTES и повторяю демонстрацию в новом каталоге. Релиз связывает код и архив; CI показывает фактические условия проверки. Я не переношу успех одной платформы на другую и не приравниваю опубликованную документацию к выполненному тесту.

Я проверил ссылки на выпуски и успешный CI 27.10.2026. Старые версии сохраняю; актуальные ограничения читаю в VALIDATION соответствующего проекта.

[Назад к профилю](https://github.com/Decl1s)
