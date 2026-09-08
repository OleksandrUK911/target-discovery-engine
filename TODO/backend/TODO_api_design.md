# TODO — API Design (Target Discovery)

## Основні ендпоінти
- [ ] Ендпоінт `POST /targets` (disease/condition → ранжований список targets) — **P0** | ~4h
- [ ] Ендпоінт `GET /target/{id}` (детальна картка target: evidence, pathways, publications) — **P0** | ~3h
- [ ] Ендпоінт `GET /diseases` (список підтримуваних demo-захворювань з автокомплітом) — **P0** | ~2h
- [ ] Ендпоінт `GET /target/{id}/network` (підграф PPI навколо target для візуалізації) — **P1** | ~3h

## Схеми відповідей
- [ ] Спроєктувати Pydantic-моделі для запиту/відповіді `POST /targets` (score breakdown у відповіді) — **P0** | ~3h
- [ ] Спроєктувати схему помилок (структуровані error responses для невідомого disease ID) — **P1** | ~2h
- [ ] Додати пагінацію для списку targets (limit/offset або cursor-based) — **P1** | ~2h

## Документація API
- [ ] Налаштувати OpenAPI/Swagger документацію (автогенерація FastAPI) — **P1** | ~1h
- [ ] Додати приклади запитів/відповідей у документацію — **P2** | ~2h
- [ ] Забезпечити англійську мову для OpenAPI-документації та текстів помилок у відповідях API (див. "Мовна політика" у `TODO_MAIN.md`) — **P1** | ~1h

### Примітки
- Схема відповіді `POST /targets` має включати breakdown скору (evidence/pathway/novelty), інакше UI не зможе показати пояснення ранжування.

### Залежності
- Формат score breakdown у відповіді визначається `ml/TODO_ranking_pipeline.md` (пояснюваність). Swagger-схема тут — прямий вхід для `frontend/TODO_state_data_layer.md` (типізований API-клієнт).
