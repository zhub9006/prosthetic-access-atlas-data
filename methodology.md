# Gap Analysis Methodology

## Clinical Trials

### Data Source
- **ClinicalTrials.gov API**: https://clinicaltrials.gov/api/v2/studies
- **Search Terms**: `prosthetic`, `amputation`, `prosthetic limb`, `prosthetic rehabilitation`
- **Total Records Retrieved**: 644 studies
- **Data Fields**: nctId, title, status, phase, sponsor, location, intervention, conditions, outcomes, eligibility

### Limitations
1. **API Timeout Issues**: Large queries timed out. Analysis based on available subset.
2. **Terminology Variance**: Some prosthetics studies use different condition terminology.
3. **Volume**: 644 studies across multiple search terms; API timeouts prevented full enumeration

## Geographic Gap Analysis

### Search Method
1. Geocode target city (Beckley, Pikeville, Greenville) using OSM geocoding
2. Run neighborhood analysis within 100 km radius
3. Cross-reference with route directions to nearest hub city (Charleston, WV / Memphis, TN)
4. Identify provider types (prosthetic, orthotic, PM&R, DME, pharmacy)

### Center Points
| Region | City | Latitude | Longitude | Radius |
|--------|------|----------|-----------|--------|
| Rural WV | Beckley | 37.78 | -81.19 | 100 km |
| E. Kentucky | Pikeville | 37.48 | -82.52 | 100 km |
| MS Delta | Greenville | 33.41 | -91.06 | 100 km |
| Hub (WV/KY) | Charleston, WV | 38.35 | -81.63 | N/A |
| Hub (MS) | Memphis, TN | 35.15 | -90.05 | N/A |

### Provider Categories Queried
- ✅ Hospital (with prosthetics department)
- ✅ Prosthetic/Orthotic clinic
- ✅ PM&R / Physiatrist
- ✅ DME supplier
- ✅ Pharmacy (with prosthetics supply)
- ⚠️ General clinic (no prosthetics)
- ❌ None found

### Infrastructure Scoring
- **Method**: Neighborhood analysis using OSM features within 50 km radius
- **Categories**: groceries, restaurants, healthcare, education, public_transport, parks, sports, entertainment, shopping, services
- **Score Range**: 0–10 (higher = more features within radius)

## Route Data
- **Method**: OSM Routing API (car mode, fastest route)
- **Beckley → Charleston**: 95 km / 59 mi / 76 min
- **Pikeville → Charleston**: 173 km / 108 mi / 127 min
- **Greenville → Memphis**: 241 km / 150 mi / 190 min

## Limitations & Caveats

1. **OSM completeness**: Private O&P clinics may not maintain OSM entries. Absence suggests a gap but does not prove non-existence. Recommend follow-up with state O&P associations.
2. **ClinicalTrials.gov scope**: The API may not index all prosthetics-related trials. Some use different condition terminology (e.g., "amputation," "rehabilitation").
3. **Geographic resolution**: OSM point-center searches may miss providers in adjacent counties. Recommend expanding radius for follow-up searches.
4. **Temporal validity**: OSM data is community-edited and may be outdated. Recommend re-running searches quarterly.
5. **West Virginia limitation**: Live OSM nearby search was rate-limited; WV data was supplemented with known state infrastructure and should be verified.
6. **Race/ethnicity data**: Available from CDC but not included in OSM gap analysis.

## Data Freshness
- **Generated**: 2026-07-15
- **Recommended refresh**: Quarterly
- **Next update**: Fall 2026
