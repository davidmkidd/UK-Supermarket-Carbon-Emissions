
![UK Supermarket Logo](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/main/logos.png)

<br>

# **Which UK supermarket retailer is the most carbon efficient?**

UK legislation requires many larger businesses to publish total carbon emissions and energy usage figures in their annual reports. Carbon emissions scale with business size, so since 2019 companies have also been required to report at least one intensity metric scaled to a measure of business size, but it is left to the business to select a size demonominator, which may be total revenue, a measure of geographical space, number of sales, or other size measure. The relative carbon intensities of businesses cannot be assessed without a common carbon intensity metric.

The UK Supermarket Comparison (UKSmktComp) tutorial shows how an common area-based intensity metric can be estimated by integrating a primary (collected for this task) archival dataset of UK supermarket retailer carbon emissions data collated from company annual reports with a secondary dataset of UK supermarket stores.

This requires:

1. The dataset of supermarket stores to be explored, cleaned, summarised.
2. The dataset of retailer emissions to be explored, cleaned, summarised.
3. Absolute emissions to be scaled to carbon intensity by retailer store area.
4. Estimated intensity compared to reported intensity.
5. Intensity for emissions components to be calculated from reported KPIs and plotted as a stacked bar chart.

Data are processed and visualised using the [R language](https://www.r-project.org/) within a set of [Google Colab](https://colab.research.google.com/) Workbooks for which no prior knowledge is required. Workbooks are designed to be compleated sequentially but may also be run independently.

# Why?

Students often struggle to understand and effectively employ archival and secondary data to answer research problems.

To effectively undertake such research students need well-developed data literacy skills, including the ability to:

* Find data, as secondary data is collected and distributed by many different organisations for many purposes.
* Understand data, including, how it was collected or created from other data products, compleateness, uncertainty, and use restrictions.
* Adapt research methodolgy based on available data.
* Understand how well the data captures the saliant aspects of the real-world system under investigation.
* Define, implement, and record workflows that clean, transform, and sumarise data for analysis.
* Apply exploratory data analysis techniques to discover pattern.
* Critically evaluate the cause and meaning of pattern.
* Identify and implement analytical approaches to test pattern.
* Critically evaluate results considering the data quality and workflow.
* Locate data and analysis in its enviromental and societal context, e.g. how might the infromation is interpreted.

Tasks that are further be complicated by:

* Data volume as the larger datasets become impossible to curate manually.
* Data complexity - how data is structured in a dataset and relationships between data items and data sets.

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

[Workbook 6](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/23986cf646a57f01adff993cbe1af4b47ab40ce8/UKSmktComp_Emissions_Scope2_Location.ipynb) Scope 2 Location-based

[Workbook 7](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/23986cf646a57f01adff993cbe1af4b47ab40ce8/UKSmktComp_Emissions_Scope2_Market.ipynb) Scope 2 Market-based

[Workbook 8](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/23986cf646a57f01adff993cbe1af4b47ab40ce8/UKSmktComp_Emissions_Scope1and2_Location.ipynb) Scope 1 and 2 Location-based

[Workbook 9](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/23986cf646a57f01adff993cbe1af4b47ab40ce8/UKSmktComp_Emissions_Scope1and2_Market.ipynb) Scope 2 and 2 Market-based

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


