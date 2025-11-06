# Codex Runbook (steps and commands)

## Quick Start
- Front: `pnpm -F @app/web dev`
- Node API: `pnpm -F @app/api-node dev`
- Py API: `uvicorn apps.api_python.app.main:app --reload --port 5000`
- Tests: `pnpm test` / `pytest`

## Feature procedure
1) Open PRD and Tech Spec to select a vertical slice.
2) Request a plan (S1..Sn) from Codex and confirm.
3) For each Sx: apply patch, run commands, verify output.
4) After finishing: run DoD, update Backlog/Spec/PRD, create ADR if needed.

## Diagnostics
- Check .env, migrations, package versions.
- Logs: browser for web, pino for node, uvicorn for python.
- For API breaking changes, follow API Change & Migration Policy.
