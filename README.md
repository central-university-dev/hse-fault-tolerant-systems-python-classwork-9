1. Запускаем PostgreSQL и pgAdmin:
```bash
docker compose up -d
```

2. Запустим миграции:
```bash
docker run --rm --network="postgresql-network" -v "$(pwd)/migrations":/app liquibase/liquibase:4.19.0 --defaultsFile=/app/liquibase.properties update
```