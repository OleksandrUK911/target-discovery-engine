# TODO — Скоринг: pathway relevance та novelty (Target Discovery)

> Частина 2 з 2 колишнього файлу "Методологія скорингу" — сфокусована на pathway-компоненті та novelty-компоненті скору. Частина 1 (комбінування evidence, ваги, нормалізація) — у `ml/TODO_scoring_evidence_weighting.md`.

## Формула загального скору
- [ ] Спроєктувати загальну формулу/модель скорингу target (комбінація evidence score, pathway relevance, novelty) — **P0** | ~4h

## Pathway relevance
- [ ] Визначити спосіб оцінки pathway relevance (кількість асоційованих pathway, вага за рівнем ієрархії Reactome) — **P0** | ~3h
- [ ] Обробити targets без жодної pathway-анотації (fallback-значення, а не виключення з ранжування) — **P1** | ~2h

## Novelty-компонент
- [ ] Визначити "novelty"-компонент (наприклад, обернено пропорційно до кількості існуючих публікацій/ліків для target) — **P0** | ~4h
- [ ] Обрати проксі-джерело для novelty (кількість drugs у Open Targets, кількість публікацій із ChEMBL/PubMed) — **P1** | ~3h
- [ ] Задокументувати межі інтерпретації novelty-проксі (низька novelty ≠ поганий target, і навпаки) — **P2** | ~1h

## Валідація pathway/novelty компонентів
- [ ] Перевірити розподіл значень pathway relevance та novelty на demo-датасеті (чи не всі targets отримують однакове значення) — **P1** | ~2h

### Примітки
- Це не "передбачення" в ML-сенсі, а прозоре ранжування на основі evidence — важливо чітко комунікувати це на співбесіді, щоб не виглядало як "чорна скринька".

### Залежності
- Потребує pathway mapping зі `data/TODO_preprocessing_pipeline.md`.
- Комбінується разом із evidence-компонентом з `ml/TODO_scoring_evidence_weighting.md` у фінальний скор, що споживає `ml/TODO_ranking_pipeline.md`.
