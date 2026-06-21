# Decision Note Template

Use decision notes for non-trivial policy, architecture, security, workflow, or process decisions.

Decision notes should preserve intent and review context. They should not include private chain-of-thought or full chat logs.

```markdown
# Decision: <short title>

Date: <YYYY-MM-DD>
Status: Proposed | Accepted | Superseded
Review Status: draft | self_checked | challenged | approved | blocked

## Gap

<What was missing, ambiguous, outdated, or unsafe?>

## Decision Record

- decision_question: <What is being decided?>
- decision_type: low | standard | high | critical
- recommendation: <Proposed action or judgment>
- evidence_consulted: <Observed facts, files, commands, diffs, tests, or cited sources>
- assumptions: <Unverified premises>
- missing_evidence: <Evidence that would improve or change judgment>
- risks: <Risk, failure mode, or trust concern>
- reversibility: <easy | moderate | hard | irreversible, with note>
- confidence: <low | medium | high, tied to evidence>
- review_triggered: none | self_check | challenge | human_approval
- challenge_summary: <Main objection and response>
- final_judgment: allow | warn | require_approval | deny | escalate | log_only
- follow_up_actions: <Next validation, owner question, or deferred work>

## Decision

<What changed?>

## Rationale

<Why this preserves the project's purpose, constraints, and reviewability?>

## Guardrail

<What should future agents or maintainers do differently?>

## Validation

<What was checked, tested, or reviewed?>

## Follow-Up

<What remains deferred or unresolved?>
```

Keep the note compact. If the decision only affects one PR, the PR description may be enough.
