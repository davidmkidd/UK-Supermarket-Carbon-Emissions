# UK Supermarket Emissions 2013-2024

From 1 October 2013, all UK-based companies listed on the Main Market of the London Stock Exchange were required to report greenhouse gas emissions, energy consumption, and energy efficiency in their annual reports. This was mandated under the Companies Act 2006 (Strategic Report and Directors’ Report) Regulations 2013, SI 2013/1970. Part 7 ‘Disclosures Concerning Greenhouse Gas Emissions’ is detailed in Schedule 7 of the Large and Medium-sized Companies and Groups (Accounts and Reports) Regulations 2008, SI 2008/410. On 1 April 2019, the Streamlined Energy and Carbon Reporting (SECR) regulations (2019) extended reporting to a wider range of public and private companies.

UKSmktComp is a dataset of Emissions and Energy Consumption data extracted from UK Annual Financial Reports of the eleven largest UK Retailers collated for the UK Supermarket Comparison Tuturials that aim to introduce Environmental Mangager's to EDA and professional graphing in R delivered as Google Colab Workbooks.

The data is supplied in two forms:
1. Raw data extracted from annual reports for EDA and Data Cleaning tutorial.
2. Cleaned data for comparative analysis tutorial.

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
Where values are reported for more than one ‘organizational scope’ only the scope that is closest to the 'UK Supermarket' is recorded. For example, only values for Waitrose supermarkets are recorded for John Lewis Partnership reports. 

## Cleaned Data: retailer_emissions_clean.csv
