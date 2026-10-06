

# Methodology

## Analytical Pipeline

The project follows a structured process from source data inspection to interactive business intelligence.

```text
CFPB Consumer Complaint Data
            ↓
      Data Inspection
            ↓
   Data Quality Assessment
            ↓
   Power BI Data Modeling
            ↓
      DAX Measures
            ↓
   Analytical Visualization
            ↓
 Interactive Intelligence Product
```



## 1. Source Data

The project begins with the CFPB Consumer Complaint Database distributed through Kaggle.

The dataset contains more than **1.47 million consumer complaint records** covering December 2011 through December 2019.



## 2. Data Inspection

The dataset was inspected for:

* Record volume
* Date coverage
* Missing values
* Categorical consistency
* Response-time behavior
* Geographic completeness
* Complaint classification structure

This inspection was used to identify analytical limitations before dashboard development.



## 3. Data Modeling

The Power BI model uses a fact-and-dimension structure.

### Fact

`Fact_Complaints`

### Dimensions

* `Dim_Date`
* `Dim_Product`
* `Dim_Issue`
* `Dim_Company`
* `Dim_Geography`

This structure supports reusable filtering and consistent measures across all dashboard pages.



## 4. Measures

DAX measures were created only where required for the analytical experience.

Examples include:

* Complaint volume
* Year-over-year complaint change
* Timely response percentage
* Median response days
* P90 response days
* Dispute rate
* Complaint share



## 5. Dashboard Architecture

The report is divided into five analytical pages:

1. Consumer Pulse
2. Complaint Intelligence
3. Company Intelligence
4. Response & Resolution
5. Geographic Intelligence

Each page answers a different business question rather than repeating the same KPI and chart structure.



## 6. Interaction Layer

The final report includes:

* Slicers
* Cross-filtering
* Interactive decomposition analysis
* Company drill-through
* Contextual report-page tooltips
* Page navigation

This allows the dashboard to function as an analytical product rather than a static report.



## 7. Analytical Principles

The analysis avoids unsupported conclusions.

In particular:

* High complaint volume is not automatically treated as poor company performance.
* Geographic complaint volume is not treated as a population-adjusted rate.
* Historical classification changes are documented rather than ignored.
* Missing values are not blindly fabricated.
* Response-time anomalies are documented rather than hidden.
