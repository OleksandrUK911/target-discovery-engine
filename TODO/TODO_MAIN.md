# TODO — Target Discovery / Prioritization Engine

## Опис проєкту

Платформа, яка на вхід отримує захворювання/стан (disease/condition) і формує
ранжований список candidate biological targets (гени/білки) на основі
відкритих біологічних даних (гени → білки → шляхи → асоціації із захворюванням).
Це перехід від "молекула" до "біологія" — демонструє роботу з
computational biology даними, а не лише з хемоінформатикою.

**Мета:** показати, що кандидат розуміє зв'язок molecular ML з біологічним
контекстом (targets, pathways, evidence), що є ключовим для AstraZeneca R&D.

**Статус:** 🔴 Не розпочато (черга після проєкту №2)

## Мовна політика

Продукт (UI, README, код, коментарі, API-документація) — англійською мовою як
основною. Українська — друга мова (i18n locale), опційна. TODO-плани
залишаються українською для зручності автора.

**[ROADMAP.md](ROADMAP.md)** — послідовність спринтів (setup → scoring → ranking/network → backend → frontend → devops → polish).

## Категорії

## Data
- [Джерела даних та ліцензування](data/TODO_sources_licensing.md)
- [Пайплайн препроцесингу](data/TODO_preprocessing_pipeline.md)
- [Якість та валідація даних](data/TODO_quality_validation.md)
- [Версіювання та відтворюваність](data/TODO_versioning_reproducibility.md)

## ML
- [Скоринг: комбінування evidence та ваги](ml/TODO_scoring_evidence_weighting.md)
- [Скоринг: pathway relevance та novelty](ml/TODO_scoring_pathway_novelty.md)
- [Пайплайн ранжування](ml/TODO_ranking_pipeline.md)
- [Мережевий аналіз](ml/TODO_network_analysis.md)
- [Оцінка та валідація ранжування](ml/TODO_evaluation_validation.md)
- [Реєстр методології скорингу](ml/TODO_model_registry.md)

## Backend
- [API Design](backend/TODO_api_design.md)
- [База даних](backend/TODO_database.md)
- [Інтеграції із зовнішніми API](backend/TODO_external_integrations.md)
- [Тестування Backend](backend/TODO_testing.md)
- [Логування та спостережуваність](backend/TODO_logging_observability.md)

## Frontend
- [UI-компоненти](frontend/TODO_ui_components.md)
- [Сторінки та флоу](frontend/TODO_pages_flows.md)
- [State та шар даних](frontend/TODO_state_data_layer.md)
- [Каркас дашборду](frontend/TODO_dashboard_layout.md)
- [Візуалізація даних](frontend/TODO_data_visualization.md)
- [Інтернаціоналізація](frontend/TODO_i18n_localization.md)
- [Доступність та адаптивність](frontend/TODO_accessibility_responsive.md)
- [Тестування Frontend](frontend/TODO_testing.md)

## DevOps
- [Контейнеризація](devops/TODO_containerization.md)
- [CI/CD](devops/TODO_cicd.md)
- [Інфраструктура та деплой](devops/TODO_infrastructure_deployment.md)
- [Моніторинг та спостережуваність](devops/TODO_monitoring_observability.md)

## Загальний прогрес

| Категорія | Виконано | Всього |
|---|---|---|
| Data | 0 | 39 |
| ML | 0 | 40 |
| Backend | 0 | 38 |
| Frontend | 0 | 57 |
| DevOps | 0 | 20 |
| **Разом** | **0** | **194** |

### Примітки
- Найскладніший проєкт із перших трьох — потребує розуміння біологічних баз даних (Open Targets, STRING, DisGeNET).
- Кожна категорія розбита на кілька фокусованих TODO-файлів у відповідній підпапці — де саме розпочати роботу, видно з переліку вище.
- Кожна задача має мітку пріоритету (**P0**/**P1**/**P2**) та орієнтовну оцінку часу — використовуйте їх для планування спринтів у [ROADMAP.md](ROADMAP.md).
- ML-категорія "Методологія скорингу" розбита на два фокусовані файли: evidence/ваги та pathway/novelty (див. вище).
