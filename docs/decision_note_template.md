# Decision Note Template

Use decision notes for non-trivial policy, architecture, security, workflow, or process decisions.

Decision notes should preserve intent and review context. They should not include private chain-of-thought or full chat logs.

```markdown
# Decision: <short title>

Date: <YYYY-MM-DD>
Status: Proposed | Accepted | Superseded

## Gap

<What was missing, ambiguous, outdated, or unsafe?>

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
