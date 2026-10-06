
# `data/README.md`

# Data

## Source

This project uses the **Consumer Financial Protection Bureau (CFPB) Consumer Complaint Database**, distributed through Kaggle.

**Kaggle dataset:**
https://www.kaggle.com/datasets/taeefnajib/bank-customer-complaints

The dataset contains consumer complaints about financial products and services, including information about the complaint issue, company, geography, submission channel, response timing, and consumer dispute status.

## Dataset Scale

* Records: **1,473,407**
* Date range: **December 2011 – December 2019**
* Source fields: **16**
* Primary analytical unit: individual consumer complaint

## Raw Fields

The source dataset contains:

* Complaint ID
* Date received
* Product
* Sub-product
* Issue
* Sub-issue
* Company public response
* Company
* State
* ZIP code
* Consumer consent provided?
* Submitted via
* Date sent to company
* Timely response?
* Consumer disputed?
* Company response to consumer

## Data Distribution

The raw CSV is not committed to this repository.

The repository documents the dataset structure, methodology, transformations, and analytical model while referencing the original public source.

## Why This Dataset?

Consumer complaint data provides an opportunity to examine financial-service problems from several analytical perspectives:

* Product-level complaint drivers
* Issue concentration
* Company complaint concentration
* Response performance
* Consumer disputes
* Geographic patterns
* Changes in classification structure over time

The project uses these dimensions to build an interactive financial consumer intelligence product in Power BI.
