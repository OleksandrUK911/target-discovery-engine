# TODO — Мережевий аналіз (Target Discovery)

## Побудова графа
- [ ] Побудова графа протеїн-протеїнових взаємодій навколо кандидатів (networkx, STRING edges) — **P0** | ~4h
- [ ] Визначити радіус підграфа (1-hop/2-hop сусіди навколо target) для обмеження розміру візуалізації — **P1** | ~2h

## Метрики мережі
- [ ] Виявлення "хабів" у мережі (degree centrality, betweenness centrality) — **P1** | ~3h
- [ ] Обчислення network proximity до відомих approved targets для цього захворювання — **P2** | ~3h
- [ ] Використання centrality як допоміжного feature у скорингу (опційно) — **P2** | ~2h

## Продуктивність
- [ ] Оптимізація побудови графа для великих PPI-мереж (обмеження за confidence score STRING) — **P2** | ~2h

### Примітки
- Мережевий аналіз не обов'язково входить у фінальний скор — може бути окремим "insight"-шаром для UI (граф взаємодій).

### Залежності
- Потребує adjacency-структури зі `data/TODO_preprocessing_pipeline.md`. Вихід (підграф + centrality) споживається ендпоінтом `GET /target/{id}/network` у `backend/TODO_api_design.md` та компонентом візуалізації мережі у `frontend/TODO_ui_components.md`.
