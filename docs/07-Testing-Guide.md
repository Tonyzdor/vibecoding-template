# Testing Guide

## Pyramid
unit → integration → e2e (narrow critical path).

## Base (always)
- Contracts: validate input/output.
- Business branches: happy/errors.
- Migrations: can be applied/rolled back.

## Stack-specific tests
- Web: Jest + React Testing Library (see tests/unit/web).
- Node: Jest/Supertest (tests/unit/api-node).
- Python: Pytest + TestClient (tests/unit/api-python).
- E2E: Playwright/Cypress — home page + /health.

## Reports
- Save coverage as artifact, failures are in logs.
