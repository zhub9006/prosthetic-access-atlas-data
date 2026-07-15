# Methodology

## Data Collection

### Clinical Trial Data
- **Source:** ClinicalTrials.gov API and web search
- **Query:** `condition: prosthetic` with term `prosthetic`
- **Date of search:** July 2025
- **Total records:** 644 unique studies
- **Analysis dimensions:**
  - Status distribution
  - Geographic distribution by country
  - Phase distribution
  - Detailed review of recent/representative studies

### Gap Analysis Data
- **Source:** OpenStreetMap (OSM) via Nominatim API
- **Search method:**
  1. Geocoded region centers using Nominatim
  2. Searched for `healthcare` category amenities within specified radius
  3. Focused on: clinic, doctor, hospital, rehabilitation, physiotherapist, pharmacy
  4. Specifically looked for prosthetic/orthotic tags (none found)

### Region Selection Criteria
1. **Rural designation:** Non-metropolitan counties per U.S. Census Bureau
2. **Prosthetic care deserts:** Areas with no known O&P providers
3. **Health disparity burden:** High rates of diabetes, vascular disease, and trauma-related amputations
4. **Geographic diversity:** Representative of three distinct underserved regions

## Search Parameters

| Region | Center Coordinates | Search Radius | Healthcare Categories |
|--------|--------------------|---------------|-----------------------|
| West Virginia (Charleston) | 38.3506°N, 81.6333°W | 20 km | healthcare (all subcategories) |
| Eastern Kentucky (Pikeville) | 37.4793°N, 82.5188°W | 30 km | healthcare (all subcategories) |
| Mississippi Delta (Greenville) | 33.4111°N, 91.0636°W | 50 km | healthcare (all subcategories) |

## Limitations
- OSM data may not capture all healthcare providers, particularly small private practices
- Proprietary/proprietary O&P companies are not always listed
- Home health agencies providing prosthetic services are not typically in OSM
- The absence of prosthetic-specific tags in OSM means we relied on the absence of relevant search results rather than negative search results
- ClinicalTrials.gov data reflects registered trials, not all real-world prosthetic research

## Validation Recommendations
1. Cross-reference with AAOP (American Academy of Orthotists and Prosthetists) provider directory
2. Verify with state licensing boards for WV, KY, and MS
3. Contact regional amputee coalitions for ground-truth validation
4. Use Medicare/Medicaid provider data for comprehensive O&P practice mapping