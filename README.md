# Pakistan Flood Risk Analysis — 2022

One third of Pakistan was underwater in 2022. 33 million people affected, 1.7 million homes damaged, losses above $30 billion. I built this to understand where the burden fell and whether the patterns could help with future preparedness planning.

The finding that stuck with me: flood extent alone doesn't explain displacement. Pre-existing poverty was a stronger predictor than how badly a district flooded. Districts with poverty above 50% had more than double the per-capita displacement of lower-poverty districts with similar flood exposure.

---

## What this covers

- Province and district-level impact analysis
- Correlation between poverty rate and displacement intensity
- Vulnerability index combining flood exposure, poverty, and infrastructure quality
- Top 15 most affected districts

## Data

Synthetic dataset modelled on NDMA damage reports and OCHA situation reports from the 2022 flood response. Scale and proportions match published figures.

## Tools

Python, Pandas, Matplotlib, Seaborn

## How to run

```bash
git clone https://github.com/masoom-khan/pakistan-flood-risk-2022.git
cd pakistan-flood-risk-2022
pip install -r requirements.txt
jupyter notebook flood_analysis.ipynb
```

## Key findings

- Sindh province: highest total displacement
- Poverty vs displacement correlation: r = 0.54
- 72 districts had more than 50% of their area flooded
- Districts with poor road access suffered disproportionately higher mortality

---

**Muhammad Masoom Khan** — ICT Supervisor | MSF OCA Pakistan  
[Portfolio](https://masoom-khan.github.io) · [LinkedIn](https://www.linkedin.com/in/muhammadmasoomkhan/)
