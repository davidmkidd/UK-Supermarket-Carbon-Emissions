# UK Supermarket Emissions 2013-2024
UK Supermarket Emissions and Energy Consumption data from UK Annual Financial Reports.

From 1 October 2013, all UK-based companies listed on the Main Market of the London Stock Exchange were required to report greenhouse gas emissions, energy consumption, and energy efficiency in their annual reports. This was mandated under the Companies Act 2006 (Strategic Report and Directors’ Report) Regulations 2013, SI 2013/1970. Part 7 ‘Disclosures Concerning Greenhouse Gas Emissions’ is detailed in Schedule 7 of the Large and Medium-sized Companies and Groups (Accounts and Reports) Regulations 2008, SI 2008/410. On 1 April 2019, the Streamlined Energy and Carbon Reporting (SECR) regulations (2019) extended reporting to a wider range of public and private companies.


## Accounting Period
Annual reports vary in accounting period with covering the previous year periods year beginning January (Calendar Year), February, or April (Financial Year). 
Reports without explicit accounting periods are assumed to be the same as other reported years for that company. 
One retailer changed accounting month, and the accounting periods of successive reports of the same company do not always begin and end on the same day of the month. 

Reporting year is assigned to the year the reports cover the majority of.

## Emissions Reporting
Annual reports vary in how emissions and energy are measured including the method (location or marked) and  reports emissions and energy for the accounting year and (often) one or more previous years, one of which will be the 'baseline' to which the value is compared. 
The accounting method may, however, change with later reports reporting recalculated values for previous years. 

Only unique year/value combinations are recorded for the earliest annual report in which the year/value is recorded.

# Business Scope

For simplicity:
1. Report periods are assigned to the year which they cover the majority of irrespective of the reporting month
2. Only unique values are recorded from the earliest annual report in which the value is reported.
3. Where values are reported for more than one ‘organizational scope’ only the scope that is closest to the 'UK Supermarket' is recorded. For example, only values for Waitrose supermarkets are recorded for John Lewis Partnership reports, and 

## UKSmktComp.zip

| File | Description |
|----------|----------|
| retailer_emissions.csv | Reported emissions and energy | 
| geolytix_retailpoints_v34_202412.csv | Geolytix UK Supermarket Stores | 
| geolytix_size_class.csv | Mid-class store floor space for Geolytix size classes | 
| uk.shp | UK Shapefile | 


## retailer_emissions.csv

| Field | Type | Description |
|----------|----------|----------|
| Retailer_Id | Text | Retailer identifier code |
| Year | Integer | Retailer identifier code |
| Method | Text | ‘Location’, ‘Market’ or NA|
| KPI | Text | Name of KPI, ‘Scope 1’, ‘Scope 2’, ‘Scope 1 and 2’, ‘Scope 3’, ‘Scope 1 – 3’, or ‘Energy’ |
| KPI_Type | Text | ‘Measure’ or ‘Intensity’ |
| Source | Text | Record source |
| Source_Year | Integer | Year of source report |
| Source_Value |Numeric | Value in report |
| Source_Unit | Text | Unit in report |
| Value | Numeric |Standardized value |
| Unit | Text | Standardized unit |
| Unit_Neum | Text | Standardized intensity unit numerator |
| Unit_Denom_1 | Text | 1st part of standardized intensity unit denominator, ‘m2’ or ‘£m’ |
| Unit_Denom_2 | Text | 2nd part of standardized intensity unit denominator, ‘Sales’, , ‘Sales Revenue’, ‘Turnover’, ‘Sales Floor’, ‘GIA’, ‘Stores and DC’. |
| Business_Scope | Text | Business extent of the value which may be organisational or geographical |


