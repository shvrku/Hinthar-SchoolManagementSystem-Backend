# Hinthar School Management System — Backend

API backend for **Hinthar**, a school management system that powers the web dashboard.

Companion frontend: [Hinthar-SchoolManagementSystem-Frontend](https://github.com/shvrku/Hinthar-SchoolManagementSystem-Frontend)

## Capabilities

- **People & catalog** — teachers, students, staff, subjects
- **Classes** — cohorts and enrollment
- **Timetable → sessions** — recurring slots generate dated class sessions
- **Lesson attendance** — per-session status and class aggregates
- **Ad-hoc sessions** — tutoring / one-off attendance flows
- **Campus check-in** — daily presence (QR and manual)
- **Stats** — system-wide summary counts

Authenticated via Clerk-issued JWTs; roles are enforced on the API.

## Tech stack

| Layer | Technology |
|-------|------------|
| API | Django 5 + Django REST Framework |
| Database | PostgreSQL |
| Auth | Clerk (JWT) |
| Docs | OpenAPI 3 (drf-spectacular) |

Interactive API docs (when the server is running): `/api/v1/docs/`

## Getting started

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
# Set DATABASE_URL, SECRET_KEY, and Clerk settings
python manage.py migrate
python manage.py runserver
```

API base: [http://localhost:8000/api/v1/](http://localhost:8000/api/v1/)

See `.env.example` for required variables. Pair with the [frontend](https://github.com/shvrku/Hinthar-SchoolManagementSystem-Frontend) on port 3000 for the full UI.

## License

© Hinthar — All rights reserved.

Shared for portfolio demonstration. Not licensed for production use or redistribution without permission.

Publishable Version Uploads Automated by Cursor
