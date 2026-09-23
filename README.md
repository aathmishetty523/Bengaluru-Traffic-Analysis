# Urban Traffic Flow & Congestion Analytics

An end-to-end data analytics project focused on understanding traffic volume, congestion, road performance, bottlenecks, and mobility patterns across Bengaluru.

## 📌 Project Overview

This project analyzes a traffic dataset containing **8,936 records** covering **January 1, 2022 to August 9, 2024** across **8 areas**.

The analysis includes:

- Data loading and inspection
- Data cleaning and validation
- Missing-value handling
- Duplicate and negative-value checks
- Traffic volume analysis
- Congestion analysis
- Speed and delay analysis
- Bottleneck identification
- Network efficiency analysis
- Outlier detection using Z-scores
- Risk-flag identification
- Expected traffic and volume-gap analysis
- Dashboard development
- Scenario simulation

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Jupyter Notebook
- ipywidgets

## 📊 Key KPIs

| KPI | Result |
|---|---:|
| Total Records | 8,936 |
| Areas Covered | 8 |
| Average Traffic Volume | 29,236 |
| Average Speed | 39.45 |
| Average Travel Time Index | 1.38 |
| Average Congestion Level | 80.82 |
| Average Road Capacity Utilization | 92.03% |
| Average Incident Reports | 1.57 |

## 🔍 Key Findings

1. **Sony World Junction** recorded the highest average traffic volume among the analyzed roads/intersections at approximately **41,471**.

2. **Sarjapur Road** followed with an average traffic volume of approximately **40,190**.

3. **Koramangala** recorded the highest average delay index at approximately **1,242.90**.

4. Traffic volume showed a positive correlation of approximately **0.837** with congestion level.

5. Traffic volume showed a negative correlation of approximately **-0.341** with average speed.

6. The data quality audit found no negative traffic-volume or negative-speed records in the analyzed dataset.

7. High-volume observations were identified using a **Z-score threshold greater than 3**.

8. Risk flags were created using high congestion combined with a delay index above the **75th percentile**.

## 📈 Dashboard

The project includes an interactive dashboard containing key traffic and congestion metrics.

**Dashboard:** `DASHBOARD.html`

Open the HTML file in a web browser to view the dashboard.

## 📊 Visualizations

The `charts` folder contains the main project visualizations:

- Traffic Volume by Day
- Traffic Volume by Road
- Delay Index by Area
- Efficiency by Area

## 📁 Project Structure

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
