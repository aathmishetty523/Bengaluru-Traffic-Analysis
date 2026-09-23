# Project Report: Urban Traffic Flow & Congestion Analytics

## 1. Objective

The objective of this project is to analyze urban traffic data and identify patterns related to traffic volume, congestion, speed, delay, road capacity, incidents, and network efficiency.

## 2. Dataset

The notebook contains analysis of:

- 8,936 records
- 16 original fields
- 8 areas
- Date range: January 1, 2022 to August 9, 2024

The original fields include date, area, road/intersection, traffic volume, average speed, travel time index, congestion level, road capacity utilization, incident reports, environmental impact, public transport usage, traffic signal compliance, parking usage, pedestrian/cyclist count, weather conditions, and roadwork/construction activity.

## 3. Data Preparation

The notebook performs:

- Column-name standardization
- Date conversion
- Hour extraction
- Missing-value inspection
- Median imputation for numeric missing values
- Duplicate checking
- Negative traffic-volume checking
- Negative average-speed checking
- Date and location coverage validation

## 4. Feature Engineering

The project creates several analytical fields:

- `hour`
- `day_name`
- `z_score`
- `is_peak`
- `high_congestion`
- `delay_index`
- `efficiency`
- `expected_volume`
- `volume_gap`
- `risk_flag`

### Main formulas

**Delay Index**

`traffic_volume / average_speed`

**Efficiency**

`average_speed / traffic_volume`

**Peak Indicator**

Peak periods are defined in the notebook as 08:00–10:00 and 17:00–19:00.

**High Congestion**

`congestion_level > 7`

**Risk Flag**

High congestion combined with delay index above the 75th percentile.

## 5. KPI Summary

| Metric | Value |
|---|---:|
| Records | 8,936 |
| Areas | 8 |
| Average traffic volume | 29,236.05 |
| Average speed | 39.45 |
| Average travel time index | 1.38 |
| Average congestion level | 80.82 |
| Average road capacity utilization | 92.03 |
| Average incident reports | 1.57 |
| Average public transport usage | 45.09 |
| Average traffic signal compliance | 79.95 |

## 6. Traffic Pattern Analysis

Average traffic volume by day:

- Wednesday: 29,697.56
- Thursday: 29,530.36
- Monday: 29,510.24
- Sunday: 29,105.28
- Saturday: 29,062.98
- Tuesday: 28,911.26
- Friday: 28,842.78

The notebook's current hour extraction produced hour `0` in the displayed aggregation, so hourly peak interpretation should be revisited if the source field is intended to represent time-of-day.

## 7. Road / Intersection Analysis

Highest average traffic volumes in the notebook:

1. Sony World Junction — 41,470.80
2. Sarjapur Road — 40,189.95
3. Trinity Circle — 35,350.14
4. Anil Kumble Circle — 35,251.83
5. CMH Road — 32,611.92

## 8. Bottleneck Analysis

Average delay index by area:

- Koramangala — 1,242.90
- M.G. Road — 1,033.27
- Indiranagar — 937.53
- Hebbal — 745.20
- Jayanagar — 690.22
- Whitefield — 562.62
- Yeshwanthpur — 482.27
- Electronic City — 409.14

These values are analytical outputs from the notebook and are not independent traffic-management recommendations.

## 9. Correlation Analysis

The notebook reports:

| Variable pair | Correlation |
|---|---:|
| Traffic volume vs average speed | -0.341 |
| Traffic volume vs congestion level | 0.837 |
| Average speed vs congestion level | -0.360 |

The strongest relationship in the calculated correlation matrix is between traffic volume and congestion level.

## 10. Outlier Analysis

A traffic-volume z-score was calculated. Records with `z_score > 3` were identified as extreme high-volume observations.

The notebook output shows several such observations concentrated in Koramangala, including records associated with Sarjapur Road and Sony World Junction.

## 11. Advanced Analysis

The project estimates expected traffic volume by hour and day, then calculates:

`volume_gap = actual traffic volume - expected traffic volume`

A risk flag is also created for records combining high congestion and relatively high delay.

## 12. Scenario Simulation

The notebook includes a scenario that reduces traffic volume by **15% during defined peak periods** and then evaluates the resulting delay-index measure.

## 13. Business / Analytics Value

This project demonstrates practical analytics skills including:

- Data cleaning
- Data quality validation
- Exploratory data analysis
- KPI development
- Feature engineering
- Correlation analysis
- Outlier detection
- Bottleneck identification
- Scenario analysis
- Visualization
- Dashboard development

## 14. Limitations

- The raw CSV file is not included in this GitHub package.
- The notebook currently loads the CSV using a local Windows path.
- The displayed hourly aggregation should be reviewed because the current notebook extracts the hour from `travel_time_index`, which is a numeric index rather than an obvious time field.
- Dashboard values are based on the notebook's recorded analytical outputs.
