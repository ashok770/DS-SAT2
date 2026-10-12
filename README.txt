FreshCart Superstores — Synthetic Assessment Dataset
====================================================

IMPORTANT
---------
This is a synthetic dataset created for practicing the FreshCart Data Science assessment.
It is not actual FreshCart company data and should be described as simulated data if asked.

Files
-----
sales.csv       Transaction-level sales records (includes intentional quality issues)
products.csv    Product master data (includes inconsistent category labels)
stores.csv      Store master data
promotions.csv  Promotion campaign details
calendar.csv    Daily calendar features (some flags intentionally missing)

Date coverage: 2024-01-01 through 2025-12-31
Approximate sales row count: 36,432 (including intentionally duplicated rows)

Intentional data quality conditions
-----------------------------------
- Missing promotion codes in some sales records
- Duplicate sales rows
- Inconsistent product category labels
- Zero or negative units and revenue values
- Incomplete holiday, festival, and season flags in calendar.csv

Suggested join keys
-------------------
sales.product_id -> products.product_id
sales.store_id   -> stores.store_id
sales.promotion_code -> promotions.promotion_code (missing codes are expected)
sales.date -> calendar.date

Notes
-----
- Empty promotion_code means no promotion code was recorded; it is not automatically proof
  that the transaction was not promoted.
- Sales are simulated with designed patterns involving weekends, festivals, promotions,
  store formats, and category seasonality. Verify these patterns through analysis rather
  than assuming them.
- Review duplicates before removing them. Since this synthetic data includes exact duplicate
  rows intentionally, document the rule you use.
- No personal or real customer data is included.
