# Iran Airlines Data Analysis with Tableau

This repository presents an in-depth analysis of Tehran Airlines' air quality and weather data using Tableau. Through nine organized sheets, three interactive dashboards, and a comprehensive story, this project provides valuable insights into pollution trends, weather patterns, and data across various stations. The visualizations are designed to inform strategies for managing environmental and operational impacts.

## Project Overview

The Tehran Airlines dataset includes metrics on air quality and meteorological factors across multiple stations, with key indicators like PM2.5, CO, and NO2 levels, as well as temperature extremes, wind patterns, and aerosol optical depth measurements. This project uses Tableau's visualization tools to create engaging dashboards and an interactive story that brings forward critical trends and actionable insights.

## Dataset

- **Data Source**: [Tehran Airlines Dataset](https://mega.nz/file/D6ZwSC6L#FLy998-On64t_TKFMiDorJxDrHtHrBS41r5rH0BfKU8)
- **Data Description**: The dataset contains air quality and meteorological data across multiple stations with the following columns:

| Column Name            | Description                                   | Data Type |
|------------------------|-----------------------------------------------|-----------|
| `date`                 | Date of data recording                        | Object    |
| `pm25`                 | PM2.5 concentration                           | Float64   |
| `no2`                  | NO2 concentration                             | Float64   |
| `co`                   | CO concentration                              | Float64   |
| `timeframe`            | Timeframe for recording                       | Float64   |
| `min`, `max`           | Min & Max readings for the period             | Float64   |
| `stage1`, `stage2`, `stage3` | Pollution stages                       | Float64   |
| `station_id_x`, `station_id_y`, `station_id` | Unique station IDs       | Float64, Int64 |
| `station_name`         | Name of the station                           | Object    |
| `lat_x`, `lon`, `lat_y`, `long` | Latitude and longitude              | Float64   |
| `station_elevation`    | Elevation of the station                      | Float64   |
| `vvmin`, `ffm`, `tmax`, `tmin`, `tm` | Weather parameters            | Float64   |
| `rrr24`, `nm`, `umax`, `umin`, `um`, `sshn` | Additional weather metrics | Float64 |
| `x_utm`, `y_utm`       | UTM coordinates                               | Float64   |
| `aod_1` to `aod_9`     | Aerosol Optical Depth measurements            | Float64   |
| `month_period`         | Monthly period indicator                      | Object    |

## Sheets Overview

### Sheet 1: Temperature Analysis
- **Columns**: `Month (Month Period)`
- **Rows**: `SUM(Tmax)`, `SUM(Tmin)`
- **Purpose**: Visualizes monthly trends in maximum and minimum temperatures.
  <img width="1123" alt="1" src="https://github.com/user-attachments/assets/d2424f2b-3024-4953-a5f1-de97ba5e56b7">
### Sheet 2: Pollution by Station
- **Columns**: `Station Name`
- **Rows**: `SUM(Pm25)`, `SUM(Co)`
- **Purpose**: Analyzes pollution levels per station based on PM2.5 and CO concentrations.
  <img width="1120" alt="2" src="https://github.com/user-attachments/assets/7a3e3b36-6371-459e-a8e1-58930a212e0b">

### Sheet 3: Pollution Stages by Month and Station
- **Columns**: `Month (Month Period)`
- **Rows**: `Station Name`, `AVG(Stage1)`, `AVG(Stage2)`
- **Purpose**: Tracks average pollution stages across stations by month.
  <img width="1120" alt="3" src="https://github.com/user-attachments/assets/a8007391-8a60-45ab-ae00-a12bed7f88c1">

### Sheet 4: Aerosol Optical Depth Analysis
- **Columns**: `Station Name`
- **Rows**: `SUM(Aod1)` through `SUM(Aod9)`
- **Purpose**: Examines AOD distribution across stations to understand particulate matter trends.
  <img width="1121" alt="4" src="https://github.com/user-attachments/assets/a7a7ca2d-fa42-4076-a040-86ae45e913aa">

### Sheet 5: Yearly Wind Speed Trends
- **Columns**: `YEAR(Month Period)`
- **Rows**: `SUM(Umax)`, `SUM(Umin)`
- **Purpose**: Displays yearly variations in maximum and minimum wind speeds.
  <img width="1121" alt="5" src="https://github.com/user-attachments/assets/52e5560a-8d0c-4e24-940e-20b4fcd4ff1a">

### Sheet 6: Average Wind Speed by Station
- **Columns**: `Station Id`
- **Rows**: `AVG(Umax)`, `AVG(Umin)`
- **Purpose**: Compares average wind speeds across stations.
  <img width="1117" alt="6" src="https://github.com/user-attachments/assets/2de632f1-c8d4-4295-9f6b-a80fc63ad106">

### Sheet 7: Station Trends by Month
- **Columns**: `Month (Month Period)`
- **Rows**: `Station Name`
- **Purpose**: Observes station data trends over monthly periods.
  <img width="1120" alt="7" src="https://github.com/user-attachments/assets/8de2c0d7-5a6d-474d-9217-eed1758b055a">
  
### Sheet 8: Elevation and NO2 Concentration
- **Columns**: `Station Name`
- **Rows**: `SUM(Station Elevation)`, `SUM(No2)`
- **Purpose**: Correlates station elevation with NO2 concentration levels.
  <img width="1121" alt="8" src="https://github.com/user-attachments/assets/30d98c8b-4d8b-4db5-9298-e4b64dc11566">

### Sheet 9: Humidity and Precipitation by Station
- **Columns**: `Station Name`
- **Rows**: `SUM(Ffm)`, `Max(Rrr24)`
- **Purpose**: Shows total humidity and maximum precipitation per station.
  <img width="1121" alt="9" src="https://github.com/user-attachments/assets/3a98e823-6cab-47f5-a18f-90ed1bad2d6e">

## Story Section

The story contains three dashboards, each emphasizing distinct aspects of the data:
1. **Dashboard 1**: Monthly temperature averages and pollutant levels, highlighting seasonal patterns.
   <img width="1121" alt="d1" src="https://github.com/user-attachments/assets/1951cf14-f85f-4ec6-9c5b-831abda7a717">

2. **Dashboard 2**: Aerosol concentrations and wind speed trends across stations by year.
   <img width="1120" alt="d2" src="https://github.com/user-attachments/assets/0c689ab2-e1d9-4356-8419-bda3ec819801">

3. **Dashboard 3**: Station elevation effects on NO2 levels and wind speed metrics.
   <img width="1123" alt="d3" src="https://github.com/user-attachments/assets/6c8f33f1-a2d7-455c-8ec4-3e78715f0c08">

## Files

- **`IranAirlinesAnalysis.twb`**: The Tableau workbook with all sheets, dashboards, and story.
- **`Report.pdf`**: A report summarizing key insights, findings, and recommendations.

## Contact

For questions or suggestions, please reach out to [laibamazhar.000@gmail.com].
