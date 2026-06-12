# CRA Direct Overview

CRA Direct is an operations platform for software manufacturers preparing for EU Cyber Resilience Act readiness. It focuses on the work that must be repeatable, reviewable, and evidenced: product records, SBOM evidence, vulnerability intelligence, affectedness decisions, Article 14 reporting workflows, notifications, and audit history.

The platform is designed around one operating principle: automation can prepare, prioritize, validate, remind, and submit, but legally meaningful decisions stay under human control and are preserved in an audit trail.

## Operating Model

```text
Product/version registry
  -> SBOM evidence upload
  -> vulnerability intelligence and scanning
  -> CRA-oriented triage
  -> VEX / affectedness review
  -> Article 14 workflow
  -> reviewer and approver gates
  -> submission, notification, and audit evidence
```

## Core Capabilities

- organization-scoped workspaces
- product and version registry
- CycloneDX and SPDX SBOM evidence validation
- immutable product-version evidence sets
- vulnerability intelligence enrichment
- active-exploitation and affectedness-oriented triage
- VEX evidence and human review
- Article 14 vulnerability and severe-incident workflows
- intermediate report and dissemination-delay support
- deadline-aware notifications
- hash-chained audit events and evidence export

## Primary Users

| User | Main responsibility |
| --- | --- |
| Security reviewer | Investigates findings, records VEX evidence, prepares draft decisions |
| Approver | Confirms legally meaningful submissions and decisions |
| Auditor | Reviews evidence, payload history, and audit chain integrity |
| Organization administrator | Manages products, service keys, contacts, and workspace readiness |
| Engineering team | Automates SBOM upload and scanner integration |

## What CRA Direct Is Not

CRA Direct is not legal advice, certification, or a guarantee of compliance. It is a technical and operational platform that helps teams implement repeatable processes, preserve evidence, and manage regulated workflows.

## Commercial Boundary

The public repositories demonstrate validation, stateless scanning, and integration patterns. The hosted product is the system of record for persistent evidence, review cases, notifications, Article 14 workflows, and audit trails.

