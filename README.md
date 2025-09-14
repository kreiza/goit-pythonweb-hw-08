# Contacts API

REST API для управління контактами з використанням FastAPI та SQLAlchemy.

## Встановлення

1. Встановіть залежності:
```bash
pip install -r requirements.txt
```

2. Налаштуйте PostgreSQL базу даних та оновіть рядок підключення в `database.py`

3. Запустіть сервер:
```bash
uvicorn main:app --reload
```

## Docker

Запуск з Docker Compose:
```bash
docker-compose up --build
```

## API Endpoints

- `POST /contacts/` - Створити новий контакт
- `GET /contacts/` - Отримати список контактів (з пошуком: `?search=query`)
- `GET /contacts/{id}` - Отримати контакт за ID
- `PUT /contacts/{id}` - Оновити контакт
- `DELETE /contacts/{id}` - Видалити контакт
- `GET /contacts/birthdays/upcoming` - Контакти з днями народження на наступні 7 днів

## Swagger документація

Доступна за адресою: http://localhost:8001/docs (Docker) або http://localhost:8000/docs (локально)