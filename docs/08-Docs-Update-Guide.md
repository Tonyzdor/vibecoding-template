# Docs Update Guide

## When
- Any changes to public contracts, data models, or behavior.
- After completing each vertical slice.

## What
- PRD — if the value/features change.
- Tech Spec — architecture, schemas, contracts, NFR.
- Backlog — statuses/priorities.
- ADR — any important decision.

## How not to forget
- In every patch, the agent must return TODO for docs (see Playbook "Contract of output").
- (Optional) local hook `scripts/verify-docs.sh`.

## Commit format
- In the description include `[docs]` and list the updated files.
