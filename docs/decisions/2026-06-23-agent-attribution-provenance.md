# Decision: Treat Agent Attribution As Provenance

Date: 2026-06-23
Status: Accepted
Review Status: self_checked

## Context

The constitution already covered provenance, accountability, identity-sensitive governed decisions, and reviewable breadcrumbs. It did not explicitly say that durable authorship metadata is provenance.

## Gap

Agents may inherit a human identity from local execution context, such as an OS account, Git config, browser session, token, checkout, or editor profile. Without a clear rule, agent-produced work could be committed, published, reviewed, or generated under a human identity that did not perform or approve that work.

## Governed Decision Record

- decision_question: Should the constitution treat durable agent attribution metadata as provenance?
- decision_type: high
- recommendation: Treat durable authorship metadata as provenance, require truthful project-approved attribution, and make public or hard-to-reverse corrections governed decisions.
- evidence_consulted: `docs/provenance_and_breadcrumbs.md`, `docs/governed_decisions.md`, `docs/security_models.md`, `docs/threat_model.md`, `docs/glossary.md`, `docs/repo_adoption_template.md`, `templates/project_AGENTS.md`, `templates/pr_checklist.md`, and user-supplied gap statement.
- assumptions: Projects need flexibility to choose their own identity convention.
- missing_evidence: No single identity scheme is selected for all adopters.
- risks: Over-mandating one identity model, silently rewriting public history, or leaving passive humans misattributed in durable records.
- reversibility: Moderate for doctrine edits; hard for public or merged attribution records in adopting projects.
- confidence: high, based on the existing provenance, integrity, identity, and governed-decision doctrine.
- review_triggered: self_check
- challenge_summary: The rule could become tool-specific or incident-specific; it is kept general and leaves the concrete identity convention to each project.
- final_judgment: allow
- follow_up_actions: Adopting projects should define their approved agent identity convention locally.

## Decision

Durable authorship metadata is provenance. This includes Git author and committer fields, PR authors, issue actors, release publishers, generated report authors, co-authorship trailers, review or sign-off trailers, and similar durable records.

Agent-produced work must use truthful, project-approved attribution. Agents must not silently inherit or reuse a human identity merely because they run under that person's local account, Git config, browser session, token, checkout, editor profile, or similar execution context.

## Rationale

Bad attribution corrupts audit trails and can impersonate passive humans by making them appear to have authored, committed, published, reviewed, or generated work they did not perform or approve. This is a provenance and integrity failure, not a harmless credit issue.

## Guardrail

Before opening, merging, publishing, or releasing agent work, verify durable authorship metadata when practical. If unmerged or unpublished work has wrong attribution, repair only the affected scope and record old and new object IDs or durable references. If wrong attribution is already public, merged, released, or hard to reverse, treat correction as a governed decision and preserve an audit trail rather than silently rewriting history.

## Validation

Review that the added doctrine stays general, preserves the authority and evidence boundary, aligns templates with the doctrine, and does not mandate one universal identity scheme.

## Unchanged

The constitution does not mandate one attribution mechanism. Projects may choose role accounts, service accounts, human review trailers, co-authorship trailers, stricter release conventions, or another explicit local convention.

## Follow-Up

No package metadata, automation, identity provider integration, Git hook, or release workflow is added by this decision.
