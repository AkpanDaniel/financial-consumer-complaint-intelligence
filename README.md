# Financial Consumer Complaint Intelligence

> An interactive Power BI analytics product for understanding consumer complaints across financial products, companies, response performance, disputes, and geographic patterns.

![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-F2C811?style=flat\&logo=powerbi\&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data%20Modeling-1F4E79?style=flat)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-217346?style=flat)
![Dataset](https://img.shields.io/badge/Records-1.47M%2B-19C3B1?style=flat)

## Overview

Financial consumer complaints contain more information than simple complaint counts. They can reveal recurring product issues, concentration across companies, differences in response performance, dispute patterns, and geographic variation.

This project transforms more than **1.47 million consumer complaint records** into an interactive Power BI intelligence product designed to answer five questions:

1. **What is happening across the consumer-finance complaint landscape?**
2. **Why are consumers complaining?**
3. **Where is complaint pressure concentrated across companies?**
4. **How effectively are complaints being handled?**
5. **Where is complaint pressure concentrated geographically?**

The dashboard was designed as a multi-page analytical product rather than a collection of standalone charts. Each page has a specific analytical purpose while maintaining a consistent fintech/product-analytics interface.


## Dashboard

### 1. Consumer Pulse

**Question:** What is happening across the consumer-finance complaint landscape?

The executive overview tracks complaint volume, response health, dispute rate, complaint trends, product concentration, and geographic concentration.

Key elements include:

* Total complaint volume
* Year-over-year complaint movement
* Timely response performance
* Median and P90 response context
* Complaint volume over time
* Complaint concentration by product
* Complaint concentration by state
* Dynamic complaint-driver panel


### 2. Complaint Intelligence

**Question:** Why are consumers complaining?

This page moves from overall volume into the underlying complaint taxonomy.

Key elements include:

* Top complaint issues
* Product × Issue breakdown
* Interactive decomposition tree
* Product-level complaint concentration
* CFPB taxonomy-change methodology note

A particularly important analytical consideration is the **April 2017 taxonomy change**, when the CFPB expanded the complaint classification structure.

Because of this change, issue and sub-issue classifications across the boundary should not automatically be interpreted as directly comparable. The dashboard preserves the original taxonomy rather than rewriting historical categories.


### 3. Company Intelligence

**Question:** Where is complaint pressure concentrated, and how are companies responding?

This page examines company-level complaint volume and response outcomes without treating complaint volume as a direct measure of company quality.

Key elements include:

* Complaint volume by company
* Company response outcomes
* Company complaint-pressure scatter analysis
* Timely response performance
* Median response time
* Dispute rate
* Company profile analysis

Complaint volume is treated as **complaint concentration**, not as a ranking of "worst" companies. A higher complaint count can reflect many factors, including customer base size, product exposure, reporting behavior, and business scale.


### 4. Response & Resolution

**Question:** How effectively are consumer complaints being handled?

This page focuses specifically on the response process.

Key elements include:

* Timely response rate
* Median response time
* P90 response time
* Response-time bands
* Median response by product
* Timely response by product
* State/company response performance analysis

Response-time analysis uses the dataset's response-time bands, including:

* Same day
* 1–2 days
* 3–5 days
* 6–10 days
* 11–30 days

The dataset also contains a small number of records with negative calculated response durations, so response-time metrics are interpreted with underlying date quality in mind.


### 5. Geographic Intelligence

**Question:** Where is complaint pressure concentrated geographically?

The final analytical page examines geographic concentration and how complaint patterns vary across states.

Key elements include:

* Geographic complaint concentration
* State × Product patterns
* Dispute rate by state
* State response performance
* Complaint volume
* Timely response performance

The project deliberately does **not** use population-normalized complaint rates because population data was not part of the source dataset. Geographic comparisons therefore focus on observed complaint volume and complaint-related performance measures.


## Key Metrics

The model includes analytical measures such as:

| Metric               | Purpose                                                  |
| -------------------- | -------------------------------------------------------- |
| Total Complaints     | Overall complaint volume                                 |
| YoY Complaint %      | Year-over-year change in complaint volume                |
| Timely Response %    | Share of complaints receiving a timely response          |
| Median Response Days | Typical response duration                                |
| P90 Response Days    | Response duration for the slower end of the distribution |
| Dispute Rate         | Share of complaints marked as disputed                   |
| Complaint Share      | Complaint concentration within the selected context      |


## Data

### Source

**Consumer Financial Protection Bureau (CFPB) Consumer Complaint Database**

The project uses the Kaggle-hosted dataset:

`taeefnajib/bank-customer-complaints`

The underlying records originate from the CFPB Consumer Complaint Database.

### Dataset scale

* **1,473,407 complaints**
* Date range: **December 2011 – December 2019**
* 16 source columns
* Financial products, issues, companies, states, submission channels, response information, and consumer dispute information

### Major source fields

* Complaint ID
* Date received
* Product
* Sub-product
* Issue
* Sub-issue
* Company
* State
* ZIP code
* Submitted via
* Date sent to company
* Timely response?
* Consumer disputed?
* Company response to consumer


## Data Model

The Power BI model uses a dimensional structure built around the complaint fact table.

### Fact

`Fact_Complaints`

### Dimensions

* `Dim_Date`
* `Dim_Product`
* `Dim_Issue`
* `Dim_Company`
* `Dim_Geography`

This structure separates transactional complaint records from reusable analytical dimensions and allows the dashboard pages to share consistent filtering and measures.


## Data Quality Considerations

Several source-data characteristics were considered during the analysis.

### Missing classifications

Some complaints do not contain values for:

* Sub-product
* Sub-issue
* State
* ZIP code

These values were not artificially filled simply to make the dashboard appear complete.

### Response-time quality

Calculated response durations include a small number of negative values. These records were retained rather than silently removed, with the limitation documented in the dashboard.

### Taxonomy change

The CFPB changed its complaint classification structure in April 2017.

This increased the available issue and sub-issue categories. Historical classifications are therefore preserved and comparisons across the taxonomy boundary are interpreted carefully.


## Design Approach

The dashboard was intentionally designed around **analytical questions rather than chart quantity**.

Each page has a distinct purpose:

| Page                    | Analytical focus                   |
| ----------------------- | ---------------------------------- |
| Consumer Pulse          | Overall complaint landscape        |
| Complaint Intelligence  | Complaint drivers                  |
| Company Intelligence    | Company concentration and outcomes |
| Response & Resolution   | Response performance               |
| Geographic Intelligence | Geographic patterns                |

The visual design follows a light fintech/product-analytics style with:

* Compact filters
* High information density without visual clutter
* Strong whitespace
* Consistent typography
* Restrained teal/blue accents
* Interactive cross-filtering
* Drill-through analysis
* Contextual report-page tooltips
* Page navigation


## Interactivity

The report includes:

* Cross-filtering between visuals
* Page-level filtering
* Product, company, state and year filtering
* Interactive decomposition analysis
* Company drill-through
* Contextual company tooltips
* Contextual state tooltips
* Multi-page navigation

The drill-through experience allows users to move from high-level company analysis into a focused company detail view.


## Tools

**Power BI**

* Power Query
* DAX
* Data modeling
* Interactive visualizations
* Drill-through
* Report-page tooltips
* Navigation

**Data source**

* CFPB Consumer Complaint Database
* Kaggle dataset distribution


## Project Outcomes

The project demonstrates how a large public complaints dataset can be transformed into an interactive intelligence product that supports questions around:

* Complaint concentration
* Product-level issues
* Company response patterns
* Response efficiency
* Consumer disputes
* Geographic variation
* Data quality and taxonomy changes

Rather than treating the dashboard as a reporting exercise, the project focuses on turning raw complaint records into a structured analytical experience.

## Dataset

The analysis uses the CFPB Consumer Complaint Database distributed through Kaggle.

**Kaggle dataset:**
https://www.kaggle.com/datasets/taeefnajib/bank-customer-complaints


## Author

**Akpan Daniel**

Data Analyst | Community Analytics | Business Intelligence

Focus areas:

* Power BI
* DAX
* Python
* Marketing & Product Analytics
* Data Visualization
* Web3 Analytics


## License

This project is intended for portfolio and educational purposes. Dataset ownership and licensing remain with the original data provider.
