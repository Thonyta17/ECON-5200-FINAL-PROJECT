# ECON 5200: Consulting Report — Final Project

**Research Question:** Does cigarette price (driven by state excise taxes) causally reduce per-capita cigarette consumption?

**Identification Strategy:** Instrumental Variables (2SLS)
**Instrument:** Log real minimum price in adjoining states (`ln_pimin`)
**Data:** Baltagi & Levin (1992) cigar panel — 46 U.S. states × 30 years (1963–1992)

## Results

| Model | Elasticity | 95% CI |
|-------|-----------|--------|
| Naive OLS | -1.455 | [-2.198, -0.712] |
| 2SLS (Causal) | -1.696 | [-2.670, -0.722] |

A 10% excise tax increase (90% pass-through to retail price) reduces per-capita packs sold by approximately **15.3%** (95% CI: -24.0% to -6.5%).

## Live Dashboard

[Streamlit Dashboard — What-If Scenarios](https://da-final-t.streamlit.app/)

## Files

| File | Description |
|------|-------------|
| `5200_final_project_starter.ipynb` | Main analysis notebook (Parts 1–7) |
| `app.py` | Streamlit dashboard with what-if scenarios |
| `CigarettesSW.csv` | Dataset (Baltagi & Levin 1992) |
| `requirements.txt` | Python dependencies |

## Reproducing

```bash
pip install -r requirements.txt
jupyter notebook 5200_final_project_starter.ipynb
streamlit run app.py
```

> **Note:** Run `pip install linearmodels` before executing the notebook, then restart the kernel so `IV2SLS` loads correctly with robust standard errors.

## Repository

## Repository

[GitHub — ECON-5200-FINAL-PROJECT](https://github.com/Thonyta17/ECON-5200-FINAL-PROJECT)

