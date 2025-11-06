# Tech Spec (Lite)

## A. Architecture (one diagram/paragraph)
web → api-node / api-python → db (Postgres). Contracts (REST/tRPC), data flow diagram.

## B. Data model (minimum)
Entities → fields → relations. Link to migrations/ORM.

## C. API contracts (source of truth)
Where it lives: OpenAPI (python) / Zod schemas (node). How to generate clients.

## D. Security
AuthN/Z (if needed), CORS, rate-limit, secrets (see extras/11).

## E. NFR/Observability
Budgets (latency/throughput). What we log/measure (see extras/12).

## F. Extension points
Where to safely add features. Folders/modules, principles.

## G. ADR
Link to docs/04-ADR/index.md.
