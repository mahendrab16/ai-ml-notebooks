# 🅿️ Smart Parking Management — Exploratory Data Analysis

## Overview
This project explores a smart-parking dataset using Python. It examines user categories, vehicle types, parking spots, parking duration, electric-vehicle labels, and dynamic-pricing factors.

The project is **exploratory data analysis (EDA)**. It does not currently claim to predict parking demand or establish causal relationships.

## Objectives
- Inspect the dataset's structure and data quality.
- Explore user and vehicle distributions.
- Compare recorded usage and parking duration across parking spots.
- Summarize dynamic-pricing factors across available groups.
- Inspect entry, exit, and timestamp fields where their formats support meaningful analysis.

## Dataset
- **Expected filename:** `IIoT_Smart_Parking_Management.csv`
- **Columns used when available:** `User_Type`, `Parking_Spot_ID`, `Parking_Duration`, `Dynamic_Pricing_Factor`, `Vehicle_Type_Weight`, `Vehicle_Type`, `Electric_Vehicle`, `Entry_Time`, `Exit_Time`, and `Timestamp`.
- **Source URL and license:** Add the verified original dataset source and license here before publishing. They were not provided in the original notebook, so they have not been guessed.

Upload the CSV to your Colab session or place it in the same folder as the notebook. The notebook checks common paths and prompts for upload in Google Colab if it cannot find the file.

## Tools
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Google Colab or Jupyter Notebook

## Workflow
1. Load the CSV and inspect its shape and columns.
2. Review data types, missing values, duplicates, and descriptive statistics.
3. Safely convert selected numeric and timestamp fields where possible.
4. Visualize user-type and vehicle-type distributions.
5. Compare total recorded parking duration and record counts by parking spot.
6. Summarize dynamic-pricing factors by parking spot and vehicle weight.
7. Inspect entry/exit fields and plot time trends only when parsing supports them.
8. Record evidence-based findings and limitations.

## Repository contents

```text
.
├── README.md
└── parking_lot_analysis.ipynb
```

## Run the notebook
1. Open `parking_lot_analysis.ipynb` in Google Colab or Jupyter.
2. Upload `IIoT_Smart_Parking_Management.csv` when prompted.
3. Run all cells from top to bottom.
4. Review the generated tables and charts.
5. Complete the notebook's Key Findings section with observations supported by the outputs.

## Important interpretation notes
- Record count by parking spot is not necessarily an occupancy rate.
- The meaning and units of `Parking_Duration`, `Entry_Time`, `Exit_Time`, and `Dynamic_Pricing_Factor` should be confirmed from the dataset documentation.
- Summing entry/exit time codes may be misleading; this notebook avoids treating such sums as traffic measures.
- Correlation or group differences do not establish causation.
- No performance metrics or factual findings are claimed without running the notebook.

## Future improvements
- Add hourly and weekday demand analysis if timestamps are valid.
- Calculate occupancy rates if capacity and occupancy status are available.
- Develop a forecasting model only after defining a valid prediction target and confirming time coverage.
- Add tests, dependency pinning, and a verified dataset citation.

## License
Choose a license for your notebook if you want to specify reuse permissions. Check the dataset's license and usage terms before redistributing the CSV.
