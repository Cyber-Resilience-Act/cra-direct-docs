# Human-In-The-Loop Review Model

CRA Direct keeps legally meaningful decisions under human control. Automation prepares evidence and drafts, but reviewer and approver actions determine the final operational decision.

## Review Roles

| Role | Responsibility |
| --- | --- |
| Reviewer | Inspects evidence, edits drafts, records affectedness, and prepares submissions |
| Approver | Confirms final readiness before submission or closure |
| Auditor | Reviews read-only evidence, payload history, and audit trails |
| Administrator | Manages workspace readiness, users, products, contacts, and service keys |

## Case Types

- VEX triage cases
- SRP stage submission cases
- intermediate report cases
- dissemination-delay requests
- external action confirmation cases

## Review Lifecycle

```text
Open
  -> in review
  -> draft generated or amended
  -> ready for approval
  -> approved, rejected, or changes requested
  -> submitted or closed
  -> preserved in audit history
```

## VEX And Affectedness

For vulnerability findings, reviewers can record product-specific affectedness evidence:

- affected
- not affected
- fixed
- under investigation
- report
- monitor

AI or scanner output can assist the review, but it should not silently close legally meaningful decisions without human evidence.

## Why This Matters

The CRA operating problem is not only finding CVEs. Teams must show who made the affectedness decision, what evidence was used, whether a report was required, what was approved, and what was submitted.

