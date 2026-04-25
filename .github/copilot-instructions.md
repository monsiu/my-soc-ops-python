# Copilot Workspace Instructions

## Mandatory Development Checklist
- [ ] Lint: `uv run ruff check .` (no errors)
- [ ] Test: `uv run pytest` (all pass)
- [ ] Build/Run: `uv run uvicorn app.main:app --reload --port 8000` (server starts)

## Quickstart
- Python (FastAPI + Jinja2 + HTMX) social bingo game
- Main app: `app/` (templates, static, models, logic, service, data, main)
- Tests: `tests/` (API & logic)

## Key Commands
- Lint: `uv run ruff check .`
- Test: `uv run pytest`
- Run: `uv run uvicorn app.main:app --reload --port 8000`

## Styling & Frontend
- Use custom CSS in `app/static/css/app.css` ([css-utilities.instructions.md](.github/instructions/css-utilities.instructions.md))
- See [frontend-design.instructions.md](.github/instructions/frontend-design.instructions.md)

## General Rules
- Never use the Simple Browser to preview the app ([general.instructions.md](.github/instructions/general.instructions.md))

## Docs & Prompts
- Main: [README.md](README.md)
- Labs: [workshop/](workshop/) & [docs/](docs/)
- Contributing: [CONTRIBUTING.md](CONTRIBUTING.md)
- Example prompts: "/setup", "Add a new bingo question", "Redesign the bingo board UI"
# Copilot Workspace Instructions

## Development Checklist
- Run `uv run ruff check .` and ensure no lint errors
- Run `uv run pytest` and ensure all tests pass
- Follow Python conventions: snake_case, type hints, no unused variables/imports

## Project Overview
Soc Ops is a Social Bingo game built with Python (FastAPI + Jinja2 + HTMX). Players find people who match questions to mark squares and get 5 in a row.

## Architecture
- `app/` — Main application
  - `templates/` — Jinja2 HTML templates (base, home, components)
  - `static/` — CSS & JS assets
  - `models.py` — Pydantic models (GameState, BingoSquare)
  - `game_logic.py` — Board generation & bingo detection
  - `game_service.py` — Session management (GameSession)
  - `data.py` — Question bank
  - `main.py` — FastAPI routes & HTMX endpoints
- `tests/` — API and game logic tests

## Key Commands
- `uv run uvicorn app.main:app --reload --port 8000` — Run dev server
- `uv run pytest` — Run tests
- `uv run ruff check .` — Lint

## Styling & Frontend
- Use custom CSS utilities in `app/static/css/app.css` (see [css-utilities.instructions.md](.github/instructions/css-utilities.instructions.md))
- For frontend design, follow [frontend-design.instructions.md](.github/instructions/frontend-design.instructions.md)

## General Instructions
- Never use the Simple Browser to preview the app. Start the server and confirm it runs, but do not open a browser preview. See [general.instructions.md](.github/instructions/general.instructions.md)

## Documentation
- Main guide: [README.md](README.md)
- Lab guides: [workshop/](workshop/) and [docs/](docs/)
- Contributing: [CONTRIBUTING.md](CONTRIBUTING.md)

## Example Prompts
- "/setup" — Set up the Python environment and install dependencies
- "Add a new bingo question" — Add to `app/data.py` and update tests
- "Redesign the bingo board UI" — Edit `templates/components/bingo_board.html` and related CSS

---

For advanced customization, consider creating agent, hook, instruction, or skill files in `.github/`.
