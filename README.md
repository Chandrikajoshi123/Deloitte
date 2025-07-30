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
