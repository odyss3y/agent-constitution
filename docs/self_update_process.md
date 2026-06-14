# Self-Update Process

Governing docs should improve when they fail to guide real work. They should not become bloated transcripts of every incident.

## When To Propose An Update

Propose a narrow update when:

- A new failure mode or ambiguity is discovered.
- Repeated agent confusion shows a rule is unclear.
- Repo docs drift from actual behavior.
- A safety boundary is missing.
- Process debt makes future work less auditable.

## Requirements

A self-update must be:

- Explicit: name the gap and the proposed rule.
- Reviewable: small enough to inspect as a normal diff.
- Narrow: address the underlying constraint without broad policy expansion.
- Conservative: preserve previous intent unless explicitly changed.
- Non-private: do not dump chat transcripts, private reasoning, or chain-of-thought.
- Actionable: include the guardrail future agents should apply.

## Decision Record

For non-trivial updates, create or update a decision note with:

- Gap: what was missing or ambiguous.
- Decision: what rule or policy changed.
- Rationale: why this preserves the constitution.
- Guardrail: what future agents should do differently.
- Follow-up: what remains unresolved or deferred.

Use `templates/decision_note.md` or the shorter form in `docs/decision_note_template.md`.

## Anti-Bloat Rules

- Do not add a new rule for every one-off incident.
- Do not quote large logs or chat history.
- Do not preserve private reasoning.
- Do not encode tool-specific quirks unless the repo truly depends on that tool.
- Do not weaken authority, evidence, reversibility, or provenance boundaries for convenience.

The goal is a stable governing layer that can learn without becoming brittle.
