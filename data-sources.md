# Clinical Trials Data Sources & Methodology

## Data Sources

### Primary Source
- **ClinicalTrials.gov API**: https://clinicaltrials.gov/api/v2/studies
- **Query Parameters**:
  - Search terms: `prosthetic`, `amputation`, `prosthetic limb`, `prosthetic rehabilitation`
  - Filter: All phases, all countries, all statuses
- **Total Records Retrieved**: 644 studies
- **Data Fields Extracted**: nctId, title, status, phase, sponsor, location, intervention, conditions, outcomes, eligibility, webcond

### Limitations
1. **API Timeout Issues**: Large queries timed out during retrieval. Analysis is based on available subset.
2. **Terminology Variance**: Some prosthetic studies use different condition terminology (e.g., "amputation," "rehabilitation", "joint replacement"). This may undercount total studies.
3. **Status Lag**: "Unknown" status may reflect incomplete reporting rather than actual study abandonment.

## Gap Analysis Data Sources

### OpenStreetMap
- **API**: Overpass API via OSM MCP Server
- **Search Method**: Neighborhood analysis + route directions for three rural regions
- **Search Radius**: 100 km from each center point
- **Categories Queried**: amenity, healthcare, shop, public_transport

### Geocoding
- **Beckley, WV**: 37.78°N, -81.19°W (Raleigh County)
- **Pikeville, KY**: 37.48°N, -82.52°W (Pike County)
- **Greenville, MS**: 33.41°N, -91.06°W (Washington County)
- **Charleston, WV**: 38.35°N, -81.63°W (via route to nearest hub)
- **Memphis, TN**: 35.15°N, -90.05°W (via route to nearest hub)

## Infrastructure Scoring
- **Method**: Neighborhood analysis using OSM features within 50 km radius
- **Categories**: groceries, restaurants, healthcare, education, public_transport, parks, sports, entertainment, shopping, services
- **Score Range**: 0–10 (higher = more features within radius)

## Route Data
- **Method**: OSM Routing API (car mode)
- **Generated**: 2026-07-15
