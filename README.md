# UK Supermarket Comparison

![UK Supermarket Logo](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/main/logos.png)

> **Which UK supermarket retailer is the most carbon efficient?**

UK legislation requires many larger businesses to publish total carbon emissions and energy usage figures in their annual reports. Carbon emissions scale with business size, so since 2019 companies have also been required to report at least one intensity metric scaled to a measure of business size, but it is left to the business to select a size demonominator, which may be total revenue, a measure of geographical space, number of sales, or other size measure. The relative carbon intensities of businesses cannot be assessed without a common carbon intensity metric.

The UK Supermarket Comparison (UKSmktComp) tutorial shows how an common area-based intensity metric can be estimated by integrating a primary (collected for this task) archival dataset of UK supermarket retailer carbon emissions data collated from company annual reports with a secondary dataset of UK supermarket stores.

This requires:

1. The dataset of supermarket stores to be explored, cleaned, summarised.
2. The dataset of retailer emissions to be explored, cleaned, summarised.
3. Absolute emissions to be scaled to carbon intensity by retailer store area.
4. Estimated intensity compared to reported intensity.
5. Intensity for emissions components to be calculated from reported KPIs and plotted as a stacked bar chart.

Data are processed and visualised using the [R language](https://www.r-project.org/) within a set of [Google Colab](https://colab.research.google.com/) Workbooks for which no prior knowledge is required. Workbooks are designed to be compleated sequentially but may also be run independently.

# Workbooks

## System and Data

[Workbook 1](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/f78133709d5a909b64282db917e478c263c2f7d6/UKSmktComp_UK_Supermarket_Retailer.ipynb) Introduction to carbon reporting and supermarket emissions.

[Workbook 2](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/f78133709d5a909b64282db917e478c263c2f7d6/UKSmktComp_Stores_Cleaning.ipynb) Clean and summarise the Geolytix Retail Points dataset of UK supermarket outlets

[Workbook 3](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/f78133709d5a909b64282db917e478c263c2f7d6/UKSmktComp_Stores_Graphing.ipynb) Explore retailer store estate portfolios

[Workbook 4](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/5dd074b8f408c64c6b50608476a41af7e6bbd622/UKSmktComp_Emissions_Cleaning.ipynb) Clean, summarise, and scale emissions and energy data

## Absolute and Intensity by Scope

For each Scope:

1. Absolute retailer emsssions time series are plotted.
2. Scaling of emissions with store number and area are tested with linear regression.
3. Emissions are scaled to intensity using the best scaling model.


[Workbook 5](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/5dd074b8f408c64c6b50608476a41af7e6bbd622/UKSmktComp_Emissions_Scope1.ipynb) Scope 1

[Workbook 6](https://colab.research.google.com/drive/1fo6NJ-2t7_VVn99Js8fanx3dGDiVdZud?usp=sharing) Scope 2 Location-based

[Workbook 7](https://colab.research.google.com/drive/1_NcLYci-JUDkaC-Rsi6FOJ8CA38BahGW) Scope 2 Market-based

[Workbook 8](https://colab.research.google.com/drive/1oSahn6j_O1kPpGFbavaFJFIFtFoa8ngS?usp=sharing) Scope 1 and 2 Location-based

[Workbook 9](https://colab.research.google.com/drive/1oSahn6j_O1kPpGFbavaFJFIFtFoa8ngS?usp=sharing) Scope 2 and 2 Market-based

## Results

[Workbook 10](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/1b7534ed6b4adeff83b0be18e91d4745ebde4fde/UKSmktComp_Intensity_Metrics.ipynb) Estimated and Reported Intensity

[Workbook 11](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/01f64ccc4e291482270340595935cfe4f2f1390c/UKSmktComp_Retailer_Comparison.ipynb) Retailer Emission Intensity Comparison

# Files

| File | Description |
|------|-------------|
| geolytix_retailpoints_v34_202412.csv | Raw Geolytix Retail Points |
| geolytix_size_class.csv | Geolytix Retail Points store size classes |
| geolytix_retailpoints_v34_202412_clean.csv | Cleaned Geolytix Retail Points |
| geolytix_retailpoints_v34_202412_summary.csv | Cleaned Geolytix Retail Points summarised by retailer and year |
| retailer_data.csv | Retailer attributes |
| retailer_emissions.csv | Retailer Emissions and Energy Data |
| retailer_yr.csv | Cleaned Retailer Emissions Data by retailer and year |


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

5. Intensity
Reported intensity values vary in magnitude within and between retailer kpis. Values within retatiler kpi time series that are one or more orders of magnitude different from the majority of values in the time series are 'corrected' by multiplying so that values are equivalent. Similarly, Sainsburys reported Scope 1 Intensity by area are multipled by 100 to align with the values of other retailers. Value changes are recorded in the 'Note' field.

| Business Scope | Description |
|------|-------------|
| UK | UK supermarket operations only |
| UK+ | All UK operations [1] |
| UK and Ireland | UK and Ireland operationa |
| UK and Europe | UK and European operations |
| Global | Global operations |

[1] J Sainsbury plc: Sainsburys, Homebase and Argos
