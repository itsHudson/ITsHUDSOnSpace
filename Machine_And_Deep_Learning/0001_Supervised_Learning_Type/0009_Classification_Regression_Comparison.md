# 9. CLASSIFICATION vs REGRESSION COMPARISON

This section helps you clearly understand the difference between the two main types of Supervised Learning problems.

Choosing the wrong problem type can completely break your solution.

Example:

```text
Wrong:
Using Classification to predict house price

Output:
"Expensive"

But business needs:
RM850,000
```

Correct:

```text
Use Regression
```

This section answers:

```text
"Should I use Classification or Regression?"
```

---

## 9.1 Comparison Examples Used Throughout This Section

This section introduces examples reused throughout this topic.

| Example | Classification Version | Regression Version | Why Comparison Matters | Industry |
| --- | --- | --- | --- | --- |
| House | Expensive / Cheap | RM850,000 | Label vs number | Real estate |
| Loan | Approve / Reject | Loan amount | Decision vs estimation | Banking |
| Healthcare | Disease type | Blood pressure value | Category vs number | Healthcare |
| E-commerce | Product category | Sales amount | Label vs quantity | Retail |

---

# 9.2 Core Definition

This section explains the biggest difference.

Classification predicts labels.

Regression predicts numbers.

| Aspect | Classification | Regression | Key Difference | Example |
| --- | --- | --- | --- | --- |
| What it predicts | Categories | Numerical values | Label vs Number | Spam vs RM520,000 |
| Goal | Make decision | Estimate value | Decision vs Estimation | Approve loan vs predict salary |

---

## 9.2.1 Example A: Loan System (Detailed)

```text
Customer applies for loan

Classification model:
Approve / Reject

Regression model:
RM50,000 loan amount

Same input
Different outputs
```

---

# 9.3 Output Characteristics

This section explains output behavior.

| Aspect | Classification | Regression | Key Difference | Example |
| --- | --- | --- | --- | --- |
| Output Type | Discrete labels | Continuous numbers | Fixed vs flexible | Fraud vs RM120 |
| Value Range | Limited classes | Infinite values | Finite vs infinite | A/B/C vs any number |
| Probability | Often used | Less common | Confidence vs value | 92% spam |

---

## 9.3.1 Example A: Fraud System (Detailed)

```text
Transaction entered

Classification:
Fraud

Probability:
92%

Regression example:
RM120 predicted stock price
```

---

# 9.4 Problem Structure

This section explains how each problem works.

| Aspect | Classification | Regression | Difference | Example |
| --- | --- | --- | --- | --- |
| Problem Type | Decision problem | Estimation problem | Choose vs Calculate | Disease vs temperature |
| Model Goal | Separate classes | Learn relationships | Boundary vs curve | Spam vs price line |

---

## 9.4.1 Example A: Healthcare (Detailed)

```text
Patient symptoms entered

Classification:
Disease type = Flu

Regression:
Blood pressure = 125 mmHg
```

---

# 9.5 Types

This section explains common subtypes.

| Classification Types | Regression Types | Difference | Example | Output |
| --- | --- | --- | --- | --- |
| Binary | Simple Regression | Two classes vs one feature | Spam vs study hours | Different structures |
| Multi-Class | Multiple Regression | Multiple labels vs multiple features | Animal vs house | Different learning |
| Multi-Label | Polynomial Regression | Multiple labels vs curves | Product tags vs growth | Different outputs |

---

## 9.5.1 Example A: Product System

```text
Classification:
Shoes + Sports + Men

Regression:
Predict monthly sales = 10,000 units
```

---

# 9.6 Algorithms

This section compares common algorithms.

| Classification Algorithm | Regression Algorithm | Difference | Example | Use Case |
| --- | --- | --- | --- | --- |
| Logistic Regression | Linear Regression | Probability vs value | Spam vs salary |
| Decision Tree Classifier | Decision Tree Regressor | Label vs number | Fraud vs house |
| Support Vector Machine (SVM) | Gradient Boosting Regressor | Different outputs | Images vs sales |

---

## 9.6.1 Example A: House System

```text
Wrong:
Logistic Regression → "Expensive"

Correct:
Linear Regression → RM850,000
```

---

# 9.7 Training Behavior

This section explains how learning differs.

| Aspect | Classification | Regression | Difference | Example |
| --- | --- | --- | --- | --- |
| Learning Goal | Separate classes | Reduce numeric error | Class vs value |
| Training Output | Probability | Number | Different outputs |
| Adjustment | Better boundaries | Better fit line | Separation vs fitting |

---

## 9.7.1 Example A: Training Difference

```text
Spam model:
Improve class boundaries

House model:
Reduce RM error
```

---

# 9.8 Evaluation Metrics

This section explains performance measurement differences.

| Classification | Regression | Difference | Example | Meaning |
| --- | --- | --- | --- | --- |
| Accuracy | Mean Absolute Error (MAE) | Correctness vs error size | Spam vs house |
| Precision | Root Mean Squared Error (RMSE) | Different measurement | Fraud vs salary |
| Recall | R-Squared (R²) | Different evaluation | Healthcare vs sales |

---

## 9.8.1 Example A: Spam Evaluation

```text
100 emails tested

90 correct

Accuracy = 90%
```

---

## 9.8.2 Example B: House Evaluation

```text
Actual price:
RM500,000

Predicted:
RM480,000

MAE:
RM20,000
```

---

# 9.9 Data Requirements

This section explains dataset differences.

| Aspect | Classification | Regression | Difference | Example |
| --- | --- | --- | --- | --- |
| Labels | Categories | Numbers | Output format |
| Data Types | Text/images/categories | Mostly numeric | Different inputs |
| Dataset | X + label | X + value | Y structure differs |

---

## 9.9.1 Example A: Dataset Comparison

### Classification Dataset

| Email Text | Label |
| --- | --- |
| Free money | Spam |

---

### Regression Dataset

| House Size | Price |
| --- | --- |
| 2000 sqft | RM850,000 |

---

# 9.10 Core Concept

This section explains the mathematical difference.

| Classification | Regression |
| --- | --- |
| Learn decision boundaries | Learn trend lines/curves |
| Separate classes | Estimate relationships |

---

## 9.10.1 Example A: Visual Thinking

```text
Classification:
Draw line between cats and dogs

Regression:
Draw line through price trends
```

---

# 9.11 Real-World Use Cases

This section compares industry applications.

| Industry | Classification Example | Regression Example | Difference | Value |
| --- | --- | --- | --- | --- |
| Finance | Fraud detection | Stock prediction | Decision vs amount |
| Healthcare | Disease classification | Blood pressure prediction | Category vs measurement |
| Retail | Product category | Sales forecasting | Label vs quantity |

---

## 9.11.1 Example A: Finance (Detailed)

```text
Transaction arrives

Classification:
Fraud / Not Fraud

Regression:
Predict stock price = RM120.50
```

---

# 9.12 Strengths and Weaknesses

This section explains tradeoffs.

| Aspect | Classification | Regression | Risk | Example |
| --- | --- | --- | --- | --- |
| Strength | Clear decisions | Precise values | Different benefits |
| Weakness | Cannot predict numbers | Cannot predict labels | Wrong usage |
| Risk | Misclassification | Large error | Business loss |

---

## 9.12.1 Example A: Wrong Model Choice

```text
Need exact house price

Used classification:
Cheap / Expensive

Business fails because exact value needed
```

---

# 9.13 Tricky Cases

This section explains situations where beginners get confused.

---

## 9.13.1 Age Group vs Exact Age

| Problem | Correct Choice | Why |
| --- | --- | --- |
| Adult/Teen/Senior | Classification | Category output |
| Predict exact age | Regression | Numerical output |

---

## 9.13.2 Salary Range vs Exact Salary

| Problem | Correct Choice | Why |
| --- | --- | --- |
| High/Medium/Low income | Classification | Category |
| Predict RM8,500 | Regression | Number |

---

## 9.13.3 Rating Prediction

```text
1-5 stars can be tricky

Classification:
Treat stars as categories

Regression:
Treat stars as numeric score
```

---

# 9.14 End-to-End Flow Comparison

This section compares full workflow.

| Stage | Classification | Regression | Difference | Example |
| --- | --- | --- | --- | --- |
| Input | Features (X) | Features (X) | Same |
| Output | Label (Y) | Number (Y) | Different |
| Training | Learn boundaries | Learn relationships | Different |
| Prediction | Assign class | Predict value | Different |

---

## 9.14.1 Example A: Full Flow Comparison

### Classification Flow

```text
Email
→ Train spam model
→ Predict Spam
```

---

### Regression Flow

```text
House data
→ Train pricing model
→ Predict RM850,000
```

---

# 9.15 Final Decision Framework

This section helps you quickly decide.

```text
Need category?
→ Classification

Need exact number?
→ Regression
```

---

## 9.15.1 Quick Examples

```text
Spam?
→ Classification

House price?
→ Regression

Disease type?
→ Classification

Sales forecast?
→ Regression
```

---

# 9.16 Final Summary

This section summarizes everything.

```text
Classification = Decision

Regression = Estimation
```

Core difference:

```text
Labels vs Numbers
```

