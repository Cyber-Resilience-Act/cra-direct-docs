# CRA Readiness Assessment

Use this checklist to identify whether a team is ready to operate CRA reporting workflows.

This is not a legal compliance assessment. It is an operational readiness assessment for product-security, engineering, and compliance teams.

## Product Records

- Products are registered with clear owners.
- Active product versions are tracked.
- Deprecated and end-of-life versions are visible.
- Support period end dates are known.
- Security contacts are assigned.
- Vulnerability disclosure policy URLs are maintained.
- Market scope and establishment/routing information are known.

## SBOM Evidence

- SBOM generation exists in CI/CD.
- CycloneDX or SPDX output is validated.
- SBOMs are mapped to product versions.
- Raw SBOM files are retained.
- Content hashes are stored.
- Duplicate and incomplete submissions are rejected.
- Version mismatches require explicit acknowledgement.

## Vulnerability Operations

- Vulnerability intelligence sources are defined.
- CISA KEV or equivalent active-exploitation signals are monitored.
- EPSS and CVSS are used as prioritization signals, not standalone reporting triggers.
- Affectedness decisions can be recorded.
- VEX evidence can be reviewed and amended.
- Supplier or maintainer context can be captured.

## Reporting Operations

- Awareness timestamps are captured.
- 24-hour and 72-hour deadlines are tracked.
- Final-report anchor events are tracked.
- Reviewers and approvers are assigned.
- Submission payloads are validated.
- Failed submissions are visible.
- Retry behavior is documented.
- Intermediate report requests can be handled.

## Audit And Evidence

- Reviewer and approver actions are recorded.
- Payload versions are retained.
- Audit entries are hash-linked or otherwise tamper-evident.
- Evidence can be exported.
- Access to audit evidence is role-scoped.

## Pilot Entry Criteria

A good CRA Direct pilot candidate usually has:

- at least one product with an SBOM
- a product-security or compliance owner
- a CI/CD or release process that can produce SBOM artifacts
- an internal workflow for vulnerability review
- a need to demonstrate evidence quality to customers, auditors, or regulators

