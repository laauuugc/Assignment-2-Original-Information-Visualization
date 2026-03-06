**Greenhouse Gas Emissions in Ireland — Data Processing**

This repository contains the data preparation workflow for Assignment 2: Develop a Novel Information Visualization, using the CSO High Value Dataset EAA17 (Greenhouse Gas Emissions).

Repository Contents

- eaa17_original.csv: Original dataset downloaded from the Central Statistics Office (CSO).

- eaa17_processing.ipynb: Jupyter Notebook containing all preprocessing steps and documented transformations.

- eaa17_processed.csv: Cleaned and aggregated dataset used in the Vega-Lite interactive dashboard.

- visualization.html: Final fully developed interactive dashboard website to explore data insights.

- visualization.json: JSON file used initially in Vega-Lite to create the main elements of the final website.

Running the dashboard

No build step, no dependencies to install, just open visualisation.html in a modern browser (Chrome or Firefox work best) and you're done. The charts load automatically by fetching eaa17_processed.csv directly from this repository via the GitHub raw URL, so you'll need an internet connection the first time. If you open the file locally and the charts don't appear, it's almost certainly a CORS issue with your browser blocking the CSV fetch, the fix is to serve it from a local server instead: run python3 -m http.server in the project folder and open http://localhost:8000/visualisation.html. Once it's running, all four interactive controls in the sticky bar at the top (year slider, gas type, baseline year, and comparison year), update the relevant charts instantly with no page reload.

Data Processing Overview

Data manipulation was performed in Python prior to visualisation to ensure clarity, accuracy, and consistency across coordinated views.
The following transformations were applied:
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
