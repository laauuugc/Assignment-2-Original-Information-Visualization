Greenhouse Gas Emissions in Ireland — Data Processing

This repository contains the data preparation workflow for Assignment 2: Develop a Novel Information Visualization, using the CSO High Value Dataset EAA17 (Greenhouse Gas Emissions).

Repository Contents
eaa17.csv: Original dataset downloaded from the Central Statistics Office (CSO).
data_cleaning_eaa17.ipynb: Jupyter Notebook containing all preprocessing steps and documented transformations.
eaa17_processed.csv: Cleaned and aggregated dataset used in the Vega-Lite interactive dashboard.

Data Processing Overview
Data manipulation was performed in Python prior to visualisation to ensure clarity, accuracy, and consistency across coordinated views.
The following transformations were applied:
- Filtered to retain Carbon dioxide (CO₂) emissions only.
- Removed missing and invalid values.
- Renamed columns for clarity and compatibility with Vega-Lite.
- Aggregated emissions by Year × NACE Sector.
- Sorted data chronologically.
- Exported a clean dataset for dashboard integration.
These steps reduce redundancy, prevent double-counting, and improve visual interpretability while preserving the integrity of the original CSO data.

How to Reproduce
- Open data_cleaning_eaa17.ipynb in Jupyter Notebook.
- Run all cells sequentially.
The processed dataset will be generated as: eaa17_processed.csv

Dataset Source
Central Statistics Office (CSO)
High Value Dataset: EAA17 – Greenhouse Gas Emissions

Purpose
The processed dataset supports an interactive Vega-Lite dashboard designed to explore:
- Sector-level emissions trends
- Temporal changes in CO₂ emissions
- Comparative analysis across economic sectors
