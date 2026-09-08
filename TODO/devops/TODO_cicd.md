# TODO — CI/CD (Target Discovery)

## GitHub Actions
- [ ] GitHub Actions: тести скорингової логіки при кожному push/PR — **P0** | ~2h
- [ ] GitHub Actions: lint/type-check backend (ruff/mypy) та frontend (eslint/tsc) — **P1** | ~2h
- [ ] GitHub Actions: build перевірка Docker-образів — **P1** | ~2h

## Автоматизація деплою
- [ ] Автодеплой на staging при мерджі у main (за наявності хостингу) — **P2** | ~3h
- [ ] Захист від деплою при незелених тестах (required status checks) — **P1** | ~1h

### Примітки
- Тести скорингової логіки — найважливіший CI-гейт, оскільки саме вона визначає коректність основної цінності продукту (ранжування).

### Залежності
- Гейт спирається на тести з `backend/TODO_testing.md` та `frontend/TODO_testing.md`; build-перевірка образів залежить від `devops/TODO_containerization.md`.
