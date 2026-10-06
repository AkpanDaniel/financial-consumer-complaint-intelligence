

# Data Quality & Limitations

Data quality is an important part of interpreting this dashboard.

The dashboard therefore documents several characteristics of the source data rather than treating the dataset as perfectly clean.


## 1. Missing Values

Several categorical and geographic fields contain missing values.

The largest gaps occur in:

* `Sub-issue`
* `Sub-product`
* `State`
* `ZIP code`

Missing values were not automatically converted into invented classifications.


## 2. Response-Time Anomalies

Response-duration analysis identified:

* Minimum response duration: **-1 day**
* Median: **0 days**
* Mean: approximately **2.92 days**
* P90: **6 days**
* P95: **11 days**
* P99: **43 days**
* Maximum: **1,962 days**
* Negative response durations: **7,052 records**

The negative durations indicate inconsistencies between the underlying received and sent dates for a small subset of records.

Consequently, response-time metrics should be interpreted with this limitation in mind.



## 3. Same-Day Responses

A large proportion of complaints have a response duration of zero days.

This is represented in the dashboard as:

**Same day**

rather than treating zero as missing data.



## 4. CFPB Taxonomy Change

The CFPB changed its complaint classification structure in **April 2017**.

The post-change structure contains more available issue classifications than the earlier structure.

This means that a simple comparison of the number of Issue or Sub-issue categories before and after April 2017 could incorrectly imply that consumer complaint behavior itself changed by the same amount.

The dashboard therefore treats this as a methodological consideration.



## 5. Complaint Volume ≠ Company Quality

A company appearing near the top of a complaint-volume chart does not automatically mean that the company performs worse than another company.

Complaint volume can be affected by:

* Customer base size
* Product exposure
* Reporting behavior
* Business scale
* Complaint submission patterns

The dashboard therefore uses neutral language such as:

**Complaint Volume**

and

**Complaint Concentration**

rather than labeling companies as "worst."



## 6. Geographic Limitations

The dataset contains state and ZIP information but does not include population estimates in the current analytical model.

Therefore, the dashboard does not claim to measure:

> complaints per 100,000 residents

or another population-normalized complaint rate.

Geographic analysis focuses on observed:

* Complaint volume
* Dispute rate
* Timely response
* Response duration
* Product patterns


## 7. Historical Coverage

The dataset ends in December 2019.

The dashboard should therefore be interpreted as an analysis of the dataset's historical period rather than a representation of current consumer complaint conditions.


## Overall Data Quality Position

The objective was not to hide imperfections in the source data.

Instead, limitations were identified, documented, and incorporated into the interpretation of the dashboard.
