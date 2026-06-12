# SBOM Evidence Model

CRA Direct treats SBOMs as compliance evidence, not temporary scanner input. The product-version SBOM set is the baseline for vulnerability analysis, affectedness review, and later audit questions.

## Supported Formats

- CycloneDX 1.4 through 1.7
- SPDX 2.2 JSON
- SPDX 2.3 JSON
- SPDX 3.0.1 JSON-LD

## Evidence Flow

```text
CI/CD or manual upload
  -> schema validation
  -> product/version binding
  -> duplicate detection
  -> raw evidence archival
  -> normalized component inventory
  -> locked evidence set
  -> scanner and review workflows
```

## Evidence Rules

- SBOMs are uploaded against registered product versions.
- A complete product-version evidence set can include multiple files.
- Files are validated before ingestion.
- Duplicate files inside one submission are rejected.
- Evidence sets are locked after upload.
- Content hashes are retained for traceability.
- Raw files are archived to object storage.
- Later vulnerability-intelligence changes create separate analysis context rather than silently mutating the original baseline.

## Product-Version Binding

The selected product and version are authoritative. SBOM metadata can help identify the artifact, but it should not silently override the registered product-version record.

If SBOM metadata declares a different version than the selected registered product version, the caller must explicitly acknowledge the mismatch.

## Why This Matters

When a regulator, customer, insurer, or auditor asks what was known about a product release, the team needs more than a scan result. It needs the SBOM input, component inventory, hashes, analysis history, review decisions, and submission history tied together.

