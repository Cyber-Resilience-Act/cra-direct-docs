# Audit Evidence Model

CRA Direct preserves a verifiable record of CRA operations. The audit model is designed for regulatory questions, procurement review, insurance review, and post-incident reconstruction.

## Evidence Features

- hash-chained audit entries
- payload hashes
- workflow and case history
- signed archive envelopes
- WORM-ready object storage path
- short-lived secure file downloads
- exportable audit evidence
- organization-scoped records

## Evidence Questions The System Should Answer

- What product and version was involved?
- Which SBOM evidence set was used?
- What vulnerabilities or incident facts were known?
- What was the awareness timestamp?
- Who reviewed the evidence?
- What decision was approved?
- What payload was submitted?
- Were deadlines met or missed?
- Can the audit chain be verified?

## Why This Matters

Regulatory, insurance, procurement, and post-incident reviews require more than a dashboard. They require evidence that shows what was known, who reviewed it, what was submitted, and when each step occurred.

## Public vs Hosted Boundary

Public tools can validate files and demonstrate stateless scanning. The hosted product retains evidence and audit history across the full workflow lifecycle.

