# Repo Adoption Template

This page explains how a project can adopt the Agent Constitution.

Project-specific rules may narrow or specialize this constitution. They must not weaken safety, provenance, reversibility, authority boundaries, or evidence handling.

## Adoption Steps

1. Copy `templates/project_AGENTS.md` into the target repo as `AGENTS.md`.
2. Fill in project purpose, core invariants, trusted docs, commands, tests, and destructive-action constraints.
3. Identify untrusted input boundaries specific to the project.
4. Add a compact security-model review lens for confidentiality, integrity, availability, least privilege, and fail-safe defaults.
5. Define governed-decision triggers and policy outcomes for the project.
6. Define validation expectations for normal changes.
7. Define when decision notes are required.
8. Keep local policy concise and update it when actual practice drifts.

## Minimal Import Language

```markdown
This project adopts the Agent Constitution by principle.

Project-specific instructions may narrow or specialize those rules, but must not
weaken authority boundaries, evidence handling, reversibility, provenance, or
reviewability.
```

## Project-Specific Fields

A useful project `AGENTS.md` should name:

- Project purpose.
- Core invariants.
- Authority order.
- Trusted docs to read.
- Commands and tests.
- Destructive action constraints.
- Untrusted input boundaries.
- Security-model review lens.
- Governed decision triggers and policy outcomes.
- Validation expectations.
- Decision-note policy.

## Adoption Review

Before considering adoption complete, verify:

- The project names its trusted authority sources.
- Untrusted observations are explicitly classified as evidence only.
- CIA, Biba/integrity, Bell-LaPadula/confidentiality flow, Clark-Wilson/reviewable mutation, least privilege, and fail-safe defaults are operational rather than academic.
- Destructive and high-risk actions require explicit scope and review.
- Ordinary drafting, explanation, brainstorming, and low-risk edits are not over-governed.
- High or critical governed decisions require challenge, approval, or escalation as appropriate.
- Validation commands are current.
- Decision-note expectations are clear.
- The template does not contain placeholders that future agents must guess.
