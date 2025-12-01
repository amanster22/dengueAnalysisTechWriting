# Analyzing Dengue Fever in Merida, Mexico (2012–2015)

Overview

This project analyzes the spatiotemporal patterns of dengue fever in Merida, Mexico using case data from 2012–2015. By leveraging precise spatial coordinates, we aim to identify persistent disease "hotspots" and understand their evolution and relationship with population density.

Research Question

How do dengue fever cases cluster spatially in Merida, Mexico, how do these spatiotemporal patterns evolve over the 2012-2015 period, and how do these dynamics correlate with population density?

Dataset

Analysis relies on Merida_Den12_13_14_15.csv, containing 540 observation locations with:

Temporal: Annual case counts (2012–2015).

Spatial: Precise X/Y coordinates.

Demographic: Integrated population density metrics.

Methodology

We employ a multistage analysis in R:

Data Cleaning: Aggregating annual trends to visualize outbreaks.

Kernel Density Estimation (KDE): creating animated maps to visualize shifting hotspot intensity.

LISA Analysis: Using Anselin's Local Moran's I to identify statistically significant clusters.

Demographic Correlation: linking disease clusters to population density.

Interactive Mapping: using leaflet for layered exploration of specific zones.

Tech Stack

Language: R

Key Libraries: leaflet (mapping), plotly (animation), spdep (spatial statistics), sf (vector data), tidyverse (data manipulation).
