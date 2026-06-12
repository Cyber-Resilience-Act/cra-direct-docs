# Stateless Scanner API

The stateless scanner API lets clients validate and scan SBOMs or PURL lists without persisting uploaded SBOMs, scan state, triage progress, or evidence.

Use it for demos, preflight checks, and pilot evaluation. Use persistent CRA Direct workflows when you need retained evidence, product-version records, review cases, notifications, Article 14 workflow history, and audit trails.

## Endpoints

| Endpoint | Purpose |
| --- | --- |
| `POST /scan-sbom` | Validate a CycloneDX or SPDX JSON SBOM, extract PURLs, and return vulnerability findings |
| `POST /scan-purls` | Scan a bounded list of Package URLs |
| `POST /triage-stateless` | Run CRA-oriented triage over client-provided findings |

## Example: Scan An SBOM

```bash
curl -X POST "$API_BASE_URL/scan-sbom" \
  -H "Authorization: Bearer $SERVICE_API_KEY" \
  -H "Content-Type: application/json" \
  -H "X-Product-Name: Demo Product" \
  -H "X-Product-Version: 1.0.0" \
  -H "Idempotency-Key: demo-scan-001" \
  --data-binary "@./sbom.json"
```

## Example: Scan PURLs

```bash
curl -X POST "$API_BASE_URL/scan-purls" \
  -H "Authorization: Bearer $SERVICE_API_KEY" \
  -H "Content-Type: application/json" \
  -H "Idempotency-Key: demo-purls-001" \
  -d '{"purls":["pkg:npm/express@4.17.1"]}'
```

## Default Limits

| Limit | Default |
| --- | ---: |
| SBOM request size | 15 MiB |
| SBOM PURLs per request | 10,000 |
| PURL chunk size | 500 |
| PURL request size | 1 MiB |
| Triage request size | 10 MiB |
| Scan and triage timeout | 180 seconds |

## Response Model

Responses include:

- request ID
- status
- product context
- format and version
- component count
- PURL count
- vulnerable component count
- vulnerability findings
- high-risk indicators

## Commercial Upgrade Path

Stateless scanning answers: "What does this SBOM or PURL list show right now?"

The hosted CRA Direct product answers: "What evidence did we retain, who reviewed it, what did we decide, what deadlines apply, what was submitted, and can we prove it later?"

