# Deloitte Virtual Internship Projects (Forage)
This repository contains my solutions to two data analysis tasks completed as part of the **Daikibo Industrials Virtual Experience Program** on [Forage](https://www.theforage.com/).
## Contents

 1. [ Telemetry Dashboard (Tableau)](#1-telemetry-dashboard-tableau)
 2. [ Equality Score Classification (Excel)](#2-equality-score-classification-excel)


## Telemetry Dashboard (Tableau)

###  Objective

Analyze telemetry data from various Daikibo factories to measure and visualize **equipment downtime** using Tableau.

###  Key Steps

- Imported JSON data (`daikibo-telemetry-data.json`) into Tableau.
- Created a **calculated field** : 

  ```tableau
  IF [Status] = "unhealthy" THEN 10 ELSE 0 END

This calculates 10 minutes of potential downtime for each "unhealthy" reading.
- Built two bar charts:
  - Down Time per Factory
  - Down Time per Device Type
- Combined both charts in an interactive dashboard.
   - Selecting a factory filters the device-type breakdown.

## Screenshot

###  Tools Used
- Tableau Desktop
- JSON Data
- Calculated Fields & Interactive Filters

## Equality Score Classification (Excel)

### Objective
Classify employee job roles by their Equality Score to assess gender pay equity across factories.

### 📁 Dataset Structure
(Original file not included for licensing reasons)


|Column	|Description|
|-------|-----------|
|Factory|	Name of the location|
|Job Role|	Title/position of the employee|
|Equality Score	|Integer from -100 to 100 (0 = ideal)|

### Added Column: Equality Class
|Equality Score	|Equality Class|
|---------------|--------------|
|Between -10 and +10 |	Fair|
|-11 to -20 / 11 to 20 |	Unfair|
|< -20 or > 20	| Highly Discriminative|

### Excel Formula Used
```
=IF(ABS(C2)<=10, "Fair", IF(ABS(C2)<=20, "Unfair", "Highly Discriminative"))
