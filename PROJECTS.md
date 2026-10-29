# Каталог моего портфолио

Я разделил 19 учебных работ на 15 проектов данных, включая флагман, и 4 дополнительные QA-практики. Я использую синтетические данные. Для выпущенных приложений я даю стабильный тег, конспект, CI и архив; у учебных QA-кейсов показываю их собственные материалы и проверки.

## Как я выбираю точку входа

Я начинаю с [сравнения снимков Polars](https://github.com/Decl1s/polars-stock-diff), если хочу разобрать небольшой файловый сценарий. Для SQL я выбираю [транзакционный мини-склад](https://github.com/Decl1s/postgres-stock-ledger) или [планы PostgreSQL](https://github.com/Decl1s/postgres-index-lab). Цельную систему я показываю в CommerceGuard.

Для первых шагов в QA я открываю [полную объяснённую копию GraphQL](https://github.com/Decl1s/graphql-helpdesk-lab/blob/codex/explained-edition/START_HERE.md): я читаю запросы, ожидаемые ответы и Docs в Bruno, затем выполняю упражнения.

## Мой флагман

[CommerceGuard — система сверки заказов и платежей](https://github.com/Decl1s/commerceguard/tree/v1.0.0): я связал приём данных, PostgreSQL, сверку, dbt/Prefect, рабочее место и проверенную локальную поставку. [Разбор решений](COMMERCEGUARD.md) · [CI](https://github.com/Decl1s/commerceguard/actions/runs/40409886361) · [Релиз](https://github.com/Decl1s/commerceguard/releases/tag/v1.0.0).

## SQL и хранилища

| Проект | Что я показываю | Проверки и поставка |
| --- | --- | --- |
| [Лаборатория индексов PostgreSQL](https://github.com/Decl1s/postgres-index-lab) | Я сравниваю один SELECT до и после partial/INCLUDE индекса: равенство строк, JSON EXPLAIN, buffers и прогретые измерения. [Конспект](https://github.com/Decl1s/postgres-index-lab/blob/v0.1.1/NOTES.md) | [CI: PostgreSQL Linux; unit/ZIP Windows](https://github.com/Decl1s/postgres-index-lab/actions/runs/40873024416) · [релиз v0.1.1](https://github.com/Decl1s/postgres-index-lab/releases/tag/v0.1.1) |
| [Мини-склад PostgreSQL](https://github.com/Decl1s/postgres-stock-ledger) | Я принимаю партию через COPY/staging одной транзакцией; разбираю дубли, конфликт и откат. [Конспект](https://github.com/Decl1s/postgres-stock-ledger/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/postgres-stock-ledger/actions/runs/39501807132) · [релиз v0.1.0](https://github.com/Decl1s/postgres-stock-ledger/releases/tag/v0.1.0) |
| [Заказы и возвраты на dbt](https://github.com/Decl1s/dbt-order-marts) | Я задаю зерно SQL-моделей, связываю ref/DAG, проверяю данные и исключаю fan-out. [Конспект](https://github.com/Decl1s/dbt-order-marts/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/dbt-order-marts/actions/runs/39766066365) · [релиз v0.1.0](https://github.com/Decl1s/dbt-order-marts/releases/tag/v0.1.0) |
| [История товаров SCD Type 2](https://github.com/Decl1s/sqlite-catalog-history) | Я сохраняю версии полного снимка и выбираю состояние на дату. [Конспект](https://github.com/Decl1s/sqlite-catalog-history/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/sqlite-catalog-history/actions/runs/38932582274) · [релиз v0.1.0](https://github.com/Decl1s/sqlite-catalog-history/releases/tag/v0.1.0) |
| [Почасовая энергия DuckDB](https://github.com/Decl1s/duckdb-meter-rollups) | Я разбираю SQL-окна, поздние пакеты, повтор и витрину Parquet. [Конспект](https://github.com/Decl1s/duckdb-meter-rollups/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/duckdb-meter-rollups/actions/runs/40307252089) · [релиз v0.1.0](https://github.com/Decl1s/duckdb-meter-rollups/releases/tag/v0.1.0) |

## Файлы и качество

| Проект | Что я показываю | Проверки и поставка |
| --- | --- | --- |
| [Разница складских снимков](https://github.com/Decl1s/polars-stock-diff) | Я сравниваю составные ключи, различаю NULL/0 и блокирую неполный снимок до DELETE. [Конспект](https://github.com/Decl1s/polars-stock-diff/blob/v0.1.1/NOTES.md) | [CI](https://github.com/Decl1s/polars-stock-diff/actions/runs/40873001434) · [релиз v0.1.1](https://github.com/Decl1s/polars-stock-diff/releases/tag/v0.1.1) |
| [Журналы сервисов Polars](https://github.com/Decl1s/polars-service-logs) | Я очищаю JSONL, сохраняю разделы Parquet и считаю почасовые метрики. [Конспект](https://github.com/Decl1s/polars-service-logs/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/polars-service-logs/actions/runs/38793161613) · [релиз v0.1.0](https://github.com/Decl1s/polars-service-logs/releases/tag/v0.1.0) |
| [Конвейер продаж DuckDB](https://github.com/Decl1s/junior-retail-pipeline) | Я превращаю синтетический CSV в проверенные SQL-витрины и отчёт. [Конспект](https://github.com/Decl1s/junior-retail-pipeline/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/junior-retail-pipeline/actions/runs/38793128450) · [релиз v0.1.0](https://github.com/Decl1s/junior-retail-pipeline/releases/tag/v0.1.0) |
| [Контроль CSV на Go](https://github.com/Decl1s/go-csv-quality) | Я проверяю контракт, дубли и порог брака, публикую согласованный набор файлов. [Конспект](https://github.com/Decl1s/go-csv-quality/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/go-csv-quality/actions/runs/40223981376) · [релиз v0.1.0](https://github.com/Decl1s/go-csv-quality/releases/tag/v0.1.0) |

## Оркестрация и события

| Проект | Что я показываю | Проверки и поставка |
| --- | --- | --- |
| [Окна событий Go](https://github.com/Decl1s/go-event-windows) | Я различаю event time, watermark, дубли, late и незакрытый EOF preview; объясняю 11 строк прибытия и влияние lag. [Конспект](https://github.com/Decl1s/go-event-windows/blob/v0.1.0/NOTES.md) | [CI Linux/Windows](https://github.com/Decl1s/go-event-windows/actions/runs/40875750187) · [релиз v0.1.0](https://github.com/Decl1s/go-event-windows/releases/tag/v0.1.0) |
| [Витрина доставок Dagster](https://github.com/Decl1s/dagster-delivery-assets) | Я связываю assets, blocking checks и восстановление публикации. [Конспект](https://github.com/Decl1s/dagster-delivery-assets/blob/v0.1.2/NOTES.md) | [CI](https://github.com/Decl1s/dagster-delivery-assets/actions/runs/40872717515) · [релиз v0.1.2](https://github.com/Decl1s/dagster-delivery-assets/releases/tag/v0.1.2) |
| [Оркестрация продаж Prefect](https://github.com/Decl1s/prefect-sales-flow) | Я организую задачи, повтор после отказа и проверяемый результат flow. [Конспект](https://github.com/Decl1s/prefect-sales-flow/blob/v0.1.1/NOTES.md) | [CI](https://github.com/Decl1s/prefect-sales-flow/actions/runs/39501733462) · [релиз v0.1.1](https://github.com/Decl1s/prefect-sales-flow/releases/tag/v0.1.1) |
| [Очередь событий SQLite](https://github.com/Decl1s/sqlite-event-queue) | Я разбираю lease, fencing, retry/DLQ и реальное падение процесса до COMMIT. [Конспект](https://github.com/Decl1s/sqlite-event-queue/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/sqlite-event-queue/actions/runs/40091515321) · [релиз v0.1.0](https://github.com/Decl1s/sqlite-event-queue/releases/tag/v0.1.0) |
| [Потоковые метрики Go](https://github.com/Decl1s/go-stream-metrics) | Я агрегирую JSONL с ограничением памяти и интервальной оценкой p95. [Конспект](https://github.com/Decl1s/go-stream-metrics/blob/v0.1.0/NOTES.md) | [CI](https://github.com/Decl1s/go-stream-metrics/actions/runs/39501830247) · [релиз v0.1.0](https://github.com/Decl1s/go-stream-metrics/releases/tag/v0.1.0) |

## Дополнительная практика тестирования

- В [graphql-helpdesk-lab](https://github.com/Decl1s/graphql-helpdesk-lab) я тестирую GraphQL с минимумом кода: 22 запроса Bruno, 83 декларативных Assert, демо-роли, частичные ошибки и обнаружение контролируемого дефекта прав. Я прошёл [CI Linux/Windows](https://github.com/Decl1s/graphql-helpdesk-lab/actions/runs/40872899008); [маршрут в интерфейсе](https://github.com/Decl1s/graphql-helpdesk-lab/blob/v0.1.1/GUIDE.md), [конспект и 5 заданий](https://github.com/Decl1s/graphql-helpdesk-lab/blob/v0.1.1/NOTES.md), [релиз и ZIP](https://github.com/Decl1s/graphql-helpdesk-lab/releases/tag/v0.1.1).
- В [refund-api-quality](https://github.com/Decl1s/refund-api-quality) я проверяю частичные возвраты: pytest, Hypothesis, идемпотентность и реальную SQLite-конкуренцию. Я прошёл 42 случая и обнаружил 3/3 контролируемых мутаций; [конспект и задания](https://github.com/Decl1s/refund-api-quality/blob/v0.1.1/NOTES.md), [успешный CI Linux/Windows](https://github.com/Decl1s/refund-api-quality/actions/runs/40873135878), [релиз и ZIP](https://github.com/Decl1s/refund-api-quality/releases/tag/v0.1.1).
- В [java-api-testing-lab](https://github.com/Decl1s/java-api-testing-lab) я разбираю REST API, HTTP и автотесты Java/JUnit.
- В [support-qa-case-study](https://github.com/Decl1s/support-qa-case-study) я документирую синтетическое обращение, проверки и SQL-диагностику.

## Как я предлагаю смотреть работы

Я начинаю с README выбранного проекта, затем открываю START_HERE или NOTES и повторяю демонстрацию в новом каталоге. Релиз связывает код и архив; CI показывает фактические условия проверки. Я не переношу успех одной платформы на другую и не приравниваю опубликованную документацию к выполненному тесту.

Я сохраняю прежние выпуски и различаю обновление документации и новые возможности приложения. Для каждой версии я сверяю тег, архив и соответствующий CI; актуальные ограничения читаю в VALIDATION проекта.

[Назад к профилю](https://github.com/Decl1s)

## Как я обновил портфолио · 29.10.2026

Я связал README всех 18 публичных проектов с каталогом, точкой входа и фактическими проверками. Я добавил в основной GraphQL-проект заметную ссылку на полную объяснённую копию. Я уточнил различие между выпущенными приложениями с архивами и отдельными учебными QA-кейсами.

Я получил успешные новые CI в 17 проектах с workflow. У обзора CommerceGuard и самого профиля я проверил документацию; я не приписываю им новый запуск приложения. Бизнес-правила и зависимости я сохранил, а обновлённые архивы пяти приложений выделил patch-версиями.

| Мой проект | Новый выпуск | Проверки соответствующего коммита |
| --- | --- | --- |
| [dagster-delivery-assets](https://github.com/Decl1s/dagster-delivery-assets) | [v0.1.2](https://github.com/Decl1s/dagster-delivery-assets/releases/tag/v0.1.2) | [CI success](https://github.com/Decl1s/dagster-delivery-assets/actions/runs/40872717515) |
| [polars-stock-diff](https://github.com/Decl1s/polars-stock-diff) | [v0.1.1](https://github.com/Decl1s/polars-stock-diff/releases/tag/v0.1.1) | [CI success](https://github.com/Decl1s/polars-stock-diff/actions/runs/40873001434) |
| [refund-api-quality](https://github.com/Decl1s/refund-api-quality) | [v0.1.1](https://github.com/Decl1s/refund-api-quality/releases/tag/v0.1.1) | [CI success](https://github.com/Decl1s/refund-api-quality/actions/runs/40873135878) |
| [postgres-index-lab](https://github.com/Decl1s/postgres-index-lab) | [v0.1.1](https://github.com/Decl1s/postgres-index-lab/releases/tag/v0.1.1) | [CI success](https://github.com/Decl1s/postgres-index-lab/actions/runs/40873024416) |
| [graphql-helpdesk-lab](https://github.com/Decl1s/graphql-helpdesk-lab) | [v0.1.1](https://github.com/Decl1s/graphql-helpdesk-lab/releases/tag/v0.1.1) | [CI success](https://github.com/Decl1s/graphql-helpdesk-lab/actions/runs/40872899008) |

Я сохранил предыдущие теги и архивы. Исходный учебный характер, синтетические примеры и ограничения платформ остаются частью описания каждой работы.
