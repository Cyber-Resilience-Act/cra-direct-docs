# CRA Direct Documentation

Public documentation for CRA Direct, a Cyber Resilience Act operations platform for software manufacturers.

CRA Direct helps product-security, engineering, and compliance teams move from ad hoc spreadsheets and ticket comments to structured SBOM evidence, vulnerability affectedness review, Article 14 workflows, notifications, and audit trails.

> Independent project notice: this repository is not affiliated with, endorsed by, or operated by the European Union, ENISA, any CSIRT, or any market surveillance authority.

## Who This Is For

- software manufacturers preparing for the EU Cyber Resilience Act
- product-security teams responsible for SBOM and vulnerability operations
- compliance teams designing Article 14 reporting processes
- auditors and technical reviewers evaluating evidence quality
- engineering teams integrating SBOM upload and vulnerability scanning into CI/CD

## Read First

| Document | Use it for |
| --- | --- |
| [Overview](docs/overview.md) | Understand the CRA Direct operating model |
| [Article 14 Workflows](docs/article-14-workflows.md) | Map awareness, 24h, 72h, final, and intermediate reporting |
| [SBOM Evidence Model](docs/sbom-evidence-model.md) | Design product-version SBOM evidence handling |
| [Stateless Scanner API](docs/stateless-scanner-api.md) | Evaluate the public stateless scanner endpoints |
| [HITL Review Model](docs/hitl-review-model.md) | Structure reviewer, approver, and auditor workflows |
| [Audit Evidence Model](docs/audit-evidence-model.md) | Understand verifiable evidence and non-repudiation |
| [Readiness Assessment](docs/readiness-assessment.md) | Run a practical gap review before a pilot |

## Public Tools vs Hosted Product

The public Cyber Resilience Act repositories provide validation tools, API examples, demo apps, and implementation guidance.

The hosted CRA Direct product adds the operational system of record:

- persistent product and version records
- SBOM evidence retention
- continuous vulnerability intelligence monitoring
- VEX and affectedness review
- human-in-the-loop approval workflows
- Article 14 vulnerability and severe-incident reporting
- notifications and deadline management
- audit evidence and exportable history

## Related Public Repositories

- `cra-stateless-scanner-demo`: demo app for trying stateless SBOM scanning and CRA triage
- `cra-sbom-validator`: offline CycloneDX and SPDX SBOM validator
- `cra-api-examples`: curl, GitHub Actions, Node, and Python API examples

## Commercial Support

CRA Direct is available as a hosted SaaS and consulting service.

For pilots, integrations, and CRA readiness support, contact: contact@cra-direct.fr

