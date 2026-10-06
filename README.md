# Financial Consumer Complaint Intelligence

> An interactive Power BI analytics product for understanding consumer complaints across financial products, companies, response performance, disputes, and geographic patterns.

![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-F2C811?style=flat\&logo=powerbi\&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data%20Modeling-1F4E79?style=flat)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-217346?style=flat)
![Dataset](https://img.shields.io/badge/Records-1.47M%2B-19C3B1?style=flat)


## Overview

Financial Consumer Complaint Intelligence transforms 1.47M+ consumer complaint records into a multi-page Power BI analytical product.

The dashboard is designed around five questions:

1. What is happening across the consumer-finance complaint landscape?
2. Why are consumers complaining?
3. Where is complaint pressure concentrated across companies?
4. How effectively are complaints being handled?
5. Where is complaint pressure concentrated geographically?

## Dashboard

The report contains five primary analytical pages:

| Page | Question |
|---|---|
| Consumer Pulse | What is happening? |
| Complaint Intelligence | Why are consumers complaining? |
| Company Intelligence | Where is complaint pressure concentrated? |
| Response & Resolution | How effectively are complaints handled? |
| Geographic Intelligence | Where is complaint pressure concentrated geographically? |

## Dataset

**Source:** Consumer Financial Protection Bureau Consumer Complaint Database

**Kaggle distribution:**  
https://www.kaggle.com/datasets/taeefnajib/bank-customer-complaints

### Dataset scale

- 1,473,407 records
- December 2011 – December 2019
- 16 source fields

## Data Model

The Power BI model uses:

### Fact

`Fact_Complaints`

### Dimensions

- `Dim_Date`
- `Dim_Product`
- `Dim_Issue`
- `Dim_Company`
- `Dim_Geography`

## Core Metrics

- Total Complaints
- YoY Complaint %
- Timely Response %
- Median Response Days
- P90 Response Days
- Complaint Volume
- Complaint Share
- Dispute Rate

## Methodology

The project includes dedicated documentation covering:

- Data preparation
- Data quality
- Response-time analysis
- CFPB taxonomy changes
- Analytical methodology
- Dashboard architecture

See the [`methodology`](methodology/) directory.

## Data Quality

Important limitations include:

- Missing Sub-issue, Sub-product, State and ZIP values
- 7,052 negative response-duration records
- CFPB complaint taxonomy change in April 2017
- No population data for population-normalized geographic rates

These limitations are documented rather than hidden.

## Interactivity

The report includes:

- Interactive filters
- Cross-filtering
- Decomposition tree
- Company drill-through
- Report-page tooltips
- Page navigation

## Repository Structure

```text
data/          Source and field documentation
images/        Dashboard screenshots
methodology/   Data and analytical methodology
powerbi/       Power BI report
docs/          Dashboard usage and project notes
```

## Dashboard Preview

A clean dashboard overview image can be added here once the final screenshots have been captured.

## Live Dashboard

**Power BI:**  
`[https://app.powerbi.com/groups/me/reports/baa9483c-0f9e-424a-b222-9d9bb7e649a1/22d93354437ff7b43a56?experience=power-bi]`

## Tools

- Microsoft Power BI
- Power Query
- DAX
- Data modeling
- Data visualization
- Business intelligence

## Author

**Akpan Daniel**

Data Analyst | Community Analytics | Business Intelligence

Focus areas include:

- Power BI
- DAX
- Python
- Product Analytics
- Marketing Analytics
- Web3 Analytics
- Data Visualization

## Dataset Attribution

The underlying complaint data originates from the CFPB Consumer Complaint Database and is distributed through Kaggle.

Dataset ownership and licensing remain with the original data provider.
