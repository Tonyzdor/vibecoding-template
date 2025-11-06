# LLM Playbook (Vibecoding)

**Strict Rule:** After each vertical slice, code and docs must be synchronized.

## 1) Ritual of a mini-iteration (vertical slice)
1) Carve out a minimal end-to-end scenario from the PRD.
2) Ask Codex: "First give me a plan of steps (S1..Sn), then code."
3) Execute each step with small diffs and run locally/tests.
4) After finishing Sn: run through DoD, update docs.

## 2) Context policy (Context Pack)
Provide Codex only the relevant context:
- Extracted fragments from `01-Tech-Spec.md` for the specific area.
- The relevant API contracts (OpenAPI or Zod schemas).
- The goal description from the PRD.
- Relevant code snippets; keep within token budget.
Do not feed unrelated files or large blobs.

## 3) Prompt formula
**Input:** A one-paragraph goal + minimal context (list of files/fragments).  
**Request:** "Provide a plan S1..Sn. For S1, give the patch(es), minimal tests and run instructions. Then proceed with S2, etc."  
**Constraints:** Do not change the architecture without a clear reason. Keep type safety. Avoid new dependencies.

## 4) Output contract (mandatory)
The agent must return:
- ✅ A list of modified/new files.
- ✅ Patches or code fragments.
- ✅ Commands to run/tests.
- ✅ TODO items for docs (exact sections/lines to update).

## 5) Anti‑patterns
- Large patches without intermediate runs are forbidden.
- Ignoring tests or contracts is forbidden.
- Silently breaking contracts is forbidden (see API & Migration policy).
