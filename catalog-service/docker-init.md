Нужен локальной машине должны быть установлены Docker и curl. Из корня репозитория:

```bash
docker build -t catalog-service ./catalog-service
docker run --rm -p 8000:8000 catalog-service
```

Проверка:

```bash
curl -i http://localhost:8000/health
```

Ожидаемый ответ: `HTTP 200 OK`, тело `{"status":"ok"}`.
