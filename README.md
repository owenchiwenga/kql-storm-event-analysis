# Project 3 — Storm Event Data Analysis and Anomaly Detection Using KQL

## Overview

This project analyzes historical storm-event data using Kusto Query Language (KQL) in Azure Data Explorer. The goal is to explore event patterns, compare geographic distributions, examine reported damage, and identify states with comparatively high event counts.

## Objectives

- Explore the structure and contents of the StormEvents dataset.
- Identify states with the highest numbers of recorded events.
- Analyze the most frequently recorded storm-event types.
- Compare reported property and crop damage across event types.
- Screen for states with event counts above a selected threshold.
- Document the findings using KQL queries and screenshots.

## Tools Used

- Azure Data Explorer
- Kusto Query Language (KQL)
- GitHub

## Investigation Workflow

1. Inspect the dataset schema.
2. Review sample records.
3. Count recorded events by state.
4. Count events by type.
5. Aggregate reported property and crop damage.
6. Compare state-level event counts against a threshold.
7. Document the findings and limitations.

## Evidence

Screenshots of the queries and their results will be stored in the `screenshots/` folder.

## Important Limitations

This project uses a sample dataset. The results describe the records available in that dataset and should not automatically be interpreted as current weather conditions or real-world storm risk.

Any threshold-based results are exploratory and do not, by themselves, establish statistical anomalies or causation.

## Author

Owen Chiwenga

## Disclaimer

This is an educational data-analysis project created to practise KQL and demonstrate data investigation skills.
