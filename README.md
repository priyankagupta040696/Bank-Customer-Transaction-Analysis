# Bank Customer & Transaction Analysis \| Advanced Excel

## Project Overview

This project analyzes more than 1 million banking transaction records to
understand customer behaviour, transaction patterns, geographic
activity, transaction value distribution, and customer transaction
frequency.

The project demonstrates an end-to-end analytical workflow using
Microsoft Excel, Power Query, the Excel Data Model, PivotTables,
PivotCharts, slicers, a timeline, and an interactive dashboard.

## Business Objective

Analyze customer and transaction behaviour to identify: - Transaction
activity and value - Customer transaction frequency - Geographic
transaction patterns - Customer age-group behaviour - Transaction amount
distribution - Time-of-day transaction patterns

## Dataset

**Dataset:** Bank Customer Segmentation (1M+ Transactions)\
**Source:** Kaggle\
**Author:** shivamb

Raw dataset: - 1,048,567 transaction records - 9 original columns -
884,265 unique customers

Key fields include CustomerID, CustomerDOB, CustGender, CustLocation,
CustAccountBalance, TransactionDate, TransactionTime, and
TransactionAmount (INR).

See `documentation/dataset_source.md` for source details.

## Tools & Skills

-   Microsoft Excel
-   Power Query
-   Data Cleaning & Transformation
-   Data Profiling and Validation
-   Excel Data Model
-   PivotTables and PivotCharts
-   Slicers and Timeline
-   Customer Segmentation
-   KPI Reporting
-   Interactive Dashboard Design

## Data Cleaning

-   Corrected TransactionDate parsing using the appropriate locale.
-   Replaced invalid DOB placeholders (`1/1/1800`) and `nan` values with
    null.
-   Retained missing DOBs rather than artificially imputing customer
    ages.
-   Retained undocumented gender code `T` without assigning an
    unsupported meaning.
-   Converted blank gender and location values to `Unknown`.
-   Retained missing account balances as null rather than replacing them
    with zero or an average.
-   Retained legitimate zero account balances.
-   Retained zero-value transactions because there was insufficient
    evidence to classify them as errors.
-   Preserved high-value transaction outliers where no evidence
    indicated invalid data.
-   Validated that all 1,048,567 transaction records remained after
    cleaning.

## Feature Engineering

Created analytical fields including: - Customer Age - Age Group -
Transaction Month - Day of Week - Time Band - Transaction Amount Band -
Customer Transaction Frequency Segment

A separate customer-level summary was created in Power Query to analyze
transaction frequency and total customer transaction value.

## Key KPIs

  KPI                            Result
  --------------------------- ---------
  Total Transactions              1.05M
  Unique Customers               884.3K
  Total Transaction Value        ₹1.65B
  Average Transaction Value      ₹1,574
  Average Account Balance       ₹115.4K

## Key Findings

-   Approximately 83.8% of customers appear only once within the
    observed transaction extract.
-   Around 51.7% of transactions are below ₹500.
-   Evening records the highest transaction volume, followed by
    Afternoon.
-   The 25--34 age group accounts for the largest transaction volume.
-   Mumbai leads the Top 10 locations by transaction volume and
    transaction value.
-   Transaction-date coverage becomes incomplete toward the end of the
    dataset, so late-period declines should not be interpreted as
    confirmed business deterioration.

## Dashboard

![Bank Customer & Transaction Analysis
Dashboard](images/bank_transaction_dashboard.png)

The interactive Excel dashboard includes five dynamic KPI cards, daily
transaction volume, Top 10 locations, time-of-day analysis, amount-band
analysis, customer-frequency analysis, slicers, and a transaction-date
timeline.

## Business Recommendations

-   Investigate behavioural differences between one-time and repeat
    customers.
-   Consider transaction activity by time of day when evaluating
    operational capacity requirements.
-   Use transaction-value and customer-frequency segmentation for deeper
    customer behaviour analysis.
-   Perform deeper analysis of high-volume geographic markets such as
    Mumbai and New Delhi.
-   Improve date completeness and demographic data quality for future
    longitudinal analysis.

## Limitations

-   Transaction-date coverage is irregular and becomes incomplete toward
    the end of the observation period.
-   Customer frequency represents activity within the available dataset
    and should not be interpreted as long-term customer retention.
-   Missing demographic information was retained as `Unknown`/null
    rather than inferred or imputed without supporting evidence.

## Project Workflow

**Raw Data → Data Profiling → Cleaning → Validation → Feature
Engineering → Data Model → PivotTable Analysis → Customer Segmentation →
Interactive Dashboard → Business Insights**
