

# Data Dictionary

## Source Dataset

**Consumer Financial Protection Bureau Consumer Complaint Database**

Kaggle distribution:

https://www.kaggle.com/datasets/taeefnajib/bank-customer-complaints


## Source Fields

| Field                          | Description                                                 | Analytical Role          |
| ------------------------------ | ----------------------------------------------------------- | ------------------------ |
| `Complaint ID`                 | Unique identifier assigned to a consumer complaint          | Complaint identifier     |
| `Date received`                | Date the complaint was received                             | Time analysis            |
| `Product`                      | Financial product associated with the complaint             | Product dimension        |
| `Sub-product`                  | More detailed product classification                        | Product detail           |
| `Issue`                        | Primary issue reported by the consumer                      | Complaint driver         |
| `Sub-issue`                    | More detailed issue classification                          | Complaint detail         |
| `Company public response`      | Public response information associated with the complaint   | Company response context |
| `Company`                      | Company associated with the complaint                       | Company dimension        |
| `State`                        | U.S. state associated with the complaint                    | Geographic dimension     |
| `ZIP code`                     | ZIP code associated with the complaint                      | Geographic detail        |
| `Consumer consent provided?`   | Indicates whether consumer consent information was provided | Data attribute           |
| `Submitted via`                | Channel through which the complaint was submitted           | Submission channel       |
| `Date sent to company`         | Date the complaint was sent to the company                  | Response timing          |
| `Timely response?`             | Indicates whether the response was considered timely        | Response performance     |
| `Consumer disputed?`           | Indicates whether the consumer disputed the response        | Consumer outcome         |
| `Company response to consumer` | Response outcome recorded for the complaint                 | Response outcome         |


## Known Missing Values

The source dataset contains missing values in several categorical/geographic fields.

| Field         | Missing records |
| ------------- | --------------: |
| `Sub-issue`   |         555,259 |
| `Sub-product` |         235,198 |
| `State`       |          24,508 |
| `ZIP code`    |          20,270 |

Other source fields were complete in the inspected dataset.

Missing categorical values were not automatically replaced with fabricated classifications.


## Power BI Model

The Power BI model separates the complaint fact table from reusable analytical dimensions.

### Fact Table

`Fact_Complaints`

### Dimensions

* `Dim_Date`
* `Dim_Product`
* `Dim_Issue`
* `Dim_Company`
* `Dim_Geography`


## Derived / Analytical Fields

The model also supports analytical fields used for dashboard analysis, including:

* Year
* Month
* Year Month
* Response Days
* Response Time Band

### Response Time Band

The response-time grouping used in the dashboard contains:

1. Same day
2. 1–2 days
3. 3–5 days
4. 6–10 days
5. 11–30 days

These bands are used to make response-duration patterns easier to interpret than a raw day-by-day distribution.


## Core Measures

The dashboard uses measures including:

* `Total Complaints`
* `YoY Complaint %`
* `Timely Response %`
* `Median Response Days`
* `P90 Response Days`
* `Complaint Volume`
* `Complaint Share`
* `Dispute Rate`

Additional contextual measures support dynamic complaint-driver and profile panels.


## Interpretation Notes

Complaint count represents observed complaint volume and should not automatically be interpreted as a measure of company quality.

Similarly, geographic complaint volume should not be interpreted as complaints per capita because population data is not included in the current analytical model.
