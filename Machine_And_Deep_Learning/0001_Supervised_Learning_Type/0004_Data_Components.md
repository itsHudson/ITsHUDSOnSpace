# 4. DATA COMPONENTS

This section explains the building blocks of Machine Learning (ML) data.

A model learns from data.

If the data is:

- incomplete
- wrong
- messy
- duplicated
- poorly split
- leaking future information

The model performs badly.

Common rule:

```text
Garbage In → Garbage Out (GIGO)
```

Bad data → Bad model predictions

---

## 4.1 Data Examples Used Throughout This Section

This section introduces the examples reused throughout this topic.

| Example | Features (Input X) | Label (Output Y) | ML Task | Real Use Case |
| --- | --- | --- | --- | --- |
| House Price Prediction | Size, location, rooms | House price | Regression | Real estate |
| Spam Detection | Email text, links | Spam/Not Spam | Classification | Gmail |
| Medical Diagnosis | Age, symptoms, blood pressure | Disease type | Classification | Hospital |
| Sales Forecasting | Historical sales, season | Future sales | Regression | Retail |

---

# 4.2 Features (Input X)

This section explains the input variables used by machine learning models.

Features are the information given to the model for learning.

---

## 4.2.1 Feature Types

| Feature Type | Definition | Example | Use Case | Notes |
| --- | --- | --- | --- | --- |
| Raw Features | Original collected data | Customer age | Banking | May need cleaning |
| Processed Features | Cleaned/transformed features | Encoded gender | ML training | Better performance |
| Selected Features | Important features only | Salary, credit score | Loan approval | Removes useless data |

---

## 4.2.2 Example A: House Features (Detailed)

```text
1. House listing enters system:
   - Size = 2,000 sqft
   - Location = Kuala Lumpur
   - Bedrooms = 4
   - Age = 5 years

2. Model receives all features

3. Model learns how each feature affects price

4. Future house predictions become possible
```

---

## 4.2.3 Example B: Spam Features (Detailed)

```text
1. Email arrives:
   "Claim your free reward now"

2. Model extracts:
   - Keyword frequency
   - Number of links
   - Sender email
   - Email length

3. These features help detect spam
```

---

# 4.3 Labels (Output Y)

This section explains the correct answers the model learns from.

Labels are required in Supervised Learning.

---

## 4.3.1 Label Types

| Label Type | Definition | Example | ML Type | Notes |
| --- | --- | --- | --- | --- |
| Classification Label | Category output | Spam | Classification | Fixed classes |
| Regression Label | Numerical output | RM500,000 | Regression | Continuous values |
| Ground Truth | Actual correct answer | Real diagnosis | Evaluation | True answer |

---

## 4.3.2 Example A: House Labels (Detailed)

```text
1. House data collected

2. Actual selling price added:
   RM850,000

3. This becomes the label

4. Model learns pricing patterns
```

---

## 4.3.3 Example B: Medical Labels (Detailed)

```text
1. Patient data collected:
   Age = 55
   Symptoms = Fever

2. Doctor diagnosis:
   Flu

3. Flu becomes label
```

---

# 4.4 Dataset

This section explains what a dataset is.

A dataset is a collection of many rows of features + labels.

---

## 4.4.1 Dataset Structure

| Component | Meaning | Example | Notes | Alternative Name |
| --- | --- | --- | --- | --- |
| Row | One record | One customer | One observation | Sample |
| Column | One feature | Age | One variable | Attribute |
| Dataset | Collection of rows | Customer table | Full data | Database |
| Structured Data | Table format | Excel sheet | Most common | Tabular data |
| Unstructured Data | Images/text/video | Photos | Complex | Raw data |

---

## 4.4.2 House Dataset Example

| House Size | Location | Bedrooms | House Age | Price |
| --- | --- | --- | --- | --- |
| 1000 sqft | Kuala Lumpur | 3 | 5 years | RM500,000 |
| 1200 sqft | Selangor | 4 | 3 years | RM650,000 |

---

## 4.4.3 Example A: Dataset Creation (Detailed)

```text
1. Collect 10,000 house records

2. Store:
   - Features
   - Labels

3. Combine into one dataset

4. Use dataset for training
```

---

# 4.5 Training Dataset

This section explains the data used for learning.

This is where the model actually learns.

---

## 4.5.1 Training Dataset Purpose

| Topic | Meaning | Example | Notes | Importance |
| --- | --- | --- | --- | --- |
| Model Learning | Learn patterns | House pricing | Core learning stage | Critical |
| Weight Updates | Adjust parameters | Neural networks | Improves model | Important |
| Largest Portion | Usually biggest split | 80% | Most common | Standard |

---

## 4.5.2 Example A: Training Dataset (Detailed)

```text
Total house records:
10,000

Training set:
8,000 records

Model learns:
Large houses in KL usually cost more
```

---

# 4.6 Validation Dataset

This section explains data used during model improvement.

Validation helps tune the model.

---

## 4.6.1 Validation Purpose

| Topic | Meaning | Example | Notes | Importance |
| --- | --- | --- | --- | --- |
| Hyperparameter Tuning | Adjust settings | Learning rate | Improve model | Important |
| Overfitting Detection | Compare performance | Accuracy drop | Prevent memorization | Critical |

---

## 4.6.2 Example A: Validation Dataset (Detailed)

```text
Validation records:
1,000

Model Version A:
90% accuracy

Model Version B:
94% accuracy

Choose Model B
```

---

# 4.7 Test Dataset

This section explains final evaluation data.

The test set must remain unseen.

---

## 4.7.1 Test Dataset Purpose

| Topic | Meaning | Example | Notes | Importance |
| --- | --- | --- | --- | --- |
| Final Evaluation | Final performance check | Spam model | Real-world simulation | Critical |
| Hidden Data | No training allowed | Exam paper | Prevent cheating | Very important |

---

## 4.7.2 Example A: Test Dataset (Detailed)

```text
Testing records:
1,000 unseen emails

Model predicts:
920 correct

Final accuracy:
92%
```

---

# 4.8 Dataset Splitting

This section explains how datasets are divided.

---

## 4.8.1 Common Split Ratios

| Training | Validation | Testing | Usage | Notes |
| --- | --- | --- | --- | --- |
| 80% | 10% | 10% | Very common | Large datasets |
| 70% | 15% | 15% | Balanced | Common |
| 60% | 20% | 20% | Small datasets | More evaluation |

---

## 4.8.2 Example A: Dataset Splitting (Detailed)

```text
10,000 customer records

Training:
7,000

Validation:
1,500

Testing:
1,500
```

---

## 4.8.3 Step-by-Step Split Process

```text
1. Collect full dataset
2. Shuffle data
3. Split data
4. Train model
5. Validate model
6. Test final model
```

---

# 4.9 Data Leakage

This section explains one of the most dangerous ML mistakes.

Data leakage means the model accidentally sees future/test information.

---

## 4.9.1 Example A: House Leakage (Detailed)

```text
Feature included:
Final selling price after negotiation

Problem:
This reveals future information

Result:
Fake high accuracy
```

---

## 4.9.2 Example B: Student Exam Leakage (Detailed)

```text
Training data accidentally includes test answers

Model scores:
99%

Real-world performance:
Poor
```

---

# 4.10 Feature Quality

This section explains why feature quality matters.

---

## 4.10.1 Feature Quality Table

| Feature Type | Example | Impact | Problem | Result |
| --- | --- | --- | --- | --- |
| Good Feature | Salary | Helpful | None | Better accuracy |
| Bad Feature | Random ID | Useless | Confuses model | Poor accuracy |
| Missing Feature | Credit score missing | Missing info | Weak learning | Lower performance |

---

## 4.10.2 Example A: Bad Feature (Detailed)

```text
Customer ID:
A12345

This ID has no predictive value

Model becomes confused
```

---

# 4.11 Data Types

This section explains common machine learning data formats.

| Data Type | Example | ML Usage | Challenge | Notes |
| --- | --- | --- | --- | --- |
| Numerical | Salary | Regression | Scaling | Common |
| Categorical | Gender | Classification | Encoding | Common |
| Text | Reviews | NLP | Cleaning | Complex |
| Image | X-ray | Computer Vision | Large data | Complex |
| Time Series | Stock prices | Forecasting | Order matters | Special handling |

---

## 4.11.1 Example A: Text Data (Detailed)

```text
Customer review:
"This product is amazing"

Model converts text into usable features
```

---

## 4.11.2 Example B: Image Data (Detailed)

```text
X-ray image uploaded

Model converts pixels into features
```

---

# 4.12 Data Quality Problems

This section explains common data issues.

| Problem | Example | Impact | Solution | Severity |
| --- | --- | --- | --- | --- |
| Missing Values | Missing salary | Poor prediction | Imputation | High |
| Duplicate Records | Same customer twice | Bias | Remove duplicates | Medium |
| Wrong Labels | Spam labeled normal | Wrong learning | Fix labels | High |
| Noise | Typing errors | Lower accuracy | Cleaning | Medium |

---

## 4.12.1 Example A: Missing Values (Detailed)

```text
House record:
Location missing

Model cannot estimate price accurately
```

---

## 4.12.2 Example B: Wrong Labels (Detailed)

```text
Spam email labeled:
Not Spam

Model learns wrong pattern
```

---

# 4.13 Real-World Examples

This section connects data components to real business systems.

| Industry | Features | Label | Goal | Example |
| --- | --- | --- | --- | --- |
| Real Estate | Size, location | Price | Predict price | Property websites |
| Healthcare | Symptoms | Disease | Diagnose illness | Hospital |
| Banking | Salary, debt | Loan approval | Risk prediction | Banks |

---

## 4.13.1 Example A: Hospital Dataset (Detailed)

```text
Patient:
Age = 60
Blood Pressure = High
Symptoms = Chest pain

Label:
Heart disease
```

---

# 4.14 Why Data Components Matter

This section explains why all these components matter.

| Reason | Example | Business Impact | Result | Importance |
| --- | --- | --- | --- | --- |
| Better Features | Better pricing | Higher accuracy | Better model | High |
| Proper Splitting | Fair testing | Reliable model | Honest evaluation | Critical |
| Clean Data | Fewer mistakes | Better decisions | Better predictions | High |
| No Leakage | Prevent cheating | Real performance | Reliable deployment | Critical |

---

## 4.14.1 Example A: Full Bad Data Scenario

```text
Missing features
Wrong labels
Duplicate records
Data leakage

Result:
Model fails in production
```

---

# 4.15 Final Summary

This section summarizes data components.

```text
Features (X)
→ Labels (Y)
→ Dataset
→ Train Split
→ Validation Split
→ Test Split
→ Data Quality
→ Better Model
```

Core lesson:

```text
Good Data → Good Model

Bad Data → Bad Model
```

Next topic:

```text
Training Process
```
