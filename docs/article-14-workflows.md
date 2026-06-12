# Article 14 Workflows

CRA Direct models Article 14 operations as controlled workflows from awareness to final evidence. The goal is to make deadlines, required fields, decisions, and audit history explicit instead of spreading them across email, spreadsheets, and ticket comments.

## Awareness

Every workflow starts with an awareness event:

- an actively exploited vulnerability affecting a product with digital elements
- a severe incident affecting product security

CRA Direct records the awareness timestamp, source, product, version, market scope, and known evidence. The awareness timestamp anchors the 24-hour and 72-hour reporting windows.

## Vulnerability Workflow

For reportable vulnerabilities, CRA Direct supports:

- 24-hour early warning
- 72-hour notification
- final vulnerability report after mitigation availability
- active-exploitation evidence
- product-specific affectedness evidence
- supplier or maintainer context
- SBOM linkage where applicable
- VEX review and amendment history

Severity alone is not treated as a reporting trigger. Active exploitation and product affectedness are handled as distinct evidence questions.

## Severe Incident Workflow

For severe incidents, CRA Direct supports:

- 24-hour early warning
- 72-hour notification
- final incident report
- incident brief and severity criteria
- suspected malicious or unlawful cause
- scope and market-impact tracking
- mitigation and restoration evidence

## Intermediate Reports

When a CSIRT coordinator or competent authority requests an update, CRA Direct can open an intermediate-report review case against an existing workflow. Intermediate reports do not reset or extend the original 24-hour, 72-hour, or final-report obligations.

## Review And Approval

Submission stages are routed through human review before filing.

```text
Draft generated
  -> reviewer checks evidence and payload
  -> reviewer submits for approval
  -> approver approves or requests changes
  -> approved payload is submitted
  -> payload and decision are preserved in audit history
```

## Deadline Handling

CRA Direct tracks:

- 24-hour early warning deadlines
- 72-hour notification deadlines
- final vulnerability deadlines after mitigation availability
- final incident deadlines
- intermediate report due dates
- reviewer and approver due dates
- failed submission and retry states

Retry behavior is deadline-aware so transient infrastructure failures remain visible and actionable instead of disappearing inside a background job.

