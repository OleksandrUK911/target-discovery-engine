# TODO — Джерела даних та ліцензування (Target Discovery)

## Open Targets Platform
- [ ] Дослідити Open Targets Platform API (GraphQL) — структура target-disease association scores — **P0** | ~3h
- [ ] Вивчити типи доказовості (genetic association, somatic mutation, drugs, pathways, RNA expression, animal models) — **P0** | ~2h
- [ ] Перевірити ліміти запитів API та наявність bulk-завантаження (Google BigQuery / FTP dumps) — **P0** | ~1h
- [ ] Перевірити ліцензію Open Targets (CC0) та умови атрибуції — **P1** | ~0.5h

## STRING DB
- [ ] Дослідити STRING DB API (протеїн-протеїнові взаємодії, confidence scores) — **P0** | ~2h
- [ ] Вивчити формат bulk-файлів (protein.links, protein.info) для offline-обробки — **P0** | ~2h
- [ ] З'ясувати ліцензійні умови STRING (CC BY 4.0) для некомерційного використання — **P1** | ~0.5h

## DisGeNET
- [ ] Дослідити DisGeNET API (ген-хвороба асоціації, gene-disease association score GDA) — **P1** | ~2h
- [ ] Перевірити ліцензійні обмеження DisGeNET (некомерційна ліцензія, реєстрація API-ключа) — **P1** | ~1h
- [ ] Оцінити необхідність альтернативи (напр. Open Targets вже включає частину DisGeNET-подібних даних) — **P2** | ~1h

## Pathway-дані
- [ ] Дослідити Reactome API/bulk-файли (pathway hierarchy, gene-pathway mapping) — **P0** | ~2h
- [ ] Дослідити KEGG API (обмеження для комерційного використання — лише академічне/особисте) — **P2** | ~1h

## Вибір демо-кейсів
- [ ] Обрати 2-3 захворювання як демонстраційні кейси (наприклад, немалоклітинний рак легені, ревматоїдний артрит) — **P0** | ~2h
- [ ] Задокументувати причини вибору (достатня кількість evidence, відомі approved targets для sanity-check) — **P1** | ~1h

### Примітки
- Усі джерела — публічні бази, без proprietary/клінічних даних; DisGeNET вимагає окремої уваги до ліцензії (некомерційне використання).
- KEGG має найсуворіші обмеження — можливо, обмежитись лише Reactome для pathway-даних, щоб уникнути ліцензійних ризиків.

### Залежності
- Вибір демо-кейсів тут є вхідними даними для `data/TODO_quality_validation.md` (аналіз покриття evidence) та `ml/TODO_evaluation_validation.md` (gold standard список для sanity-check).
- Дослідження API/bulk-форматів джерел напряму визначає обсяг роботи в `data/TODO_preprocessing_pipeline.md` (ETL-скрипти) та `backend/TODO_external_integrations.md` (клієнти API).
