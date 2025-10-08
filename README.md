Fanjingshan-PLUS-Simulation

This repository contains the simulation outputs and visualization results from the study “Multi-scenario land-use change simulation with PLUS: Evidence from the Fanjingshan Region.”

📘 Overview

The data represent baseline and projected land-use/land-cover (LULC) patterns for the Fanjingshan Region, a UNESCO World Heritage Site and biodiversity hotspot in southwestern China.
Simulations were conducted using the Patch-generating Land Use Simulation (PLUS) model to explore alternative land-use futures for the year 2032 under three development and protection scenarios.

📂 Repository Structure
Fanjingshan-PLUS-Simulation/
│
├── baseline/          # 2022 baseline LULC raster (reference year)
│
├── S1/                # Natural Development Scenario (NDS)
│   └── landuse_2032_S1.tif
│
├── S2/                # Cropland Protection Scenario (CPS)
│   └── landuse_2032_S2.tif
│
├── S3/                # Ecological Priority Scenario (EPS)
│   └── landuse_2032_S3.tif
│
└── pareto_2d/         # Two-dimensional Pareto evaluation of ecological-development trade-offs
    ├── pareto_plot.png
    └── pareto_metrics.csv

🧭 Data Description
Folder	Contents	Description
baseline	2022 baseline land-use map	Reference map derived from observed data (CAS 30 m dataset).
S1	NDS projection (2032)	Simulates natural development trends with minimal policy constraints.
S2	CPS projection (2032)	Enforces cropland protection policies; limits urban expansion.
S3	EPS projection (2032)	Prioritizes ecological conservation and forest connectivity.
pareto_2d	Pareto front results	Quantitative trade-off evaluation using ΔED, ΔCONTAG, and ΔImp.

All rasters are 30 m resolution and projected to CGCS2000 / Gauss–Kruger Zone 36N (EPSG: 4547).
Values correspond to the classified land-use types used in the PLUS model.

🧮 Methodological Context

Model: Patch-generating Land Use Simulation (PLUS)

Temporal coverage: 2002–2022 (historical) → 2032 (projected)

Evaluation: Landscape metrics (NP, PD, ED, CONTAG, SHDI, SHEI) + Pareto analysis (ΔED–ΔCONTAG–ΔImp)

Software: ArcGIS Pro 3.4, FRAGSTATS v4.2, Python 3.10

🔗 Data Sources

CAS 30 m Annual Land Cover Dataset (1985–2023)

SRTM DEM 30 m (NASA)

MODIS NPP (MOD17A3HGF), EVI (MOD13Q1), and ET (MOD16A2GF)

GDP 1 km grid (RESDC, China)

Administrative boundaries (NGCC, License No. GS(2024)0650)

All third-party data are publicly available from their original providers as listed in the article’s Table 1.
