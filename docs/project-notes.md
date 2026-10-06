


# Project Notes

## Project Concept

Financial Consumer Complaint Intelligence was developed as a portfolio Business Intelligence project using a large public financial complaint dataset.

The objective was to move beyond a conventional dashboard and create an analytical product with:

- Clear business questions
- Structured data modeling
- Reusable DAX measures
- Page-specific analytical experiences
- Interactive exploration
- Drill-through
- Contextual tooltips
- Consistent product-style navigation



## Dashboard Architecture

The report follows a five-stage analytical flow:

```text
Consumer Landscape
       ↓
Complaint Drivers
       ↓
Company Intelligence
       ↓
Response Performance
       ↓
Geographic Intelligence
```

Each page has a distinct role.



## Design Philosophy

The visual design follows a light fintech/product-analytics style.

Design principles include:

- White analytical cards
- Light page background
- Generous whitespace
- Compact filters
- Restrained use of accent colors
- Minimal unnecessary decoration
- Page-specific KPIs
- Limited chart repetition

The objective was to make the report feel closer to a lightweight analytics product than a traditional Power BI report.



## Why Visuals Are Not Repeated

The five pages intentionally avoid repeating the same chart merely to fill space.

For example:

- Page 1 owns the overall complaint trend.
- Page 2 owns issue analysis.
- Page 3 owns company analysis.
- Page 4 owns response analysis.
- Page 5 owns geographic analysis.

This allows each page to contribute something different to the overall analytical story.



## Analytical Language

The project uses neutral analytical language.

For example:

**Preferred:**

> Company complaint concentration

rather than:

> Worst companies

Similarly:

> State complaint concentration

rather than:

> Worst states

This distinction is important because complaint volume alone does not establish service quality.



## Key Methodological Considerations

### April 2017 taxonomy change

The CFPB expanded its complaint classification structure in April 2017.

Historical classification comparisons therefore require caution.

### Response-time anomalies

The dataset contains a small number of negative response durations.

### Missing values

Sub-issue, Sub-product, State, and ZIP code contain missing records.

### Geographic normalization

Population-normalized complaint rates were not calculated because population data is not included in the model.



## Portfolio Objective

This project demonstrates capability across:

- Data inspection
- Data quality assessment
- Data modeling
- DAX
- Power BI
- Business intelligence
- Data visualization
- Analytical storytelling
- Interactive dashboard design

The emphasis is on turning a large public dataset into a structured decision-support experience.
