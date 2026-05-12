# 3. REGRESSION (PREDICT CONTINUOUS VALUES / ESTIMATION)

This section explains **Regression**, which is another major type of **Supervised Learning (SL)**.

Classification predicts **categories**

Example:
- Spam / Not Spam
- Approve / Reject

Regression predicts **numbers**

Example:
- House Price = RM500,000
- Temperature = 32.5°C

Regression answers:

**"What exact number should be predicted?"**

---

## 3.1 What is Regression?

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Regression | A supervised learning task that predicts continuous numeric values | Model learns relationship between input (X) and numeric output (Y) | House → RM500,000 | One of the two main supervised learning tasks |
| Main Goal | Predict exact numerical values | Learn patterns from historical data | Salary prediction | Output must be a number |
| Output Type | Continuous numeric output | Can produce decimal values | 32.5°C | Not fixed categories |

---

## 3.2 Simple Regression Flow

| Step | Process | Input | Output | Purpose |
| --- | --- | --- | --- | --- |
| 1 | Collect data | House information | Dataset | Prepare training data |
| 2 | Provide labels | House prices | Labeled dataset | Give correct answers |
| 3 | Train model | Historical data | Trained model | Learn relationships |
| 4 | Predict value | New house info | Predicted price | Estimate future value |
| 5 | Evaluate model | Actual vs predicted values | Error score | Measure accuracy |

---

## 3.3 Input and Output in Regression

| Component | Definition | Example | Output | Notes |
| --- | --- | --- | --- | --- |
| Input (X) | Information given to model | House size | Raw data | Features used for prediction |
| Features | Individual variables | Size, location | Input variables | Multiple features possible |
| Output (Y) | Numeric value model predicts | House price | RM500,000 | Continuous value |
| Label | Correct answer during training | Actual house price | Ground truth | Required for training |
| Prediction | Estimated value for new data | Future price | RM550,000 | Final output |

---

## 3.4 Nature of Regression Problems

| Topic | Definition | How It Works | Example | Notes |
| --- | --- | --- | --- | --- |
| Continuous Values | Output can be any number within a range | Model predicts flexible values | Salary prediction | Infinite possible values |
| Exact Estimation | Precise values matter | Small differences matter | Temperature prediction | More precise than classification |
| Trend Prediction | Learns patterns over time | Uses historical trends | Sales forecasting | Common business use |

---

# 3A. TYPES OF REGRESSION

## 3.5 Simple Regression

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Simple Regression | Uses only one input feature | Model learns relationship between one X and one Y | House size → Price | Easiest regression type |
| Straight Line Relationship | Often uses linear relationship | Fits best line | Study hours → marks | Common beginner example |

---

## 3.6 Multiple Regression

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Multiple Regression | Uses multiple input features | Combines multiple variables to predict output | Size + location + age → price | Common in real business datasets |
| Feature Weighting | Each feature gets importance weight | More important features affect output more | Salary prediction | Helps improve accuracy |

---

## 3.7 Polynomial Regression

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Polynomial Regression | Models curved relationships | Uses higher-degree values | Temperature changes | Handles non-linear patterns |
| Curve Fitting | Fits curves instead of straight lines | Captures complex trends | Population growth | More flexible than linear regression |

---

# 3B. REGRESSION ALGORITHMS

## 3.8 Linear Regression (LR)

| Topic | Definition | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Linear Regression (LR) | Basic regression model using straight line relationship | Finds best-fit line | Salary prediction | Cannot handle complex patterns |

---

## 3.9 Polynomial Regression

| Topic | Definition | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Polynomial Regression | Uses curves for prediction | Adds squared/cubic terms | Growth trends | Can overfit |

---

## 3.10 Ridge Regression (L2)

| Topic | Definition | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Ridge Regression (L2) | Reduces overfitting by shrinking weights | Penalizes large weights | House price prediction | Keeps all features |

---

## 3.11 Lasso Regression (L1)

| Topic | Definition | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Lasso Regression (L1) | Removes less important features | Some weights become zero | Feature selection | May remove useful features |

---

## 3.12 Elastic Net

| Topic | Definition | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Elastic Net | Combines Ridge + Lasso | Uses both penalties | Large datasets | Requires tuning |

---

## 3.13 Decision Tree Regressor (DTR)

| Topic | Definition | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Decision Tree Regressor (DTR) | Tree-based regression model | Splits data into rules | House pricing | Can overfit |

---

## 3.14 Random Forest Regressor (RFR)

| Topic | Definition | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Random Forest Regressor (RFR) | Uses multiple regression trees | Averages predictions | Sales prediction | Slower training |

---

## 3.15 Gradient Boosting Regressor (GBR)

| Topic | Definition | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Gradient Boosting Regressor (GBR) | Improves errors step-by-step | New models fix old errors | Demand forecasting | Can be slow |

---

# 3C. REGRESSION OUTPUT TYPES

## 3.16 Numeric Output

| Output Type | Definition | Example | Why Important | Notes |
| --- | --- | --- | --- | --- |
| Integer Output | Whole number output | Predict 100 sales | Easy interpretation | No decimals |
| Decimal Output | Fraction values | Temperature = 32.5°C | More precise | Common |
| Range Output | Predicted range | RM400k–RM450k | Useful for uncertainty | Less common |

---

## 3.17 Prediction Interpretation

| Topic | Definition | Example | Why Important | Notes |
| --- | --- | --- | --- | --- |
| Exact Value | Single prediction | RM500,000 | Direct decision-making | Most common |
| Error Margin | Shows uncertainty | ±RM20,000 | Helps risk planning | Optional |

---

# 3D. REGRESSION EVALUATION METRICS

## 3.18 Mean Absolute Error (MAE)

| Topic | Definition | How It Works | Example | When to Use |
| --- | --- | --- | --- | --- |
| Mean Absolute Error (MAE) | Average absolute error | Measures average mistake | RM10,000 error | Easy interpretation |

---

## 3.19 Mean Squared Error (MSE)

| Topic | Definition | How It Works | Example | When to Use |
| --- | --- | --- | --- | --- |
| Mean Squared Error (MSE) | Average squared error | Punishes large mistakes | Large pricing errors | Large errors matter more |

---

## 3.20 Root Mean Squared Error (RMSE)

| Topic | Definition | How It Works | Example | When to Use |
| --- | --- | --- | --- | --- |
| Root Mean Squared Error (RMSE) | Square root of MSE | Returns original unit | RM20,000 | Easier interpretation |

---

## 3.21 R² Score (R-Squared Score)

| Topic | Definition | How It Works | Example | When to Use |
| --- | --- | --- | --- | --- |
| R² Score | Measures how well model explains data | Value between 0 and 1 | 0.85 | Model performance evaluation |

---

# 3E. REGRESSION USE CASES

## 3.22 House Price Prediction

| Input | Process | Output | Business Use | Example |
| --- | --- | --- | --- | --- |
| Size, location | Train regression model | House price | Real estate | RM500,000 |

---

## 3.23 Sales Forecasting

| Input | Process | Output | Business Use | Example |
| --- | --- | --- | --- | --- |
| Historical sales | Learn trends | Future sales | Business planning | Next month sales |

---

## 3.24 Stock Price Prediction

| Input | Process | Output | Business Use | Example |
| --- | --- | --- | --- | --- |
| Past stock prices | Learn patterns | Future price | Investment analysis | RM120.50 |

---

## 3.25 Temperature Prediction

| Input | Process | Output | Business Use | Example |
| --- | --- | --- | --- | --- |
| Weather data | Learn weather patterns | Future temperature | Forecasting | 32.5°C |

---

## 3.26 Demand Forecasting

| Input | Process | Output | Business Use | Example |
| --- | --- | --- | --- | --- |
| Historical demand | Predict future demand | Product quantity | Inventory planning | 5,000 units |

---

## 3.27 Regression vs Classification

| Feature | Regression | Classification | Difference | Example |
| --- | --- | --- | --- | --- |
| Output | Number | Category | Main difference | House price vs Spam |
| Goal | Estimate exact value | Choose class | Different tasks | Salary vs Fraud |
| Example Output | RM500,000 | Approve/Reject | Numeric vs Label | Core difference |

---

## 3.28 Common Problems in Regression

| Problem | Definition | Cause | Example | Solution |
| --- | --- | --- | --- | --- |
| Overfitting | Model memorizes data | Model too complex | Bad future prediction | Regularization |
| Underfitting | Model too simple | Weak learning | Poor accuracy | Better model |
| Outliers | Extreme values | Unusual data | RM50M house | Data cleaning |
| Missing Data | Incomplete inputs | Poor collection | Missing salary | Imputation |

---

## 3.29 Final Summary

| Question | Answer | Example | Notes | Importance |
| --- | --- | --- | --- | --- |
| What does regression do? | Predict numbers | House price | Core supervised learning task | Very important |
| What output does it give? | Continuous values | Temperature | Not categories | Key difference |
| When should it be used? | When exact value matters | Sales forecasting | Common business task | Important |
| Why learn it? | Used in pricing, forecasting, estimation | Stock prediction | Major ML foundation | Essential |
