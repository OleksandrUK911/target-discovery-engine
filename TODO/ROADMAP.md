# ROADMAP — Target Discovery / Prioritization Engine

Послідовність спринтів для соло-розробки part-time (~1 тиждень на спринт,
орієнтовно 10-15 год/тиждень з асистуванням Claude Code). Кожен спринт
фокусується на **P0/P1**-задачах відповідних TODO-файлів; **P2**-задачі
підбираються опційно, якщо залишається час.

## Спринт 1 — Джерела даних та препроцесинг
**Мета:** дослідити всі зовнішні джерела, обрати демо-захворювання та побудувати уніфікований датасет target-disease з нормалізованими ідентифікаторами.
- [data/TODO_sources_licensing.md](data/TODO_sources_licensing.md)
- [data/TODO_preprocessing_pipeline.md](data/TODO_preprocessing_pipeline.md)
- [data/TODO_quality_validation.md](data/TODO_quality_validation.md) (базова перевірка покриття)

**Тривалість:** ~1 тиждень

## Спринт 2 — Методологія скорингу
**Мета:** спроєктувати та реалізувати прозору формулу скорингу таргетів (evidence + pathway + novelty) з нормалізацією та обґрунтованими вагами.
- [ml/TODO_scoring_evidence_weighting.md](ml/TODO_scoring_evidence_weighting.md)
- [ml/TODO_scoring_pathway_novelty.md](ml/TODO_scoring_pathway_novelty.md)
- [ml/TODO_model_registry.md](ml/TODO_model_registry.md) (документація формули)

**Тривалість:** ~1 тиждень

## Спринт 3 — Ранжування, мережевий аналіз та валідація
**Мета:** зібрати pipeline ранжування з пояснюваністю скору, додати мережевий (PPI) аналіз і перевірити результат проти відомих approved targets.
- [ml/TODO_ranking_pipeline.md](ml/TODO_ranking_pipeline.md)
- [ml/TODO_network_analysis.md](ml/TODO_network_analysis.md)
- [ml/TODO_evaluation_validation.md](ml/TODO_evaluation_validation.md)
- [data/TODO_versioning_reproducibility.md](data/TODO_versioning_reproducibility.md)

**Тривалість:** ~1 тиждень

## Спринт 4 — Backend API та зовнішні інтеграції
**Мета:** підняти FastAPI-сервіс з основними ендпоінтами, БД-кешем, клієнтами зовнішніх API та базовим тестовим покриттям.
- [backend/TODO_api_design.md](backend/TODO_api_design.md)
- [backend/TODO_database.md](backend/TODO_database.md)
- [backend/TODO_external_integrations.md](backend/TODO_external_integrations.md)
- [backend/TODO_testing.md](backend/TODO_testing.md) (unit-тести скорингу/ранжування)

**Тривалість:** ~1 тиждень

## Спринт 5 — Frontend dashboard
**Мета:** реалізувати UI пошуку захворювання, таблицю ранжування з розбивкою скору, картку target та типізований шар даних з кешуванням.
- [frontend/TODO_ui_components.md](frontend/TODO_ui_components.md)
- [frontend/TODO_pages_flows.md](frontend/TODO_pages_flows.md)
- [frontend/TODO_state_data_layer.md](frontend/TODO_state_data_layer.md)

**Тривалість:** ~1 тиждень

## Спринт 6 — DevOps, деплой та спостережуваність
**Мета:** контейнеризувати застосунок, налаштувати CI/CD-гейти на тестах і задеплоїти публічне демо з обмеженим набором demo-захворювань.
- [devops/TODO_containerization.md](devops/TODO_containerization.md)
- [devops/TODO_cicd.md](devops/TODO_cicd.md)
- [devops/TODO_infrastructure_deployment.md](devops/TODO_infrastructure_deployment.md)
- [backend/TODO_logging_observability.md](backend/TODO_logging_observability.md)

**Тривалість:** ~1 тиждень

## Спринт 7 — Полірування, доступність та документація
**Мета:** довести UX до презентабельного стану (адаптивність, доступність, E2E-тести) і закрити моніторинг та P2-полірування, що залишились.
- [frontend/TODO_accessibility_responsive.md](frontend/TODO_accessibility_responsive.md)
- [frontend/TODO_testing.md](frontend/TODO_testing.md)
- [devops/TODO_monitoring_observability.md](devops/TODO_monitoring_observability.md)
- [ml/TODO_model_registry.md](ml/TODO_model_registry.md) (версіювання, changelog)

**Тривалість:** ~1 тиждень (буфер під P2-задачі з усіх категорій)

### Примітки
- Спринти 1-3 (Data + ML) — критичний шлях: без валідної методології скорингу немає що показувати в API/UI, тому вони йдуть першими.
- Спринт 4 (Backend) і Спринт 5 (Frontend) можна частково паралелити, якщо контракт API (`backend/TODO_api_design.md`) зафіксований заздалегідь.
- Спринт 7 — буферний; за потреби його обсяг скорочується першим при стисненні термінів.
