# Prosthetic Access Atlas — Data Repository

> Structured datasets for prosthetic care access gap analysis and clinical trial landscapes.

## Overview

This is the companion data repository for the Prosthetic Access Atlas. It contains structured datasets, JSON clinical trial records, and raw gap analysis findings.

## Contents

### Clinical Trials Data
- `clinical-trial-landscape.md` — Full status/phase/geographic distribution of 644 prosthetic studies
- `key-studies.json` — Structured JSON for highlighted trials (recruiting & completed)
- `data-sources.md` — Methodology and API references

### Gap Analysis
- `west-virginia.md` — Beckley, WV area prosthetic care gap
- `eastern-kentucky.md` — Pikeville, KY area prosthetic care gap
- `mississippi-delta.md` — Greenville, MS area prosthetic care gap
- `methodology.md` — Data collection and analysis methodology
- `sources.md` — Primary data sources and validation records

### Maps
- `access-disparity-map.md` — Visual gap map with travel distances and access tiers

## Key Statistics

| Metric | Value |
|--------|-------|
| Total prosthetic trials | 644 |
| Currently recruiting | 113 (17.5%) |
| Completed | 271 (42.1%) |
| Unknown status | 134 (20.8%) |
| Gap regions with zero providers | 3 (WV, KY, MS) |
| Maximum drive to nearest care | ~190 min (Greenville → Memphis) |

## Data Quality

- ✅ Live OSM queries for KY and MS (successfully retrieved)
- ⚠️ WV data supplemented (OSM rate-limited)
- ⚠️ ClinicalTrials.gov API timeouts on large queries
- 📋 Recommendation: Quarterly refresh cycle

## License

MIT License

## Generated

2026-07-15