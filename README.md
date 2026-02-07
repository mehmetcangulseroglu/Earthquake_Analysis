# Real-Time Earthquake Analysis & Visualization Pipeline

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge\&logo=python\&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge\&logo=pandas\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-013243?style=for-the-badge\&logo=numpy\&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Data%20Visualization-brightgreen?style=for-the-badge)

---

## Project Overview

This project is an **end-to-end data analysis pipeline** that monitors **global seismic activities in near real-time**. By connecting to the **USGS (United States Geological Survey) API**, it automatically fetches the latest earthquake data, processes it to identify potential high-risk zones, and visualizes meaningful insights.

A special focus is placed on the **Turkey region**, enabling localized monitoring, trend analysis, and historical pattern exploration.

---

## Key Features

### 1. Automated Data Ingestion

* Fetches live earthquake data directly from **USGS servers** (JSON/CSV).
* No manual downloads required — the pipeline stays continuously up-to-date.

### 2. Data Cleaning & Preprocessing

* **Missing Value Handling:** Statistical imputation (mean/median) for missing `depth` and `error` values.
* **Datetime Parsing:** Converts timestamps into proper datetime objects for time-series analysis.
* **Noise Reduction:** Filters out non-earthquake events such as explosions or quarry blasts.

### 3. Feature Engineering

* **Energy Calculation:** Converts Richter magnitude (M) into **released seismic energy (Joules)** using the Gutenberg–Richter formula:

  ```math
  E = 10^{(1.5 \times M + 4.8)}
  ```

* **Risk Classification:** Earthquakes are categorized into:

  * `Low Risk`
  * `Moderate Risk`
  * `High Risk`

  based on magnitude and depth thresholds.

### 4. Exploratory Data Analysis (EDA)

* **Geospatial Visualization:** Mapping earthquake epicenters using latitude and longitude.
* **Correlation Analysis:** Examining relationships between **depth (km)** and **magnitude**.
* **Turkey-Specific Insights:** Dedicated filtering and analysis for seismic activity within Turkey.

---

## Tech Stack

* **Language:** Python 3.x
* **Data Manipulation:** Pandas (DataFrames, GroupBy, Pivot Tables)
* **Numerical Computing:** NumPy (vectorized operations)
* **Visualization:** Matplotlib, Seaborn

---

## Project Structure

```bash
├── data/
│   └── earthquake_cleaned.csv    # Cleaned dataset ready for ML or further analysis
├── notebooks/
│   └── earthquake_analysis.ipynb # Main analysis notebook (EDA & visualizations)
├── README.md                     # Project documentation
└── requirements.txt              # Project dependencies
```

---

## How to Run

1. **Clone the repository**

   ```bash
   git clone https://github.com/mehmetcangulseroglu/earthquake-analysis-turkey.git
   ```

2. **Install dependencies**

   ```bash
   pip install pandas numpy seaborn matplotlib
   ```

3. **Run the analysis**

   * Open `earthquake_analysis.ipynb` using **Jupyter Lab** or **VS Code**
   * Run all cells to fetch live data and generate visualizations

---

## Sample Insights

* *Deep earthquakes tend to have higher magnitudes but are felt less intensely on the surface due to energy dissipation.*
* *The Pacific Ring of Fire accounts for approximately 90% of global seismic activity.*

---

## Future Improvements

* Real-time alert system for high-risk earthquakes
* Interactive maps using Plotly or Folium
* Machine learning models for earthquake risk prediction

---

## Author

**Mehmet Can Gülseroğlu**
Computer Engineer | Data Science & AI

📅 2026
