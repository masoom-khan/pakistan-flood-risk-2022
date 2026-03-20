# 🌊 Pakistan Flood Risk Analysis (2022)

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![GeoPandas](https://img.shields.io/badge/GeoPandas-Spatial%20Analysis-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> Geospatial analysis of the 2022 Pakistan superfloods — mapping affected populations, infrastructure damage, and displacement hotspots across all provinces to support humanitarian response planning.

---

## 📌 Problem Statement

The 2022 Pakistan floods affected 33 million people, damaged 1.7 million homes, and caused losses of $30+ billion. This analysis uses publicly available disaster data to understand the spatial distribution of impact and identify factors that made certain areas more vulnerable.

**Questions addressed:**
- Which districts experienced the most severe flooding?
- How does flood exposure correlate with poverty levels and population density?
- Where were the largest displacement concentrations?
- Which infrastructure (roads, bridges, schools, hospitals) was most affected?

---

## 📂 Dataset

| Source | Description | Link |
|--------|-------------|------|
| NDMA Pakistan | District-level damage reports | [ndma.gov.pk](http://ndma.gov.pk) |
| OCHA Pakistan | Humanitarian situation reports | [data.humdata.org](https://data.humdata.org/dataset/pakistan-floods-2022) |
| World Bank | Poverty headcount by district | [data.worldbank.org](https://data.worldbank.org) |
| UNOSAT | Flood extent raster maps | [unosat.org](https://unosat.org/products/) |
| Pakistan Bureau of Statistics | Population by district (2017 census) | [pbs.gov.pk](https://www.pbs.gov.pk) |

---

## 🔧 Tools & Libraries

```
Python 3.8+
pandas, numpy       — data wrangling
geopandas           — spatial analysis
folium              — interactive maps
matplotlib, seaborn — static charts
plotly              — interactive visualisations
shapely             — geometry operations
```

---

## 📊 Analysis Steps

### 1. Data Integration
- Downloaded damage reports from NDMA and OCHA ReliefWeb
- Merged with district-level population and poverty data
- Standardised district/tehsil naming conventions across datasets

### 2. Spatial Analysis
- Loaded Pakistan district shapefiles (ADM2 level)
- Calculated flood-affected area as % of district area using UNOSAT rasters
- Created choropleth maps of damage severity by district

### 3. Vulnerability Assessment
- Built composite vulnerability index: flood exposure × poverty rate × population density
- Identified top 20 most vulnerable districts
- Analysed correlation: flood_area_pct vs. poverty_headcount (r = 0.54)

### 4. Infrastructure Impact
- Mapped damaged roads, schools, hospitals by province
- Calculated estimated reconstruction cost by district

---

## 📈 Key Findings

| Metric | Value |
|--------|-------|
| People affected | 33+ million |
| Districts with >50% area flooded | 72 |
| Homes damaged/destroyed | 1.7 million |
| Most affected province | Sindh (8.2M affected) |
| Correlation: poverty vs. flood impact | r = 0.54 |
| Districts in extreme vulnerability | 28 (top quintile) |

> **Key insight:** Districts with poverty rates above 50% experienced 2.3x higher displacement rates per capita than wealthier districts with similar flood extent, demonstrating the compounding effect of pre-existing vulnerability.

---

## 🚀 How to Run

```bash
git clone https://github.com/YOUR_USERNAME/pakistan-flood-risk-2022.git
cd pakistan-flood-risk-2022
pip install -r requirements.txt
jupyter notebook flood_analysis.ipynb
```

---

## 📁 Structure

```
pakistan-flood-risk-2022/
├── README.md
├── requirements.txt
├── flood_analysis.ipynb
├── data/
│   └── README_data.md
└── outputs/
    ├── flood_impact_map.html     ← interactive Folium map
    ├── district_vulnerability.png
    └── poverty_vs_impact.png
```

---

## 👤 Author
**Muhammad Masoom Khan** | Data Analyst | MSF Holland  
[LinkedIn](https://www.linkedin.com/in/muhammadmasoomkhan/) | [Portfolio](https://muhammadmasoomkhan.github.io)
