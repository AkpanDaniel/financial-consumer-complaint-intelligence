


# Data Cleaning & Preparation

## Objective

The preparation stage focused on making the source data suitable for structured analysis while preserving the meaning of the original CFPB records.

The goal was not to aggressively transform the source data, but to create a reliable analytical model while retaining important source-data characteristics.



## Dataset Inspection

The dataset contains:

* **1,473,407 records**
* **16 source fields**
* Date coverage from **December 2011 to December 2019**

The source structure was reviewed before the Power BI model was created.


## Missing Values

Missing values were identified in several fields.

| Field       | Missing records |
| ----------- | --------------: |
| Sub-issue   |         555,259 |
| Sub-product |         235,198 |
| State       |          24,508 |
| ZIP code    |          20,270 |

These missing values were retained rather than being replaced with unsupported assumptions.

This is particularly important for categorical complaint fields because assigning an artificial category could change the analytical distribution.



## Date Preparation

Complaint dates were used to support time-based analysis.

The model provides date-related analytical fields such as:

* Year
* Month
* Year Month

These fields support:

* Complaint trend analysis
* Year filtering
* Year-over-year comparison
* Consistent time-based reporting


## Response-Time Analysis

Response duration is based on the relationship between:

* `Date received`
* `Date sent to company`

The resulting response duration supports:

* Median response days
* P90 response days
* Response-time bands
* Timely-response analysis

The dataset contains a small number of negative response durations. These were documented as a data-quality limitation rather than silently removed from the analytical context.



## Response Time Band

For dashboard usability, response duration is grouped into the following bands:

* Same day
* 1–2 days
* 3–5 days
* 6–10 days
* 11–30 days

These bands provide a more readable view of response behavior than displaying hundreds of individual response-day values.



## Classification Structure

The original complaint classification fields were preserved.

The project does not rewrite historical Product or Issue labels to force them into a single artificial taxonomy.

This is important because the CFPB changed its complaint classification structure in April 2017.



## Preparation Principle

The guiding principle was:

> Preserve source meaning first; transform only where the transformation improves analytical usability without changing the underlying interpretation.
