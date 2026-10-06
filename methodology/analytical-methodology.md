

# Analytical Methodology

## Purpose

The dashboard was designed around five analytical questions rather than around a fixed collection of charts.


## 1. Consumer Landscape

The first page establishes the overall complaint landscape.

Metrics include:

* Total complaints
* Year-over-year complaint movement
* Timely response
* Dispute rate
* Complaint volume over time
* Product concentration
* Geographic concentration

The objective is to understand the scale and direction of complaint activity before moving into deeper analysis.



## 2. Complaint Drivers

The second page focuses on the reasons consumers complain.

The primary analytical dimensions are:

* Product
* Issue

An interactive decomposition tree allows users to explore complaint volume from the overall total into product and issue categories.

This keeps complaint-driver analysis focused rather than mixing unrelated dimensions into the same decomposition.



## 3. Company Intelligence

Company analysis focuses on:

* Complaint concentration
* Response outcomes
* Timely response
* Median response time
* Dispute rate

Complaint volume is treated as an observed concentration metric, not as an automatic quality ranking.

A company with a large complaint volume may also have a larger customer base or greater product exposure.



## 4. Response & Resolution

Response analysis focuses on how complaints are handled after submission.

Primary measures:

### Timely Response %

The percentage of complaints recorded as receiving a timely response.

### Median Response Days

The median number of days between complaint receipt and the recorded date sent to the company.

Median is used because response-duration data can be strongly affected by unusually long records.

### P90 Response Days

The 90th percentile response duration.

This helps expose slower response behavior that may not be visible from the median alone.

### Response Time Band

Response duration is grouped into:

* Same day
* 1–2 days
* 3–5 days
* 6–10 days
* 11–30 days



## 5. Geographic Intelligence

Geographic analysis uses state-level complaint information.

The page examines:

* Geographic complaint concentration
* State × Product patterns
* Dispute rate by state
* State response performance

No population-normalized complaint rate is calculated because population data is not included in the model.


## 6. Interactive Analysis

The report allows users to change the analytical context through:

* Year
* Product
* State
* Company
* Issue

depending on the dashboard page.

Visuals also support cross-filtering where appropriate.



## 7. Drill-Through Analysis

Company-level analysis can be taken further using a dedicated Company Detail drill-through page.

This allows users to move from an aggregate company view into:

* Company complaint volume
* Product profile
* Top issues
* Response outcomes
* Complaint trend



## 8. Interpretation Principle

The dashboard distinguishes between:

**What the data shows**

and

**What the data proves.**

For example, a high complaint count identifies high complaint concentration, but it does not by itself prove poor service quality.

This distinction is maintained throughout the analytical design.
