# TODO — Візуалізація даних (Target Discovery)

## Граф PPI-мережі
- [ ] Обрати бібліотеку для інтерактивного графа PPI (d3-force vs cytoscape.js — оцінка продуктивності на мережах середнього розміру) — **P0** | ~3h
- [ ] Стилізація вузлів/ребер за силою evidence (товщина/колір ребра — confidence score зі STRING) — **P1** | ~3h
- [ ] Zoom/pan та click-to-expand (розкриття сусідів вузла без повного перезавантаження графа) — **P1** | ~4h

## Ранжування targets
- [ ] Bar chart ранжованих targets за скором (horizontal bar, сортування, tooltip з breakdown) — **P0** | ~3h
- [ ] Stacked/grouped bar для розбивки скору (evidence/pathway/novelty compoненти в одному barchart) — **P1** | ~3h

## Pathway-діаграма
- [ ] Pathway diagram view (візуалізація шляху з Reactome — вузли реакцій/білків) — **P1** | ~1d
- [ ] Підсвітка обраного target на pathway-діаграмі (візуальний зв'язок список ↔ діаграма) — **P2** | ~2h

## Спільна інфраструктура візуалізацій
- [ ] Спільна легенда/color-scale для узгодженості кольорів evidence між графом, бар-чартом і pathway-діаграмою — **P1** | ~2h

### Примітки
- Вибір бібліотеки для графа — критичне рішення на старті: d3-force дає більше контролю над стилізацією, cytoscape.js — готові layout-алгоритми та кращу продуктивність "з коробки" на великих графах.
- Узгоджена колірна шкала для evidence strength (не окремо для кожного графіка) — важливо для сприйняття, коли користувач переключається між графом, бар-чартом і pathway-діаграмою.

### Залежності
- Граф PPI споживає дані з ендпоінта `GET /target/{id}/network` (`backend/TODO_api_design.md`), побудованого на основі `ml/TODO_network_analysis.md`. Bar chart ранжування споживає score breakdown з `ml/TODO_ranking_pipeline.md`. Компоненти цього файлу рендеряться на сторінках з `frontend/TODO_pages_flows.md` та мають текстовий fallback за `frontend/TODO_accessibility_responsive.md`.
