# UK Supermarket Emissions Comparison

![UK Supermarket Logo](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/main/logos.png)


UKSmktComp is dataset of UK Supermarket Retailer Carbon Emissions and Energy Consumption data extracted from the UK Annual Financial Reports of the eleven largest UK Retailers and a copy of the [Geolytix Retial Points] (https://geolytix.com/blog/supermarket-retail-points/) data set. These data were collated for the UKSmktComp Google Colab R Workbooks tutorials that introduces EDA, data cleaning, standardisation, professional graphing, and regression analysis of secondary data to Environmental Managers. 

| File | Description |
|------|-------------|
| geolytix_retailpoints_v34_202412.csv | Raw Geolytix Retail Points for UKSmktComp-1-Stores-Cleaning.ipynb, downloaded Septemeber 2024 |
| geolytix_size_class.csv | Geolytix Retail Points store size classes for UKSmktComp-1-Stores-Cleaning.ipynb |
| geolytix_retailpoints_v34_202412_clean.csv | Cleaned Geolytix Retail Points for UKSmktComp-2-Stores-Graphing.ipynb |
| retailer_emissions.csv | Raw Retailer Emissions Data for UKSmktComp-3-Emissions-Cleaning.ipynb |
| retailer_emissions_clear.csv | Cleaned Retailer Emissions Data for UKSmktComp-4-Emissions-Graphing.ipynb |


## Raw Data: retailer_emissions.csv
Carbon emmissions and energy consumption was extracted from the annual reports of the eleven largest UK supermarket retailers published 2013 to 2025.

| Field | Type | Description |
|----------|----------|----------|
| Retailer_Id | Text | Retailer identifier |
| Source_Year | Integer | Year of source report |
| KPI | Text | Name of KPI, ‘Scope 1’, ‘Scope 2’, ‘Scope 1 and 2’, ‘Scope 3’, ‘Scope 1 – 3’, or ‘Energy’ |
| Method | Text | ‘Location’, ‘Market’ or NA|
| KPI_Type | Text | ‘Measure’ or ‘Intensity’ |
| Year | Integer | Year of KPI value |
| Source | Text | Record source |
| Source_Value |Numeric | Value in report |
| Source_Unit | Text | Unit in report |
| Value | Numeric | Source_Value standardized to tCO2e or GWh  |
| Unit | Text | Standardized unit |
| Unit_Neum | Unit numerator of standardisted intensity |
| Unit_Denom_1 | Text | 1st part of standardized intensity unit denominator, ‘m2’ or ‘£m’ |
| Unit_Denom_2 | Text | 2nd part of standardized intensity unit denominator, ‘Sales’, , ‘Sales Revenue’, ‘Turnover’, ‘Sales Floor’, ‘GIA’, ‘Stores and DC’. |
| Business_Scope | Text | Business extent of the value which may be organisational or geographical |

Notes: 

1. Accounting Period
Annual reports vary in accounting period with covering the previous year periods year beginning January (Calendar Year), February, or April (Financial Year). 
Reports without explicit accounting periods are assumed to be the same as other reported years for that company. 
One retailer changed accounting month, and the accounting periods of successive reports of the same company do not always begin and end on the same day of the month. 

Reporting year is assigned to the year the reports cover the majority of.

2. Emissions Reporting
Annual reports vary in how emissions and energy are measured including the method (location or marked) and  reports emissions and energy for the accounting year and (often) one or more previous years, one of which will be the 'baseline' to which the value is compared. The accounting method may, however, change with later reports reporting recalculated values for previous years. 

Only unique year/value combinations are recorded for the earliest annual report in which the year/value is recorded.

3. Business Scope
The geographical/organisational scope for which values are reported.  If values for more than one scope are reported only the scope closest to 'UK Supermarkets' is recorded, for example, only values for Waitrose supermarkets are recorded from John Lewis Partnership reports. Business scope may change between reporting periods.

| Business Scope | Description |
|------|-------------|
| UK | UK supermarket operations only |
| UK+ | All UK operations [1] |
! UK and Ireland | UK and Ireland operationa |
| UK and Europe | UK and European operations |
| Global | Global operations |

[1] J Sainsbury plc: Sainsburys, Homebase and Argos

## Cleaned Data: retailer_emissions_clean.csv
