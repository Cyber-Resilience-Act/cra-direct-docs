# Example: SBOM Upload Workflow

This example shows how a CI/CD pipeline can feed SBOM evidence into a CRA operations process.

## Scenario

An engineering team releases product version `1.2.3` and generates a CycloneDX or SPDX SBOM during the build.

## Workflow

1. Product and version are registered in the CRA workspace.
2. CI/CD generates CycloneDX or SPDX SBOM output.
3. SBOM is validated before upload.
4. A service key uploads the SBOM evidence set.
5. CRA Direct binds the upload to the selected product version.
6. Raw files are archived and content hashes are retained.
7. Normalized component records are created.
8. The evidence set is locked.
9. Baseline analysis is queued.
10. Findings and review cases are linked back to the product version.

## Example Upload

```bash
curl -X POST "$API_BASE_URL/ingest-sbom?queue_analysis=true" \
  -H "Authorization: Bearer $SERVICE_API_KEY" \
  -H "X-Product-Id: $PRODUCT_ID" \
  -F "version=$PRODUCT_VERSION" \
  -F "files=@./sbom.json;type=application/json"
```

## Evidence To Preserve

- product ID
- product version
- SBOM file names and hashes
- schema format and version
- upload actor or service key
- upload timestamp
- analysis job reference
- validation failures, if any

## Common Failure Modes

- generating SBOMs without mapping them to registered product versions
- overwriting previous evidence instead of retaining immutable release evidence
- accepting metadata version mismatches silently
- treating a successful scan result as evidence retention

