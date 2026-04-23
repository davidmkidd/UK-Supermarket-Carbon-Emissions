
![UK Supermarket Logo](https://github.com/davidmkidd/UK-Supermarket-Carbon-Emissions/blob/main/logos.png)

<br>

# UK Supermarket Carbon Emissions

> ***A practical tutorial for analysing real‑world environmental data***

---

## Overview

Environmental managers are increasingly expected to work with secondary and archival data: company annual reports, ESG disclosures, and public datasets that were not created for academic analysis. These data are often incomplete, inconsistent, and difficult to compare — but they are exactly the data you will encounter in professional practice.

This repository provides a guided, hands‑on tutorial designed for MSc Environmental Management students. Using UK supermarket carbon emissions as a case study, you will learn how to analyse real corporate data, calculate meaningful metrics, and communicate results clearly and responsibly.

No prior experience with programming or data analysis is assumed.

## Why UK supermarkets?

UK supermarkets are well suited to teaching applied environmental data skills because:

they publish carbon and energy data in annual and ESG reports
they vary greatly in size, business model, and reporting practice
they are familiar organisations, making results easier to interpret
they raise important questions about responsibility, scale, and intensity rather than simple “league tables”

The focus of this tutorial is not ranking supermarkets as “good” or “bad”, but learning how environmental data can — and cannot — support decision‑making.

---

## Learning outcomes

By completing this tutorial, you will be able to:

* explain the difference between absolute emissions and emissions intensity
* work confidently with archival and secondary data
* recognise common limitations in self‑reported ESG data
* calculate and interpret emissions intensity metrics
* produce clear, publication‑quality graphs suitable for reports and presentations
* critically interpret trends and differences between organisations

These skills are central to professional roles in environmental management, sustainability reporting, consultancy, and policy.

---

## What you will work with

The tutorial uses:

* reported Scope 1 and Scope 2 carbon emissions from UK supermarket annual and ESG reports
* reported emissions targets where available
* store opening dates and store size data from the GEOLYTIX Supermarket Retail Points dataset
* derived emissions intensity metrics based on retailer estate characteristics

All data used are secondary, publicly available, and representative of what environmental practitioners typically encounter.

---

## What this tutorial is (and is not)

This tutorial is:

* practical and applied
* based on real data, including gaps and inconsistencies
* focused on interpretation and communication, not just calculation
* suitable for students from non‑quantitative backgrounds

This tutorial is not:

* a programming course
* an exercise in “clean” or perfectly structured data
* a definitive assessment of supermarket sustainability performance

Uncertainty and imperfection are intentionally part of the learning process.

---

## Structure of the tutorial

The materials are structured to guide you step by step:

1. Understanding the data
> Where the emissions data come from, what they represent, and why they differ.

2. Preparing and structuring data
> Organising reported figures so they can be analysed and visualised.

3. Absolute emissions vs intensity
> Why absolute emissions favour large organisations, and how intensity metrics change interpretation.

4. Visualising emissions and targets
> Creating clear time‑series graphs that distinguish between reported values and targets.

5.  Interpreting results critically
> Understanding what the graphs show — and what they do not show.

Each step builds on the previous one and includes explanation alongside code.

---

## Workbooks

### System and Data

[Workbook 1](/UKSmktComp_UK_Supermarket_Retailer.ipynb) Introduction to carbon reporting and supermarket emissions.

[Workbook 2](/UKSmktComp_Stores_Cleaning.ipynb) Clean and summarise the Geolytix Retail Points dataset of UK supermarket outlets

[Workbook 3](/UKSmktComp_Stores_Graphing.ipynb) Explore retailer store estate portfolios

[Workbook 4](/UKSmktComp_Emissions_Cleaning.ipynb) Clean, summarise, and scale emissions and energy data

### Absolute and Intensity by Scope

For each Scope:

1. Absolute retailer emsssions time series are plotted.
2. Scaling of emissions with store number and area are tested with linear regression.
3. Emissions are scaled to intensity using the best scaling model.


[Workbook 5](/UKSmktComp_Emissions_Scope1.ipynb) Scope 1

[Workbook 6](/UKSmktComp_Emissions_Scope2_Location.ipynb) Scope 2 Location-based

[Workbook 7](/UKSmktComp_Emissions_Scope2_Market.ipynb) Scope 2 Market-based

[Workbook 8](/UKSmktComp_Emissions_Scope1and2_Location.ipynb) Scope 1 and 2 Location-based

[Workbook 9](/UKSmktComp_Emissions_Scope1and2_Market.ipynb) Scope 2 and 2 Market-based

### Results

[Workbook 10](/UKSmktComp_Intensity_Metrics.ipynb) Estimated and Reported Intensity

[Workbook 11](/UKSmktComp_Retailer_Comparison.ipynb) Retailer Emission Intensity Comparison

---

## Important assumptions and limitations
This tutorial makes several important assumptions that reflect real‑world practice:

* Emissions data are self‑reported and reflect company reporting decisions
* Not all retailers report data consistently across years
* Intensity estimates rely on store size and opening data, which introduce uncertainty
* Scope 3 emissions are not included due to reporting inconsistency

These limitations are not flaws in the exercise. They are central to understanding how environmental data are used responsibly in professional contexts.

## Software and skills
The tutorial uses R for data analysis and visualisation.

* No prior experience with R is required
* Code is provided with explanation
* The emphasis is on understanding outputs, not memorising syntax

Students are encouraged to focus on interpretation rather than technical perfection.

---

## How to use this repository

* Read this README first for context
* Work through the tutorial materials in order
* Use the comments and explanations to guide your understanding
* Focus on *why* each step is taken, not just how

This repository is suitable for use in taught sessions, workshops, or independent study.
---

## How this supports your MSc and future work
The skills developed here are directly transferable to:

* environmental management and sustainability roles
* ESG reporting and analysis
* consultancy and advisory work
* local authority and NGO environmental projects

You will practise working with the same kinds of data, constraints, and trade‑offs faced by professionals in the field.

---

## Acknowledgements
Store location and size information are derived from the GEOLYTIX Supermarket Retail Points dataset. Emissions data are taken from publicly available company reports.
All analysis is for teaching purposes only.
---

## Author
David M. Kidd
Senior Lecturer, 
Dept. of Geography, Geology, and the Environment
Kingston University London


## Files

| File | Description |
|------|-------------|
| geolytix_retailpoints_v34_202412.csv | Raw Geolytix Retail Points |
| geolytix_size_class.csv | Geolytix Retail Points store size classes |
| geolytix_retailpoints_v34_202412_clean.csv | Cleaned Geolytix Retail Points |
| geolytix_retailpoints_v34_202412_summary.csv | Cleaned Geolytix Retail Points summarised by retailer and year |
| retailer_data.csv | Retailer attributes |
| retailer_emissions.csv | Retailer Emissions and Energy Data |
| retailer_yr.csv | Cleaned Retailer Emissions Data by retailer and year |


