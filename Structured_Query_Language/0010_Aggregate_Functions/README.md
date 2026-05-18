# Section 10: Aggregate Functions

## 10.1 Aggregation Fundamentals
- What aggregation means
- Row-level vs summary-level data
- Business reporting use cases
- Aggregation workflow

---

## 10.2 Core Aggregate Functions
- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()

---

## 10.3 COUNT Variations
- COUNT(*)
- COUNT(column)
- COUNT(DISTINCT column)
- NULL behavior in COUNT

---

## 10.4 SUM Operations
- Numeric summation
- Decimal summation
- Overflow concerns
- Financial calculations

---

## 10.5 AVG Operations
- Mean calculations
- Decimal precision
- NULL handling

---

## 10.6 MIN and MAX
- Numeric comparisons
- Date comparisons
- String comparisons

---

## 10.7 DISTINCT Aggregation
- SUM(DISTINCT)
- AVG(DISTINCT)
- COUNT(DISTINCT)
- Performance implications

---

## 10.8 NULL Handling in Aggregates
- Ignored NULL values
- NULL edge cases
- COALESCE usage

---

## 10.9 Conditional Aggregation
- CASE inside aggregates
- Filtered aggregations
- Conditional KPI calculations

---

## 10.10 Grouped Aggregation Preview
- Aggregates with GROUP BY
- Aggregates with HAVING

(Note: Full grouping covered later)

---

## 10.11 Statistical Aggregate Functions
- STDDEV
- VARIANCE
- STDDEV_POP
- STDDEV_SAMP
- VAR_POP
- VAR_SAMP

---

## 10.12 Percentile Aggregates
- PERCENTILE_CONT
- PERCENTILE_DISC
- Median calculations

---

## 10.13 Collection Aggregates
- STRING_AGG
- GROUP_CONCAT
- ARRAY_AGG
- JSON_AGG
- XML aggregation

---

## 10.14 Boolean Aggregates
- BOOL_AND
- BOOL_OR
- EVERY

---

## 10.15 Bitwise Aggregates
- BIT_AND
- BIT_OR

---

## 10.16 Approximate Aggregates
- APPROX_COUNT_DISTINCT
- HyperLogLog concepts
- Big data optimization

---

## 10.17 Window Aggregate Preview
- SUM OVER()
- AVG OVER()
- Running totals preview

(Note: Full window functions covered later)

---

## 10.18 Nested Aggregation
- Aggregates inside subqueries
- Multi-stage aggregation

---

## 10.19 Aggregation Across Joins
- Aggregating joined data
- Duplicate aggregation risks

---

## 10.20 Time-Based Aggregation
- Daily aggregation
- Weekly aggregation
- Monthly aggregation
- Yearly aggregation

---

## 10.21 Aggregation Performance
- Index-assisted aggregation
- Hash aggregation
- Sort aggregation
- Distributed aggregation

---

## 10.22 Aggregation Memory Issues
- Large grouping memory usage
- Spill-to-disk risks

---

## 10.23 Aggregation Debugging
- Incorrect totals
- Duplicate inflation
- Missing NULL handling

---

## 10.24 Vendor Differences
- Function availability differences
- Approximate aggregation support
- JSON aggregation support

---

## 10.25 Aggregation Security
- Sensitive metric exposure
- Aggregated privacy concerns

---

## 10.26 Aggregation Anti-Patterns
- Aggregating duplicated joins
- Using wrong aggregate functions
- Ignoring NULL behavior

---

## 10.27 Real-World Aggregation Examples
- Sales dashboards
- Financial reports
- Healthcare metrics
- User growth analytics
- Inventory summaries

---
