# 10. FULL PROCESS: CLASSIFICATION & REGRESSION PIPELINE

This section combines everything into one complete Machine Learning (ML) workflow.

This is one of the most important sections because beginners often learn ML topics separately and fail to understand how everything connects.

Real Machine Learning works as a full pipeline.

Not like this:

```text
Learn algorithm only → Done ❌
```

Real workflow:

```text
Problem
→ Data
→ Training
→ Evaluation
→ Improvement
→ Deployment
→ Monitoring
```

This section answers:

```text
"How does an entire ML project work from start to finish?"
```

---

# 10.1 Pipeline Examples Used Throughout This Section

This section introduces the examples reused throughout this topic.

| Example | ML Type | Input | Output | Real Use Case |
| --- | --- | --- | --- | --- |
| Spam Detection | Classification | Email text | Spam/Not Spam | Gmail |
| Fraud Detection | Classification | Transaction data | Fraud/Not Fraud | Banking |
| House Price Prediction | Regression | House features | House price | Real estate |
| Sales Forecasting | Regression | Historical sales | Future sales | Retail |

---

# PART A: CLASSIFICATION FULL PIPELINE

This section explains how a full classification project works.

---

## 10.2 Step 1: Problem Definition (Classification)

This section defines the business problem.

---

### Example A: Spam Detection (Detailed)

```text
Business problem:
Too many spam emails

Input (X):
Email text
Sender
Links

Output (Y):
Spam / Not Spam

Problem type:
Classification
```

---

### Step-by-Step Flow

```text
Identify problem
→ Identify input
→ Identify output labels
→ Confirm labels are categories
```

---

# 10.3 Step 2: Data Collection (Classification)

This section explains collecting labeled data.

---

### Example A: Spam Dataset (Detailed)

```text
Collect:
100,000 emails

Labels:
Spam
Not Spam

Store dataset
```

---

### Example B: Fraud Dataset

```text
Collect:
Transaction records

Labels:
Fraud
Normal
```

---

# 10.4 Step 3: Data Preprocessing (Classification)

This section explains cleaning data.

---

### Common Tasks

| Task | Why Needed | Example | Result | Risk if Ignored |
| --- | --- | --- | --- | --- |
| Remove missing values | Improve quality | Missing sender | Cleaner data | Poor training |
| Encode categories | Convert text | Country labels | Usable format | Model failure |
| Convert text | NLP preparation | Email text | Features | Bad learning |

---

### Example A: Spam Preprocessing

```text
Raw email:
"WIN FREE MONEY NOW!!!"

Cleaned:
win free money
```

---

# 10.5 Step 4: Feature Engineering (Classification)

This section improves model inputs.

---

### Example A: Spam Features

```text
Original:
Email text

New features:
- Number of links
- Keyword count
- Email length
```

---

# 10.6 Step 5: Dataset Splitting (Classification)

This section creates fair evaluation.

---

### Example

```text
100,000 emails

Training:
70,000

Validation:
15,000

Testing:
15,000
```

---

# 10.7 Step 6: Model Selection (Classification)

This section chooses algorithms.

| Algorithm | Why Use | Example | Strength | Weakness |
| --- | --- | --- | --- | --- |
| Logistic Regression | Simple baseline | Spam | Fast | Limited |
| Random Forest | Better patterns | Fraud | Strong | Slower |
| Neural Network | Complex patterns | Images | Powerful | Expensive |

---

### Example A

```text
Start simple:
Logistic Regression

Need better accuracy:
Try Random Forest
```

---

# 10.8 Step 7: Model Training (Classification)

This section teaches the model.

---

### Training Flow

```text
Input X
→ Predict ŷ
→ Compare with Y
→ Calculate loss
→ Update parameters
→ Repeat
```

---

### Example A

```text
Email:
"Free money"

Prediction:
Not Spam

Actual:
Spam

Model learns from mistake
```

---

# 10.9 Step 8: Evaluation (Classification)

This section measures performance.

| Metric | Meaning | Example | Why Important |
| --- | --- | --- | --- |
| Accuracy | Overall correctness | 92% | General performance |
| Precision | Correct positives | Fraud alerts | Reduce false alarms |
| Recall | Find positives | Disease detection | Reduce missed cases |
| F1 Score | Balance | Spam | Balanced metric |

---

### Example A

```text
1000 emails tested

920 correct

Accuracy:
92%
```

---

# 10.10 Step 9: Improvement (Classification)

This section improves weak models.

---

### Example A

```text
Problem:
Overfitting

Solution:
Regularization
Cross validation
More features
```

---

# 10.11 Step 10: Deployment (Classification)

This section moves model into production.

---

### Example A: Gmail Spam Filter

```text
User receives email

Model predicts spam

Email moved automatically
```

---

# 10.12 Step 11: Monitoring (Classification)

This section keeps model healthy.

---

### Example A

```text
Spam tactics change

Model accuracy drops

Retrain model
```

---

# 10.13 Full Classification Flow

```text
Define Problem
→ Collect Data
→ Clean Data
→ Engineer Features
→ Split Data
→ Select Model
→ Train
→ Evaluate
→ Improve
→ Deploy
→ Monitor
```

---

---

# PART B: REGRESSION FULL PIPELINE

This section explains how a full regression project works.

---

# 10.14 Step 1: Problem Definition (Regression)

This section defines numeric prediction problems.

---

### Example A: House Price Prediction

```text
Input:
House size
Location
Bedrooms

Output:
RM850,000

Problem type:
Regression
```

---

# 10.15 Step 2: Data Collection (Regression)

This section gathers numeric datasets.

---

### Example A

```text
Collect:
50,000 house records

Collect:
Actual selling prices
```

---

# 10.16 Step 3: Data Preprocessing (Regression)

This section cleans regression datasets.

---

### Common Tasks

| Task | Why Needed | Example | Result | Risk |
| --- | --- | --- | --- | --- |
| Missing value handling | Complete dataset | Missing house age | Better model | Poor learning |
| Remove outliers | Prevent distortion | RM50M house | Stable model | Wrong patterns |
| Scaling | Improve training | Large ranges | Better learning | Slow training |

---

### Example A

```text
Remove incorrect prices

Fix missing values

Clean dataset
```

---

# 10.17 Step 4: Feature Engineering (Regression)

This section improves prediction features.

---

### Example A

```text
Original:
House size

New feature:
Price per square foot
```

---

# 10.18 Step 5: Dataset Splitting (Regression)

This section creates train/validation/test sets.

---

### Example A

```text
50,000 houses

Train:
35,000

Validation:
7,500

Test:
7,500
```

---

# 10.19 Step 6: Model Selection (Regression)

This section selects regression algorithms.

| Algorithm | Use Case | Example | Strength | Weakness |
| --- | --- | --- | --- | --- |
| Linear Regression | Simple patterns | Salary | Fast | Limited |
| Random Forest Regressor | Complex patterns | House price | Strong | Slower |
| Gradient Boosting Regressor | Advanced patterns | Sales | High accuracy | Expensive |

---

# 10.20 Step 7: Model Training (Regression)

This section trains regression models.

---

### Example A

```text
House entered

Prediction:
RM780,000

Actual:
RM850,000

Error:
RM70,000

Model updates
```

---

# 10.21 Step 8: Evaluation (Regression)

This section measures regression performance.

| Metric | Meaning | Example | Why Important |
| --- | --- | --- | --- |
| MAE | Average error | RM20,000 | Easy understanding |
| RMSE | Larger error penalty | RM30,000 | Sensitive |
| R² | Pattern explanation | 0.85 | Overall fit |

---

### Example A

```text
Actual:
RM850,000

Predicted:
RM830,000

MAE:
RM20,000
```

---

# 10.22 Step 9: Improvement (Regression)

This section improves weak regression models.

---

### Example A

```text
Problem:
Weak predictions

Solution:
Better features
Regularization
Ensemble methods
```

---

# 10.23 Step 10: Deployment (Regression)

This section puts regression models into production.

---

### Example A: Property Website

```text
User enters house details

Model predicts price

Website shows result
```

---

# 10.24 Step 11: Monitoring (Regression)

This section keeps regression models updated.

---

### Example A

```text
Market prices change

Model becomes outdated

Retrain model
```

---

# 10.25 Full Regression Flow

```text
Define Problem
→ Collect Data
→ Clean Data
→ Engineer Features
→ Split Data
→ Select Model
→ Train
→ Evaluate
→ Improve
→ Deploy
→ Monitor
```

---

# 10.26 Classification vs Regression Pipeline Comparison

This section shows both pipelines side-by-side.

| Stage | Classification | Regression | Same/Different | Example |
| --- | --- | --- | --- | --- |
| Problem Definition | Labels | Numbers | Different output | Spam vs house |
| Data Collection | Labeled classes | Numeric labels | Slightly different | Fraud vs sales |
| Training | Similar process | Similar process | Mostly same | Learn patterns |
| Evaluation | Accuracy/F1 | MAE/RMSE | Different metrics | Different outputs |
| Deployment | Same | Same | Same | Real systems |

---

# 10.27 End-to-End ML Lifecycle

This section connects the entire course.

```text
Supervised Learning
→ Classification / Regression
→ Data Components
→ Training
→ Model Issues
→ Improvement
→ Deployment
→ Monitoring
```

This is how real Machine Learning works in companies.

---

# 10.28 Final Summary

This section summarizes everything.

```text
Machine Learning is a full lifecycle
—not just model training.
```

Core lesson:

```text
Problem
→ Data
→ Model
→ Evaluation
→ Deployment
→ Maintenance
```

You now understand the complete ML pipeline.
