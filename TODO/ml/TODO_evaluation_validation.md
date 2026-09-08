# TODO — Оцінка та валідація ранжування (Target Discovery)

## Sanity-check проти відомих targets
- [ ] Порівняння отриманого ранжування з відомими approved targets (sanity check — чи вони у топі списку) — **P0** | ~3h
- [ ] Зібрати невеликий "gold standard" список approved/clinical-stage targets для кожного demo-захворювання — **P0** | ~4h

## Аналіз чутливості
- [ ] Аналіз чутливості скору до ваг компонентів (sensitivity analysis — варіювання ваг evidence/pathway/novelty) — **P1** | ~4h
- [ ] Перевірка стабільності топ-N ранжування при невеликих змінах ваг — **P1** | ~2h

## Метрики якості ранжування
- [ ] Обчислення precision@K для gold standard targets (чи входять у топ-10/топ-20) — **P1** | ~3h
- [ ] Порівняння з baseline (наприклад, чисте сортування за Open Targets overall score) — **P2** | ~2h

### Примітки
- Формальних "правильних відповідей" немає (це не supervised ML задача) — валідація ґрунтується на біологічній правдоподібності, а не на accuracy metric.

### Залежності
- Gold standard список формується на основі демо-кейсів з `data/TODO_sources_licensing.md` і використовується для перевірки виходу `ml/TODO_ranking_pipeline.md`.
