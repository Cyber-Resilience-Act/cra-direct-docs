# Example: Severe Incident Workflow

This example shows how a product-security team can structure a severe-incident reporting workflow.

## Scenario

The operations team detects a product-security incident with suspected malicious activity. The initial scope is incomplete, but the team has enough evidence to start the reporting workflow.

## Workflow

1. Security team confirms a severe incident affecting product security.
2. Awareness time, source, severity, and suspected malicious cause are recorded.
3. Initial market scope is captured or marked unknown with rationale.
4. A 24-hour early warning case is opened.
5. Reviewer validates initial facts, uncertainty, and sensitivity.
6. Approver confirms the early warning submission.
7. The 72-hour notification expands scope, impact, root-cause understanding, mitigation, and user guidance.
8. The final incident report is prepared after the 72-hour stage according to the applicable final-report window.
9. Every stage is reviewed, approved, submitted, and retained as evidence.

## Evidence To Preserve

- awareness timestamp
- source and source reference
- incident brief
- severity criteria
- suspected malicious or unlawful cause
- affected products and versions
- affected Member States or unknown-scope rationale
- mitigation and restoration evidence
- reviewer and approver history

## Common Failure Modes

- waiting for full certainty before starting the 24-hour workflow
- failing to distinguish known facts from investigation assumptions
- losing history as scope changes
- treating end-user communication as a blocker for SRP filing

