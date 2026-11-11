# ALISOT API

FastAPI backend for the ALISOT personal website.

## Local run

```bash
cd backend
python -m venv .venv
# Windows: .venv\\Scripts\\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

API docs: http://localhost:8000/docs

## Endpoints
- `GET /api/health` — health check
- `POST /api/contact` — save a contact message

## Environment
Set `DATABASE_URL` to a PostgreSQL connection string and `CORS_ORIGINS` to a comma-separated list of frontend origins. SQLite is used automatically for local development when DATABASE_URL is omitted.

Deploy this folder as a Docker service on Railway or Render. Configure the environment variables in the hosting dashboard.
