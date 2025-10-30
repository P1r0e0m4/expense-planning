# SmartExpense (Flask)

## Prerequisites
- Python 3.10+
- Windows PowerShell

## Setup
1. Create and activate venv (PowerShell):
```
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Environment:
- A `.env` file is provided. Edit values if needed.
```
SECRET_KEY=change-this-secret
DATABASE_URL=sqlite:///smartexpense.db
```

## Run
```
python wsgi.py
```
Open http://127.0.0.1:5000/ in your browser.

## First-use flow
- Register at `/auth/register`.
- Add categories at `/expenses/categories`.
- Add expenses at `/expenses/`.
- View dashboard at `/dashboard/`.
- Set budgets at `/budgets/`.
- Export CSV at `/reports/`.

## Project Structure
```
Internal-hackathon/
  wsgi.py
  requirements.txt
  .env
  smartexpense/
    __init__.py
    config.py
    extensions.py
    models/
    blueprints/
    templates/
```

## Notes
- SQLite for MVP; switch `DATABASE_URL` to Postgres/MySQL if required.
- Tables auto-create on first run; migrations via Flask-Migrate can be added later.
