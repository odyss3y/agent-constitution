# Provenance and Breadcrumbs

Provenance is the traceable origin and reason for a change. Breadcrumbs are compact notes that preserve the intent and constraints future maintainers need.

Breadcrumbs preserve review context. They do not preserve private chain-of-thought, full chat logs, or every intermediate mistake.

Durable authorship metadata is provenance. Git author and committer fields, PR authors, issue actors, release publishers, generated report authors, co-authorship trailers, review or sign-off trailers, and similar metadata describe who or what produced, reviewed, or published work.

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

For attribution repairs, record the affected scope, the old and new object IDs or durable references when they exist, the publication state of the affected work, and the validation performed.

## Agent Attribution

Agent-produced work must use truthful, project-approved attribution. An agent must not silently inherit or reuse a human identity merely because it is running under that person's local account, Git config, browser session, token, checkout, editor profile, or similar execution context.

Passive-human misattribution is unsafe. It can corrupt audit trails by making a person appear to have authored, committed, published, reviewed, or generated work they did not perform or approve.

Before opening, merging, publishing, or releasing agent work, verify durable authorship metadata when practical. Check the metadata that will persist for the target surface, such as commit author and committer fields, PR or issue actors, release publisher, generated report author fields, co-authorship trailers, and review or sign-off trailers.

Projects should define their approved agent identity convention locally. A project may use role accounts, service accounts, human review trailers, co-authorship trailers, stricter release rules, or another reviewable scheme, but the chosen convention should be explicit.

## Repairing Attribution

If unmerged or otherwise unpublished agent work has wrong attribution, repair only the affected scope and record old and new object IDs or durable references. Keep the operation narrow, reviewable, and validated.

If wrong attribution is already public, merged, released, or hard to reverse, treat correction as a governed decision. Preserve an audit trail and avoid silent history rewrite. Use the project's chosen correction path, such as a follow-up commit, release note, issue or PR note, reviewed history rewrite, or other explicit provenance repair.

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
