# Maji Ndogo Water Access Analysis

## Table of Contents
-[Project Overview](#project-overview)

-[Recommendations](#recommendations)

-[Project Overview](#project-overview)

-[Data Sources](#data-sources)

-[Tools](#tools)

-[Data Cleaning/Preparations](#data-cleaningpreparations)

-[Exploratory Data Analysis](#exploratory-data-analysis)

-[Data Analysis](#data-analysis)

-[Results](#results)

-[Recommendations](#recommendations)

-[Limitations](#limitations)

-[References](#references)

### Project Overview

The Maji Ndogo Water Project is a data-driven initiative focused on addressing water access challenges in a fictional country called Maji Ndogo. The country faces a water crisis characterized by inadequate access to clean and safe drinking water, long waiting times at water collection points, contaminated water sources, and insufficient water infrastructure.
The project aims to investigate these challenges using data to understand the extent of the crisis, identify the communities most affected, and recommend practical solutions for improving water access.


### Data Sources

The primary data source for the Maji Ndogo Water Project is the Maji Ndogo Water Services database (md_water_services), which contains information about water sources, water quality, water collection visits, locations, and infrastructure improvements.

### Tools

- SQL server - Data Cleaning & Analysis
   -[Download here](https://www.mysql.com/downloads/)
- Power BI - Creating reports
  -[Download here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)

### Data Cleaning/Preparations



### Exploratory Data Analysis
EDA involved exploring the md_water_services_data to answer key questions, such as:




### Data Analysis
Interesting code I worked with
```sql
SELECT g.country_name,g.Sub_region, g.Avglandarea,(round(g.avgLandarea/ total_land_area
)*100) as pct_regional_land
FROM united_nations.geographical_locations as g
JOIN
(SELECT Sub_region, sum(Avglandarea) as total_land_area
FROM united_nations.geographical_locations
GROUP BY sub_region) as land_per_region
on g.Sub_region=land_per_region.Sub_region;
```

### Results


### Recommendations


### Limitations


### References



