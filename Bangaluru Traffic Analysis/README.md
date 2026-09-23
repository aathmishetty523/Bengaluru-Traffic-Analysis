# Urban Traffic Flow & Congestion Analytics

An end-to-end data analytics project focused on understanding traffic volume, congestion, road performance, bottlenecks, and mobility patterns across Bengaluru.

## Project Overview

This project analyzes a traffic dataset containing **8,936 records** covering **January 1, 2022 to August 9, 2024** across **8 areas**.

The analysis covers:

- Data loading and inspection
- Data cleaning and validation
- Missing-value handling
- Duplicate and negative-value checks
- Traffic volume analysis
- Congestion analysis
- Speed and delay analysis
- Bottleneck identification
- Network efficiency
- Outlier detection using z-scores
- Risk-flag identification
- Expected traffic and volume-gap analysis
- Interactive dashboard logic
- Scenario simulation

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Jupyter Notebook
- ipywidgets

## Key KPIs

| KPI | Result |
|---|---:|
| Total records | 8,936 |
| Areas covered | 8 |
| Average traffic volume | 29,236 |
| Average speed | 39.45 |
| Average travel time index | 1.38 |
| Average congestion level | 80.82 |
| Average road capacity utilization | 92.03% |
| Average incident reports | 1.57 |

## Key Findings

1. **Sony World Junction** had the highest average traffic volume among the listed roads/intersections at approximately **41,471**.
2. **Sarjapur Road** followed with approximately **40,190** average traffic volume.
3. **Koramangala** had the highest average delay index at approximately **1,242.90**.
4. Traffic volume showed a positive correlation of approximately **0.837** with congestion level.
5. Traffic volume showed a negative correlation of approximately **-0.341** with average speed.
6. The quality audit found no negative traffic-volume or negative-speed records in the notebook output.
7. The notebook identified high-volume observations using a z-score threshold greater than 3.
8. A risk flag was created using high congestion together with delay index above the 75th percentile.

## Project Structure

```text
Urban-Traffic-Flow-Congestion-Analytics/
│
├── analysis.ipynb
├── README.md
├── REPORT.md
├── DASHBOARD.html
├── requirements.txt
│
└── charts/
    ├── traffic_volume_by_day.png
    ├── traffic_volume_by_road.png
    ├── delay_index_by_area.png
    └── efficiency_by_area.png
```

## How to Run

1. Clone/download the repository.
2. Install the required Python libraries:

```bash
pip install -r requirements.txt
```

3. Open `analysis.ipynb` in Jupyter Notebook or VS Code.
4. Update the dataset path in the data-loading cell to the location of your CSV file.
5. Run the notebook from top to bottom.

## Dashboard

Open `DASHBOARD.html` in a browser to view the portfolio dashboard summary.

## Charts

The `charts` folder contains the main visualizations used for the project presentation.

## Resume Description

**Urban Traffic Flow & Congestion Analytics | Python, Pandas, SQL/Analytics, Power BI-ready**

Analyzed 8,936 Bengaluru traffic records to identify congestion patterns, high-volume roads, bottlenecks, traffic anomalies, and network-efficiency indicators using Python, Pandas, NumPy, Matplotlib, Seaborn and Plotly. Developed KPI logic, risk flags, delay metrics and scenario analysis to support data-driven traffic insights.


