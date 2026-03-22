# UK Supermarket Emissions Comparison

![UK Supermarket Logo](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/main/logos.png)

UK-Supermarket-Carbon-Emissions is dataset of raw and processed UK Supermarket RUKSmktCompetailer Carbon Emissions and Energy Consumption data extracted from the Annual Financial Reports of the eleven largest UK Retailers and a copy of the [Geolytix Retial Points] (https://geolytix.com/blog/supermarket-retail-points/) data for the [UKSmktComp Google Colab tutorial] (https://colab.research.google.com/drive/1f8a0pXfF9PqCujiwjf4TO4-k7ezt-6b3#scrollTo=SMDXbzxxDvQQ) that introduces EDA, data cleaning, standardisation, professional graphing, and regression analysis of secondary data to environmental managers.

| File | Description |
|------|-------------|
| geolytix_retailpoints_v34_202412.csv | Raw Geolytix Retail Points for UKSmktComp-1-Stores-Cleaning.ipynb |
| geolytix_size_class.csv | Geolytix Retail Points store size classes for UKSmktComp-1-Stores-Graphing.ipynb |
| geolytix_retailpoints_v34_202412_clean.csv | Geolytix Retail Points summarised by retailer and year for UKSmktComp-2-Stores-Graphing.ipynb |
| retailer_emissions.csv | Raw Retailer Emissions Data for UKSmktComp-3-Emissions-Cleaning.ipynb |
| retailer_yr.csv | Cleaned Retailer Emissions Data by retailer and year for UKSmktComp-4-Emissions-Graphing.ipynb |


## Raw Data: retailer_emissions.csv
2013 - 2025 carbon emmissions and energy consumption of the UKs eleven largest supermarket retailers extracted from  annual reports.

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
| Value | Numeric | Source_Value standardized to tCO2e or GWh |
| Unit | Text | Standardized unit |
| Unit_Neum | Unit numerator of standardisted intensity |
| Unit_Denom_1 | Text | 1st part of standardized intensity unit denominator, ‘m2’ or ‘£m’ |
| Unit_Denom_2 | Text | 2nd part of standardized intensity unit denominator, ‘Sales’, , ‘Sales Revenue’, ‘Turnover’, ‘Sales Floor’, ‘GIA’, ‘Stores and DC’. |
| Business_Scope | Text | Business extent of the value which may be organisational or geographical |

### Notes:
1. Accounting Period
Reports vary in accounting period with most covering either the previous year beginning January (calendar year), February, or April (financial year). Reports without an explicit accounting period are assumed to be the same as other reported years for that company. Values are assigned to the year the reports cover the majority of.

2. Value Recalculation
The accounting method may change and historic values recalculated to new estimated in later reports. Only unique year/value combinations are recorded for the earliest annual report in which the year/value is recorded.

3. Value Standardization
KPIs may be reported in different units, e.g. tCO2e or 1000's, tCO2eKWh or GWh. 'Raw reported' values and units are recorded in *Source_Value* and *Source_Unit*, with strandardised values in *Value* field and units in *Unit*, *Unit_Neum*, *Unit_Denom_1*, and *Unit_Denom_2*. Emissions are standardised to 'tCO2e' and energy to 'GWh'. Area-based intensity metrics are standardised to 'm2' and monetory intensity to million pounds '£m'.

4. Business Scope
Values are recorded for different business scopes, for example 'UK' or 'Global' operations, or the entire UK business or just the suprmarket component. Values for all business scopes are recorded. Business scope may change between reports.

| Business Scope | Description |
|------|-------------|
| UK | UK supermarket operations only |
| UK+ | All UK operations [1] |
! UK and Ireland | UK and Ireland operationa |
| UK and Europe | UK and European operations |
| Global | Global operations |

[1] J Sainsbury plc: Sainsburys, Homebase and Argos
