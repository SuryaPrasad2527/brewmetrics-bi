# BrewMetrics BI

A version-controlled Power BI business intelligence solution for analyzing sales performance at BrewMetrics Coffee Co.

## Project Overview

BrewMetrics Coffee Co. operates Flagship stores, Kiosks, and Drive-Thrus across four cities. This project develops a Power BI analytics solution that allows managers to explore sales performance, seasonal trends, city-level differences, product performance, and store-format performance.

The project also demonstrates a version-controlled BI development workflow using Power BI Project files, GitHub, Git, and GitHub Copilot.

## Technologies Used

* Power BI Desktop
* Power BI Project (.pbip)
* Power Query
* DAX
* Git
* GitHub
* Visual Studio Code
* GitHub Copilot

## Data Model

The source data contains transaction-level sales information including the date, city, store format, category, item, quantity, unit price, and sales amount.

The flat source data was transformed into a star schema.

### Fact Table

#### Fact_Sales

The `Fact_Sales` table contains transaction-level sales information.

Important fields include:

* `sale_id`
* `date`
* `city`
* `store_format`
* `category`
* `item`
* `quantity`
* `unit_price`
* `sales_amount`

### Dimension Tables

#### Dim_Date

Contains date-related information used for time-based analysis.

Fields include:

* Date
* Year
* Month
* Month Number
* Day

#### Dim_City

Contains the cities in which BrewMetrics operates.

#### Dim_Product

Contains product and category information.

The product hierarchy can be analyzed as:

**Category → Item**

#### Dim_StoreFormat

Contains the different store formats:

* Flagship
* Kiosk
* Drive-Thru

The model uses the dimension tables to filter the transaction-level `Fact_Sales` table.

## DAX Measures

The project includes measures for:

* Total Sales
* Previous Month Sales
* Month-over-Month Growth %
* Running Total Sales
* Product Sales Rank
* Average Transaction Value

These measures are used in the Power BI report to support sales analysis.

## Dashboard

The dashboard was designed to allow a manager to explore the sales patterns in the dataset.

The report includes:

* Monthly sales analysis
* City-level sales comparison
* Cold Brew sales trend
* Product ranking
* Sales-related KPI measures
* A slicer for interactive filtering
* City → Store Format drill-down

The dashboard specifically allows the seasonal Cold Brew pattern and differences in city-level performance to be explored.

## Key Insights

### 1. Bengaluru Performance

Bengaluru records the highest total sales among the four cities in the supplied dataset, making it the strongest-performing city in the analysis.

### 2. Cold Brew Seasonality

Cold Brew sales show stronger performance during April and May compared with June in the supplied data. This allows the dashboard to highlight the seasonal pattern built into the dataset.

### 3. Store Format Analysis

The City → Store Format drill-down allows managers to investigate how sales performance differs between Flagship stores, Kiosks, and Drive-Thrus within each city.

## Version Control

The project was developed incrementally using Git and GitHub.

The commit history records the progression from:

1. Initial project setup
2. Star schema creation
3. Individual DAX measures
4. Dashboard development
5. Project documentation

This makes changes to the BI solution traceable and reviewable.

## AI-Assisted Development

GitHub Copilot was used as an assistant during DAX development and documentation. Copilot suggestions were reviewed and modified where necessary rather than being accepted without verification.

The `NOTES.md` file records the Copilot-assisted development process and the corrections made to the generated DAX.
