# Sample Superstore

Project: sample-super-store

Overview
--------
This repository contains the data and final Power BI report(s) for a "Sample Superstore" analysis. The project demonstrates an end-to-end analysis workflow using data originally sourced from Kaggle, cleaned using Power BI's Power Query Editor, and analyzed / visualized inside Power BI Desktop. The repository stores raw and cleaned data as Excel files, the Power BI workbook, and exported result images.

Data
----
- Source: Kaggle (sample superstore dataset)
- Raw data file(s): `Raw Data/Sample - Superstore.xls`
- Cleaned data file(s): `Cleaned Data/Sample - Superstore.xls`

Data cleaning
-------------
All data cleaning and transformation was performed using Power BI's Power Query Editor. Typical steps performed in the cleaning process include:

- Loading the raw Excel sheet(s) into Power Query
- Renaming and normalizing column names
- Converting data types (dates, numeric columns)
- Handling missing or malformed values (imputing or removing rows as appropriate)
- Removing duplicate rows
- Creating calculated columns needed for analysis (for example: Year, Month, Profit Margin)
- Applying filters and trimming whitespace

The cleaned dataset used for analysis is stored in `Cleaned Data/` (exported after transformation) and embedded inside the Power BI report (`Result/sample_super_store.pbix`).

Analysis & deliverables
-----------------------
All analysis and visualizations were completed in Power BI Desktop. The work includes:

- Interactive Dashboard: overview of Sales, Profit, Quantity and key KPIs across time, categories and regions (`Result/Dashboard.png` shows a static snapshot).
- Forecasting: time series forecasting on Sales (Power BI forecasting visuals) and comparison with historical trends (`Result/Foracasting.png` snapshot).
- Sales breakdowns: Sales and Profit by Region, State, Category and Sub-Category.
- Time-series analysis: monthly and yearly trends, seasonality, and year-over-year comparisons.
- Profitability analysis: analysis of Profit vs Discount, identifying low-margin items and unprofitable transactions.
- Customer & Order insights: top customers, order priority analysis, shipping mode impact on KPIs.
- Segmentation: simple segmentations (top/bottom performers by product and region).

Files in this repository
------------------------
- `Raw Data/Sample - Superstore.xls` — original dataset downloaded from Kaggle.
- `Cleaned Data/Sample - Superstore.xls` — cleaned/exported dataset (after Power Query transformations).
- `Result/sample_super_store.pbix` — the Power BI Desktop file containing the full interactive report and transformations (Power Query steps live in this file).
- `Result/Dashboard.png` — a static screenshot of the dashboard for quick preview.
- `Result/Foracasting.png` — a static screenshot of the forecasting visual (note: file name preserved as-is).

How to view and reproduce
-------------------------
To open and interact with the report:

1. Install Power BI Desktop (Windows).
2. Open `Result/sample_super_store.pbix` in Power BI Desktop to view the interactive dashboards and Power Query transformations.

If you want to reproduce the cleaned data from the raw Excel by hand:

1. Open `Result/sample_super_store.pbix` in Power BI Desktop.
2. In the Home ribbon, click Transform data -> Power Query Editor to inspect the applied transformation steps.
3. To export cleaned tables, right-click a query in Power Query and choose "Reference" (if you need a stable copy) then load to a new worksheet or export to CSV from Power BI.

Notes and next steps
--------------------
- The repository currently contains only data and Power BI artifacts — no scripts or automated pipeline. If you want reproducible Python scripts or automated cleaning, I can add a `scripts/` folder with an ingestion/cleaning script and a small notebook for exploratory analysis.
- Consider renaming `Result/Foracasting.png` to `Result/Forecasting.png` for clarity (I preserved the existing filename in this README).
- If you prefer the cleaned CSV files instead of Excel or embedded Power BI tables, I can export them as `CSV` and add a short script to regenerate them automatically.

Contact / Authors
-----------------
If you want to extend this work (add automated ETL, tests, or recreate visuals in Python), tell me which part to start with and I will implement it.

License
-------
See the repository `LICENSE` file for license details.
