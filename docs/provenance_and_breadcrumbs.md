# Provenance and Breadcrumbs

Provenance is the traceable origin and reason for a change. Breadcrumbs are compact notes that preserve the intent and constraints future maintainers need.

Breadcrumbs preserve review context. They do not preserve private chain-of-thought, full chat logs, or every intermediate mistake.

## What To Record

For meaningful changes, record:

- What changed.
- What intentionally did not change.
- Why the change was made.
- Validation performed.
- Semantics or invariants preserved.
- Deferred work.
- Follow-up guardrails.

For governed artifacts that may become stale, add only the provenance needed to make review possible. Useful fields include `constitution_version`, `generated_at`, `reviewed_at`, `evidence_files`, and `review_status`.

## Where To Record It

Use the smallest durable location that fits the change:

- Commit message or PR description for normal implementation context.
- Decision note for policy, architecture, security, or workflow tradeoffs.
- Issue handoff for ongoing work.
- Changelog or release note only when the change affects users.

## Good Breadcrumbs

Good breadcrumbs are:

- Short enough to review.
- Specific enough to verify.
- Clear about uncertainty.
- Clear about non-goals.
- Tied to evidence, tests, or docs.

## Bad Breadcrumbs

Avoid:

- Full transcripts.
- Private reasoning.
- Vague claims such as "improved safety" without mechanism.
- Unverified claims from model output or external pages.
- Retconning assumptions as observed facts.

The goal is continuity without leaking private reasoning or burying future maintainers in noise.
