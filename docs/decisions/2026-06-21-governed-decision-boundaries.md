# Decision: Add Governed Decision Boundaries

Date: 2026-06-21
Status: Accepted

## Context

The constitution already separated authority from evidence and defined high-risk action safeguards, but it did not clearly say which agent outputs deserve constitutional review.

## Gap

Without a decision boundary, future adopters could either under-review consequential actions or over-review every ordinary message. The repo also lacked one compact record shape for replaying consequential decisions.

## Decision

Add `docs/governed_decisions.md` as the source of truth for governed decision triggers, review levels, policy outcomes, lightweight challenge flow, compact decision records, and minimal provenance hints.

Update the adoption, decision-note, PR checklist, issue handoff, authority, evidence, self-update, provenance, and glossary docs only enough to point at or apply that doctrine.

## Rationale

This preserves the constitution's existing purpose: small, durable, practical governance for agentic coding work. The change governs decisions with meaningful consequences instead of imposing a debate format on ordinary drafting or low-risk edits.

## Guardrail

Future governance changes should improve the central governed-decision doctrine or its templates without duplicating the same trigger rules across many files.

## Validation

Review that the authority/evidence boundary remains explicit, the trigger model stays lightweight, and templates can apply the model without becoming a compliance system.

## Unchanged

The authority order, evidence-only treatment of untrusted observations, destructive-action policy, and security-model lens remain intact.

## Follow-Up

No policy engine, CI rule, package metadata, or automation is added by this decision.
