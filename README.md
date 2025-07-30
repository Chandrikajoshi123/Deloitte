# Deloitte Virtual Internship Projects (Forage)
This repository contains my solutions to two data analysis tasks completed as part of the **Daikibo Industrials Virtual Experience Program** on [Forage](https://www.theforage.com/).
## Contents

 1. [ Telemetry Dashboard (Tableau)](#1-telemetry-dashboard-tableau)
 2. [ Equality Score Classification (Excel)](#2-equality-score-classification-excel)


## Telemetry Dashboard (Tableau)

###  Objective

Analyze telemetry data from various Daikibo factories to measure and visualize **equipment downtime** using Tableau.

###  Key Steps
<br>
- Imported JSON data (`daikibo-telemetry-data.json`) into Tableau.<br>
- Created a **calculated field**: 

  ```tableau
  IF [Status] = "unhealthy" THEN 10 ELSE 0 END
```
This calculates 10 minutes of potential downtime for each "unhealthy" reading.
- Built two bar charts:
  - Down Time per Factory
  - Down Time per Device Type
- Combined both charts in an interactive dashboard.
   - Selecting a factory filters the device-type breakdown.
