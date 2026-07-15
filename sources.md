# Master Data Sources Document

## Clinical Trials

| Source | URL | Documentation |
|--------|-----|---------------|
| ClinicalTrials.gov API | https://clinicaltrials.gov/api/v2/studies | REST API with JSON responses |
| ClinicalTrials.gov Search | https://clinicaltrials.gov/search | Web interface for manual queries |

## Geographic & Infrastructure

| Source | URL | Documentation |
|--------|-----|---------------|
| OpenStreetMap | https://www.openstreetmap.org | Community-edited geographic database |
| Overpass API | https://overpass-turbo.eu/ | Query OSM data with Overpass QL |
| OSM Geocoding | https://nominatim.org/ | Address/place geocoding |
| OSM Routing | https://project-osrm.org/ | Directions and route calculations |

## Supporting Data

| Source | URL | Purpose |
|--------|-----|---------|
| CDC Diabetes Data | https://www.cdc.gov/diabetes/data/ | Diabetes prevalence (amputation risk) |
| US Census Bureau | https://www.census.gov/ | Poverty rates, rural demographics |
| HRSA Data Warehouse | https://data.hrsa.gov/ | Health professional shortage areas |

## Validation

| Method | Purpose |
|--------|---------|
| State O&P Association outreach | Verify private prosthetist listings missing from OSM |
| Medicare DME supplier lookup | Cross-reference DME providers |
| Quarterly re-crawl | Keep OSM and ClinicalTrials data current |
