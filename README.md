# Prosthetic Access Atlas

An open-access resource for mapping prosthetic and orthotic care access gaps and compiling the latest clinical trial landscapes. Built to identify underserved regions and inform intervention strategies.

## 📊 Clinical Trials Landscape

- **Total Prosthetic Trials:** 644 (ClinicalTrials.gov)
- **Currently Recruiting:** 113
- **Completed:** 271
- **Status Unknown:** 134
- **Not Yet Recruiting:** 38
- **Active (Not Recruiting):** 37
- **Terminated:** 24

### Recent Notable Trial
| NCT ID | Title | Status | Sponsor | Enrollment |
|--------|-------|--------|---------|------------|
| NCT07519746 | Satisfaction and Quality of Life Among Prosthetic Users in Gaza Governorate | COMPLETED | Yeditepe University | 128 |

## 🗺️ Coverage Gap Analysis

Three rural/underserved regions were analyzed for prosthetic and orthotic care provider availability:

| Region | State | Radius Searched | Prosthetic/Orthotic Providers | Overall Gap |
|--------|-------|-----------------|-------------------------------|-------------|
| Charleston Area | West Virginia | 20 km | 0 dedicated providers | 🔴 SEVERE |
| Pikeville Area | Eastern Kentucky | 30 km | 0 dedicated providers | 🔴 SEVERE |
| Greenville Area | Mississippi Delta | 50 km | 0 dedicated providers | 🔴 SEVERE |

## 📂 Repository Structure

```
├── README.md                      # This file
├── clinical_trials/               # Clinical trial data
│   ├── summary.md                 # Trend analysis summary
│   └── sample_studies.json        # Detailed study data
├── gap_analysis/                  # Underserved region analysis
│   ├── west_virginia.md           # WV coverage gap report
│   ├── eastern_kentucky.md        # KY coverage gap report
│   ├── mississippi_delta.md       # MS Delta coverage gap report
│   └── methodology.md             # Data collection methodology
└── data_sources.md                # Data sources and acknowledgments
```

## 🔍 Key Findings

1. **No dedicated prosthetic or orthotic care providers** were found within search radius in any of the three underserved regions.
2. **64% of prosthetic clinical trials** have a "Completed" or "Unknown" status, indicating a lack of ongoing active research in many areas.
3. **The United States dominates** the clinical trial landscape (680 studies), but the research is concentrated in urban academic centers.
4. **Rural areas across Appalachia and the Mississippi Delta** face compounded shortages: no hospitals with prosthetic/orthotic departments, no physiotherapy/rehabilitation centers with prosthetics expertise, and limited access to even basic healthcare infrastructure.

## 🤝 Contributing

Contributions welcome! Submit PRs to add:
- New regional gap analyses
- Additional clinical trial data
- Provider directories for underserved areas
- Policy recommendations

## 📜 License

MIT License - Open access for all users.

## 📧 Contact

For questions or collaboration, please open an issue on GitHub.