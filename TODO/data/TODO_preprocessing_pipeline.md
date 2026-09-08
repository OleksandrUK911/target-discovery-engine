# TODO — Пайплайн препроцесингу (Target Discovery)

## Уніфікована таблиця target-disease
- [ ] Спроєктувати схему таблиці ген → хвороба → тип доказовості → значення скору → джерело — **P0** | ~3h
- [ ] Написати ETL-скрипт злиття Open Targets association scores з DisGeNET GDA — **P0** | ~1d
- [ ] Обробити випадки конфліктуючих/дублюючих оцінок з різних джерел (стратегія агрегації) — **P0** | ~4h

## Нормалізація ідентифікаторів
- [ ] Нормалізація ідентифікаторів генів через HGNC (symbol → Ensembl gene ID) — **P0** | ~4h
- [ ] Нормалізація ідентифікаторів білків через UniProt (accession ↔ gene symbol mapping) — **P0** | ~4h
- [ ] Обробка застарілих/alias-символів генів (HGNC previous symbols, synonyms) — **P1** | ~3h

## Інтеграція pathway-даних
- [ ] Побудова mapping ген → pathway (Reactome) для кожного кандидата — **P0** | ~4h
- [ ] Агрегація pathway-рівня в pathway relevance feature (кількість/вага асоційованих шляхів) — **P1** | ~3h

## PPI-дані
- [ ] Препроцесинг STRING edges (фільтрація за combined_score threshold) — **P0** | ~3h
- [ ] Побудова adjacency-структури для подальшого мережевого аналізу — **P0** | ~3h

### Примітки
- Нормалізація ID — критична: без неї гени з різних джерел (symbol vs Ensembl vs UniProt) не зіллються коректно.

### Залежності
- Потребує вибору демо-захворювань та розуміння API/bulk-форматів з `data/TODO_sources_licensing.md` перед стартом ETL.
- Вихідна уніфікована таблиця та adjacency-структура є прямим входом для `ml/TODO_scoring_evidence_weighting.md`, `ml/TODO_network_analysis.md` та `backend/TODO_database.md` (наповнення БД).
