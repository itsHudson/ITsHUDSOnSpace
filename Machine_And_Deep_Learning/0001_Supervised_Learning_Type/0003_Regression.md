# 3. REGRESSION (PREDICT CONTINUOUS VALUES / ESTIMATION)

This section explains **Regression**, the second major branch of **Supervised Learning (SL)**.

Classification predicts:

- Spam / Not Spam
- Approve / Reject

Regression predicts:

- House Price = RM500,000
- Temperature = 32.5°C
- Sales = 8,000 units

Regression answers:

```text
"What exact numerical value should be predicted?"
```

---

## 3.1 Regression Examples Used Throughout This Section

This section introduces the examples reused throughout the entire regression topic.

| Example | Input | Output | Regression Type | Real Use Case |
| --- | --- | --- | --- | --- |
| House Price Prediction | House details | RM500,000 | Multiple Regression | Real estate |
| Salary Prediction | Experience + education | RM8,000/month | Simple/Multiple Regression | HR hiring |
| Temperature Prediction | Weather data | 32.5°C | Time Trend Regression | Weather forecasting |
| Sales Forecasting | Historical sales | 8,000 units | Forecasting Regression | Business planning |
| Demand Forecasting | Customer demand history | 5,000 units | Forecasting Regression | Inventory planning |

---

# 3.2 What is Regression?

This section explains the basic meaning of regression.

Regression predicts continuous numerical values.

---

## 3.2.1 Core Formula

This section explains the basic regression formula.

```text
Input (X) → Model → Numerical Output (Y)
```

```text
f(X) = Y
```

---

## 3.2.2 Step-by-Step Regression Process

This section explains the overall regression workflow.

```text
1. Collect historical data
2. Add correct numerical labels
3. Train regression model
4. Learn numerical relationships
5. Predict future values
```

---

## 3.2.3 Example A: House Price Prediction (Detailed)

```text
1. New house data arrives:
   - Size = 2,000 sqft
   - Bedrooms = 4
   - Location = Kuala Lumpur
   - House age = 5 years

2. Model extracts features

3. Model compares with historical house sales

4. Model finds similar houses

5. Model predicts:
   RM850,000

6. Real estate platform shows estimated price
```

---

## 3.2.4 Example B: Temperature Prediction (Detailed)

```text
1. Weather data enters system:
   - Humidity = 85%
   - Wind speed = 10 km/h
   - Rainfall = Low

2. Model compares historical weather patterns

3. Model predicts tomorrow temperature

4. Final prediction:
   32.5°C
```

---

# 3.3 Input and Output in Regression

This section explains the required components.

| Component | Definition | House Example | Salary Example | Why Important |
| --- | --- | --- | --- | --- |
| Input (X) | Data given to model | House size | Experience | Features for prediction |
| Features | Individual variables | Location | Education | Improve accuracy |
| Output (Y) | Numerical value | House price | Salary | Final prediction |
| Label | Correct answer during training | Actual price | Actual salary | Required |
| Prediction | Future estimated value | RM850,000 | RM9,000 | Final output |

---

## 3.3.1 Example A: Salary Prediction (Detailed)

```text
1. Employee profile:
   - Experience = 5 years
   - Degree = Master's
   - Skills = Python + SQL

2. Model compares previous employee salaries

3. Model predicts:

   RM9,500/month
```

---

## 3.3.2 Example B: House Prediction (Detailed)

```text
1. User enters house details

2. Features extracted:
   - Size
   - Location
   - Bedrooms
   - Age

3. Model predicts:

   RM780,000
```

---

# 3.4 Nature of Regression Problems

This section explains how regression outputs behave.

| Topic | Meaning | Example | Why Important | Notes |
| --- | --- | --- | --- | --- |
| Continuous Values | Any number within range | RM500,000 | Flexible output | Infinite possibilities |
| Exact Estimation | Small differences matter | 32.5°C | Precision matters | More precise |
| Trend Prediction | Learn historical trends | Sales forecasting | Business planning | Common use |

---

## 3.4.1 Example A: Sales Forecasting (Detailed)

```text
1. Business checks last 12 months sales

2. Model identifies:
   - Holiday spikes
   - Seasonal drops

3. Predicts next month sales

4. Final output:
   8,500 units
```

---

## 3.4.2 Example B: Stock Price Prediction (Detailed)

```text
1. Historical stock prices collected

2. Model learns price movement trends

3. Predicts tomorrow stock price

4. Final prediction:
   RM120.50
```

---

# 3.5 Types of Regression

This section explains common regression problem structures.

| Type | Input Features | Output | Example | Use Case |
| --- | --- | --- | --- | --- |
| Simple Regression | One feature | One value | Study hours → marks | Beginner |
| Multiple Regression | Multiple features | One value | House price | Most common |
| Polynomial Regression | Non-linear relationship | One value | Population growth | Curved patterns |

---

## 3.5.1 Example A: Simple Regression (Detailed)

```text
1. Student studies 6 hours

2. Model learned:

More study hours → higher marks

3. Predicts:

85 marks
```

---

## 3.5.2 Example B: Multiple Regression (Detailed)

```text
1. House input:
   - Size
   - Location
   - Bedrooms
   - Age

2. Model combines all features

3. Predicts:

RM900,000
```

---

## 3.5.3 Example C: Polynomial Regression (Detailed)

```text
1. Historical population growth data collected

2. Model detects curved growth pattern

3. Predicts future population:

2.5 million people
```

---

# 3.6 Common Regression Algorithms

This section explains commonly used algorithms.

| Algorithm | Full Form | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Linear Regression (LR) | Linear Regression | Best-fit line | Salary prediction | Cannot handle complexity |
| Ridge Regression | Ridge Regression | Reduces overfitting | House price | Keeps all features |
| Lasso Regression | Lasso Regression | Removes weak features | Feature selection | May remove useful features |
| Decision Tree Regressor (DTR) | Decision Tree Regressor | Rule splitting | House pricing | Can overfit |
| Random Forest Regressor (RFR) | Random Forest Regressor | Multiple trees | Sales prediction | Slower |
| Gradient Boosting Regressor (GBR) | Gradient Boosting Regressor | Fixes previous errors | Demand forecasting | Slow training |

---

## 3.6.1 Example A: Linear Regression (Detailed)

```text
1. Collect salary data

2. Model learns:

More experience → higher salary

3. New employee:
   Experience = 7 years

4. Predicted salary:

RM11,000
```

---

## 3.6.2 Example B: Random Forest Regressor (Detailed)

```text
1. Collect housing data

2. Multiple trees make predictions

3. Average prediction calculated

4. Final prediction:

RM780,000
```

---

# 3.7 Regression Output Types

This section explains output forms.

| Output Type | Meaning | Example | Use Case | Notes |
| --- | --- | --- | --- | --- |
| Integer Output | Whole numbers | 5,000 units | Inventory | No decimals |
| Decimal Output | Decimal values | 32.5°C | Weather | Common |
| Range Output | Prediction range | RM400k–RM450k | Risk planning | Less common |

---

## 3.7.1 Example A: Decimal Output (Detailed)

```text
Weather model predicts:

32.5°C
```

---

## 3.7.2 Example B: Range Output (Detailed)

```text
House prediction:

RM450,000 - RM500,000
```

---

# 3.8 Regression Evaluation Metrics

This section explains how regression performance is measured.

| Metric | Full Form | What It Measures | Example | Best Use |
| --- | --- | --- | --- | --- |
| MAE | Mean Absolute Error | Average error | RM10,000 | Easy interpretation |
| MSE | Mean Squared Error | Larger mistakes punished more | House pricing | Large errors matter |
| RMSE | Root Mean Squared Error | Error in original unit | RM20,000 | Easy interpretation |
| R² Score | R-Squared Score | Model explanation strength | 0.85 | Overall performance |

---

## 3.8.1 Example A: Mean Absolute Error (Detailed)

```text
Actual price:
RM500,000

Predicted price:
RM480,000

Error:
RM20,000
```

---

## 3.8.2 Example B: R² Score (Detailed)

```text
R² = 0.85

Meaning:
Model explains 85% of price variation
```

---

# 3.9 Real-World Applications

This section explains practical usage.

| Industry | Input | Output | Example | Business Value |
| --- | --- | --- | --- | --- |
| Real Estate | House details | Price | Property platform | Better pricing |
| Retail | Sales history | Future sales | Inventory planning | Reduce shortages |
| Finance | Stock prices | Future price | Investment | Better decisions |
| Weather | Weather data | Temperature | Forecasting | Planning |

---

## 3.9.1 Example A: Retail Forecasting (Detailed)

```text
1. Store checks previous sales

2. Model predicts next month demand

3. Output:

6,000 units

4. Store prepares inventory
```

---

## 3.9.2 Example B: Weather Forecasting (Detailed)

```text
1. Weather sensors collect data

2. Model predicts tomorrow temperature

3. Output:

31.8°C
```

---

# 3.10 Regression vs Classification

This section explains the difference.

| Regression | Classification | Output Type | Example |
| --- | --- | --- | --- |
| Predict numbers | Predict categories | Number vs Label | House price vs Spam |

---

## 3.10.1 Example A: Regression

```text
House → RM500,000
```

---

## 3.10.2 Example B: Classification

```text
Email → Spam
```

---

# 3.11 Common Problems in Regression

This section explains common issues.

| Problem | Cause | Example | Impact | Solution |
| --- | --- | --- | --- | --- |
| Overfitting | Model too complex | Memorizes prices | Poor future prediction | Regularization |
| Underfitting | Model too simple | Weak predictions | Low accuracy | Better model |
| Outliers | Extreme values | RM50M house | Distorted learning | Data cleaning |
| Missing Data | Missing inputs | Missing salary | Poor prediction | Imputation |

---

## 3.11.1 Example A: Outlier Problem (Detailed)

```text
Most houses:
RM500,000

One house:
RM50,000,000

Model becomes confused
```

---

## 3.11.2 Example B: Missing Data Problem (Detailed)

```text
Missing house location

Model cannot make accurate prediction
```

---

# 3.12 End-to-End Example: House Price Prediction System

This section connects everything.

| Step | Input | Process | Output | Purpose |
| --- | --- | --- | --- | --- |
| 1 | House data | Collect data | Dataset | Training |
| 2 | Prices | Add labels | Labeled data | Learning |
| 3 | Training data | Train model | Regression model | Learn |
| 4 | Testing data | Evaluate | Metrics | Check performance |
| 5 | New house | Predict price | RM850,000 | Real usage |

---

## 3.12.1 Full Pipeline

```text
Collect Data
→ Create Features
→ Add Labels
→ Train Model
→ Evaluate Model
→ Improve Model
→ Deploy Model
→ Predict Future Value
```

---

# 3.13 Final Summary

This section summarizes regression.

Regression predicts numerical values.

```text
Input → Learn Patterns → Predict Number
```

Examples:

```text
House → RM850,000
Temperature → 32.5°C
Sales → 8,000 units
Salary → RM9,500
```
