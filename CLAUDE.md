# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

"Spendly" — a Flask + SQLite expense tracker built as a step-by-step learning project. It is a scaffold: many parts are intentional placeholders to be implemented in numbered steps.

## Commands

```powershell
# Activate venv (Windows PowerShell)
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
.\venv\Scripts\Activate.ps1

pip install -r requirements.txt
python app.py                 # dev server with debug, http://localhost:5001
pytest                        # run all tests (pytest + pytest-flask are installed)
pytest path/to/test.py::test_name   # single test
```

No tests or linter are configured yet.

## Architecture

- `app.py` — single Flask app; all routes live here. Runs on port **5001** (not the Flask default).
- `database/db.py` — currently only a comment stub. It is meant to provide `get_db()` (SQLite connection with `row_factory` and foreign keys enabled), `init_db()` (`CREATE TABLE IF NOT EXISTS`), and `seed_db()`. `database/` is a package (`__init__.py`).
- `templates/` — Jinja templates extending `base.html` (landing, login, register). `static/css/style.css`, `static/js/main.js`.
- SQLite file `expense_tracker.db` is gitignored.

## Placeholder routes

`/logout`, `/profile`, `/expenses/add`, `/expenses/<id>/edit`, `/expenses/<id>/delete` return stub strings labelled with the step that implements them (Steps 3, 4, 7, 8, 9). `/register` and `/login` currently only render templates (GET only, no form handling). Replace stubs in place rather than adding duplicate routes.
