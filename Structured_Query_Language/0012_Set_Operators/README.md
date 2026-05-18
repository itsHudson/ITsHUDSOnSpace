# Section 12: Set Operators

## 12.1 Set Operation Fundamentals
- What set operators are
- Combining result sets
- SQL set theory basics
- Row compatibility requirements

---

## 12.2 UNION
- Combining unique rows
- Duplicate elimination
- Schema matching requirements

---

## 12.3 UNION ALL
- Combining all rows
- Preserving duplicates
- Performance advantages

---

## 12.4 UNION vs UNION ALL
- Duplicate removal differences
- Performance differences
- Use case selection

---

## 12.5 INTERSECT
- Finding common rows
- Duplicate handling
- Multi-query intersections

---

## 12.6 EXCEPT
- Finding missing rows
- Result subtraction
- Duplicate handling

---

## 12.7 MINUS
- Oracle-specific EXCEPT equivalent
- Vendor syntax differences

---

## 12.8 Column Compatibility Rules
- Same column count
- Compatible data types
- Column ordering requirements

---

## 12.9 Data Type Conversion
- Implicit conversions
- Explicit conversions
- Type mismatch handling

---

## 12.10 Ordering Set Results
- ORDER BY after set operations
- Final result sorting

---

## 12.11 Filtering Set Results
- WHERE before set operations
- Filtering final combined results

---

## 12.12 Aggregating Set Results
- Aggregation after unions
- Multi-stage reporting

---

## 12.13 Joins vs Set Operators
- Horizontal combination
- Vertical combination
- Use case differences

---

## 12.14 Set Operations with Subqueries
- Nested unions
- Nested intersections
- Nested exclusions

---

## 12.15 CTE + Set Operators
- Combining WITH clauses
- Modular query design

---

## 12.16 Duplicate Management
- Duplicate removal strategies
- Deduplication costs

---

## 12.17 NULL Behavior
- NULL comparisons
- NULL duplicate handling

---

## 12.18 Performance Considerations
- Sorting overhead
- Hashing overhead
- Large dataset processing
- Distributed execution costs

---

## 12.19 Distributed Set Operations
- Cross-shard unions
- Data movement costs

---

## 12.20 Security Considerations
- Combining restricted datasets
- Access control concerns

---

## 12.21 Debugging Set Operations
- Column mismatch errors
- Unexpected duplicates
- Missing rows

---

## 12.22 Vendor Differences
- EXCEPT support differences
- MINUS support differences
- INTERSECT support differences

---

## 12.23 Set Operator Anti-Patterns
- Using UNION instead of UNION ALL unnecessarily
- Mismatched schemas
- Overcomplicated nested sets

---

## 12.24 Real-World Set Operator Examples
- Multi-region sales merging
- Customer deduplication
- Audit comparison reports
- Data migration validation

---
