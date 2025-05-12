# Tornado Hazard Dashboard – Western Europe (ERA5-based)

This project provides an interactive dashboard for visualizing tornado hazard levels across Western Europe using reanalysis data from ERA5 and a custom database of tornado events.

## 🚀 Objective

To create a data-driven tool that supports climate risk assessment and catastrophe modeling using atmospheric variables such as CAPE, SRH, and wind shear, which are known to contribute to tornadic environments.

## 🛰️ Data Sources

- [ERA5 Reanalysis](https://cds.climate.copernicus.eu/)
  - Variables: CAPE, 0–3km SRH, Bulk Shear, 2m Temperature, SLP
  - Temporal resolution: hourly or 3-hourly
  - Spatial resolution: ~0.25°
- Custom tornado events dataset (France/Western Europe, 1900–2024)

## 🧰 Tech Stack

- Python (Pandas, Xarray, Numpy, Scikit-learn)
- Streamlit (interactive dashboard)
- Plotly / Folium (interactive mapping)
- NetCDF4 / cfgrib (ERA5 reading)
- GeoPandas (event spatial mapping)

## 📊 Key Features

- Interactive map of tornado events overlaid with reanalysis-derived hazard scores
- Time slider for seasonal/temporal variation
- Risk score computation based on meteorological variables
- Simple clustering of high-risk environments (optional ML)

## ⚙️ Installation

```bash
git clone https://github.com/matthieulacroix/climatecatrisk-tornado-hazard-dashboard.git
cd climatecatrisk-tornado-hazard-dashboard
pip install -r requirements.txt
streamlit run app/dashboard.py
