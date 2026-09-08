# TODO — Контейнеризація (Target Discovery)

## Dockerfile
- [ ] Dockerfile backend з графовими бібліотеками (networkx та їх системними залежностями) — **P0** | ~2h
- [ ] Dockerfile frontend (multi-stage build: build + nginx serve) — **P0** | ~2h
- [ ] Оптимізація розміру образів (slim base images, layer caching для pip/npm) — **P2** | ~2h

## docker-compose
- [ ] docker-compose.yml (backend + frontend + БД кешу) — **P0** | ~2h
- [ ] Налаштування .env для локальної розробки (API keys, DB connection string) — **P0** | ~1h
- [ ] Healthcheck для сервісів у docker-compose — **P1** | ~1h

### Примітки
- networkx сам по собі легкий, але деякі його опційні бекенди (наприклад, для великих графів) можуть вимагати додаткових system-залежностей — варто перевірити на етапі побудови образу.

### Залежності
- Dockerfile backend залежить від фінального набору залежностей `ml/TODO_network_analysis.md` (networkx) та `backend/TODO_database.md` (обрана СУБД).
