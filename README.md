# Spendly — Expense Tracker

A Flask + SQLite expense tracker, built step by step as a learning project with Claude Code (CampusX).

> **Status:** work in progress. The landing, login and register pages render, but authentication, the database and expense management are not implemented yet.

## Tech Stack

- **Backend:** Python, Flask 3.1.3, Werkzeug 3.1.6
- **Database:** SQLite (via the built-in `sqlite3` module)
- **Frontend:** Jinja2 templates, plain CSS, vanilla JavaScript
- **Testing:** pytest, pytest-flask

## Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/Chalkduggo/Spendly-with-Claude-Code-CampusX.git
cd Spendly-with-Claude-Code-CampusX

# 2. Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate          # Windows (PowerShell: .\venv\Scripts\Activate.ps1)
source venv/bin/activate       # macOS / Linux

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app
python app.py
```

Open http://localhost:5001 in your browser.

## Project Structure

```
├── app.py              # Flask app and all routes
├── requirements.txt
├── database/
│   └── db.py           # Database helpers (get_db, init_db, seed_db) — to be implemented
├── templates/          # Jinja2 pages (base, landing, login, register)
└── static/
    ├── css/style.css
    └── js/main.js
```

## Roadmap

This plan is a draft and will change as the project evolves.

| Step | Feature | Status |
|------|---------|--------|
| 1 | Database setup: `get_db`, `init_db`, `seed_db`; `users` and `expenses` tables | Pending |
| 2 | Registration and login (password hashing, sessions, flash messages) | Pending |
| 3 | Logout | Pending |
| 4 | Profile page (user details, expense summary) | Pending |
| 5 | Expense list | Pending |
| 6 | Filters and summaries (by date, category, totals) | Pending |
| 7 | Add expense | Pending |
| 8 | Edit expense (owner-only) | Pending |
| 9 | Delete expense (POST, owner-only) | Pending |
| 10 | Tests (pytest, pytest-flask) | Pending |

## Running Tests

```bash
pytest
```

No tests exist yet.
