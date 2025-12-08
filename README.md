# Analyzing Dengue Fever in Merida, Mexico (2012–2015)

## Overview
This project analyzes the spatiotemporal patterns of Dengue Fever in Merida, Mexico, using case data from 2012–2015. By leveraging precise spatial coordinates and annual case counts, we aim to identify persistent disease "hotspots" and understand their evolution over time.

This analysis highlights the value of integrating temporal and spatial techniques to uncover patterns of disease persistence, providing a foundation for data-driven public health strategies.

## Research Question
How do dengue fever cases cluster spatially in Merida, Mexico? specifically:
1. How do these spatiotemporal patterns evolve over the 2012-2015 period?
2. How do these dynamics correlate with population density?

## Dataset
The analysis relies on `Merida_Den12_13_14_15.csv`, containing 540 observation locations with:
* **Temporal:** Annual case counts (2012–2015).
* **Spatial:** Precise Latitude/Longitude coordinates.
* **Demographic:** Integrated population density metrics.

## Key Findings
* **Temporal Volatility:** The analysis identified a significant resurgence of cases in **2015**, contrasting with lower transmission years.
* **Spatial Clustering:** Using LISA (Local Indicators of Spatial Association) analysis, we identified statistically significant "hotspots" of infection.
* **Persistence:** Certain zones exhibited persistent high risk across multiple years, suggesting environmental or structural factors driving transmission in those specific neighborhoods.

## Methodology
We conducted a multistage analysis in R:
1.  **Data Cleaning & Exploratory Data Analysis:** Aggregating annual trends to visualize outbreak curves.
2.  **LISA Analysis:** Using Anselin's Local Moran's I (via `spdep`) to identify statistically significant spatial clusters.
3.  **Interactive Mapping:** Utilizing `leaflet` for layered exploration of specific zones and `plotly` for temporal visualization.

## Technologies Used
* **Language:** R
* **Key Libraries:** `tidyverse`, `sf` (spatial vectors), `spdep` (spatial statistics), `leaflet` (interactive maps), `plotly`.

## Project Structure
```text
├── data/                  # Raw dataset (Merida_Den12_13_14_15.csv)
├── renv/                  # Environment settings
├── dengueAnalysis.Rmd     # Main analysis notebook
├── dengueAnalysis.html    # Knitted HTML output
├── renv.lock              # Package version lockfile
├── .Rprofile              # R startup script
└── README.md              # Project documentation
