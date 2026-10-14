# Investigation Report — Storm Event Data Analysis Using KQL

## 1. Project Overview

This project explores the StormEvents sample dataset using Kusto Query Language (KQL) in Azure Data Explorer. The analysis examines recorded event distribution, event types, reported property and crop damage, and states with comparatively high event counts.

## 2. Objectives

- Inspect the dataset schema and sample records.
- Identify states with the highest recorded event counts.
- Identify the most frequently recorded event types.
- Compare reported property and crop damage by event type.
- Apply a simple threshold to screen for states with comparatively high event counts.
- Document the investigation using reproducible KQL queries and screenshots.

## 3. Tools and Dataset

- **Platform:** Azure Data Explorer
- **Query language:** Kusto Query Language (KQL)
- **Dataset:** StormEvents sample dataset
- **Documentation:** GitHub

## 4. Methodology

### Step 1 — Dataset Inspection

Used `getschema` to inspect the available columns and data types, followed by `take 10` to review sample records.

### Step 2 — Geographic Distribution

Grouped records by state, counted the events, and sorted the results in descending order to identify the states with the highest recorded counts.

### Step 3 — Event-Type Analysis

Grouped records by event type and sorted by count to identify the most frequently recorded event types.

### Step 4 — Reported Damage Analysis

Aggregated the `DamageProperty` and `DamageCrops` fields by event type to compare reported damage values.

**Interpretation note:** Damage values must be interpreted according to the dataset's documented units and conventions. They should not automatically be described as dollar totals without verification.

### Step 5 — Threshold-Based Screening

Calculated the average number of recorded events per state and screened for states whose counts exceeded twice that average.

This is an exploratory threshold, not a formal statistical anomaly-detection method. A high count alone does not establish unusual weather, causation, or elevated real-world risk.

## 5. Findings

The query outputs and screenshots provide evidence of the dataset structure, geographic distribution, event-type frequency, reported damage fields, and threshold-screening results.

Specific rankings and values should be taken directly from the captured query results rather than inferred or assumed.

## 6. Limitations

- The analysis uses a sample dataset and may not represent current weather conditions.
- Results depend on the records and definitions included in the dataset.
- Event counts do not measure event severity by themselves.
- Damage aggregations require confirmation of the dataset's units and scaling conventions.
- The threshold-based screen is exploratory and does not prove statistical anomalies or causation.

## 7. Conclusion

This project demonstrates practical KQL skills, including schema inspection, aggregation with `summarize`, sorting with `order by`, limiting output with `take`, calculating an average, and applying a threshold using `where`.

The work is an educational data-analysis exercise and is not a cybersecurity incident investigation.

## 8. Evidence

Query results and screenshots are intended to be stored in the `screenshots/` folder. The reusable queries are available in `storm_event_queries.kql`.

## Author

Owen Chiwenga

## Disclaimer

This project was created for educational purposes to practise KQL and demonstrate data investigation and documentation skills.
