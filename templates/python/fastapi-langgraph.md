# Project: [Project Name]

## Do NOT
- Don't use `Optional[X]` — use `X | None`
- Don't use plain dicts across boundaries — use Pydantic models
- Don't restructure the LangGraph graph unless explicitly asked

## What This Is
[One or two sentences. What does this service/agent do?]

## Architecture
[e.g. LangGraph multi-agent system with FastAPI front-end and human-in-the-loop workflows]

## Key Commands
```bash
# Install deps
uv sync

# Run
uv run fastapi dev src/main.py

# Test
uv run pytest

# Lint
uv run ruff check .
uv run ruff format .
```

## Stack
- Python 3.12+
- FastAPI, LangGraph, Pydantic v2
- async-first throughout
- uv for package management
- Ruff for linting and formatting

## Code Conventions
- Type hints on every function — parameters and return types. No exceptions.
- Pydantic v2 models for all structured data. No plain dicts crossing boundaries.
- `async`/`await` for all I/O-bound code.
- Use `|` union syntax (Python 3.10+), not `Optional[X]` or `Union[X, Y]`.
- No mutable default arguments.
- Prefer `Annotated` for Pydantic field metadata.
- LangGraph: follow existing graph/node/edge structure — don't restructure the graph unless asked.

## Project Structure
```
src/
  agents/       ← LangGraph graphs and nodes
  tools/        ← tool definitions
  models/       ← Pydantic schemas
  api/          ← FastAPI routes
docs/           ← specs and architecture notes
specs/          ← task specs before implementation
```

## Things Claude Got Wrong Before
- Added sync functions in async context 
