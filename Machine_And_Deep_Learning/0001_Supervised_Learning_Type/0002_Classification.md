# 2. CLASSIFICATION (PREDICT CATEGORIES / LABELS / DECISIONS)

This section explains how Classification works in Supervised Learning.

Classification is used when a model predicts:

- Category
- Label
- Class
- Decision

Instead of predicting continuous numerical values.

---

# 2.1 Classification Examples Used Throughout This Section

This section introduces the detailed examples that will be reused throughout this topic.

| Example | Input | Output | Classification Type | Real Use Case |
| --- | --- | --- | --- | --- |
| Email Spam Detection | Email content | Spam / Not Spam | Binary Classification | Gmail spam filtering |
| Animal Image Classification | Animal image | Cat / Dog / Bird | Multi-Class Classification | Computer vision |
| Fraud Detection | Transaction records | Fraud / Not Fraud | Binary Classification | Banking security |
| Product Tagging | Product image | Shoes + Sports + Men | Multi-Label Classification | E-commerce tagging |

---

# 2.2 What is Classification?

This section explains the basic meaning of classification.

Classification predicts which category an input belongs to.

---

## 2.2.1 Core Formula

```text
Input (X) → Model → Category Output (Y)
```

```text
f(X) = Y
```

---

## 2.2.2 Step-by-Step Classification Process

```text
1. Collect historical labeled data
2. Train classification model
3. Learn category patterns
4. Receive new unseen input
5. Predict final category
```

---

## 2.2.3 Example A: Email Spam Detection (Detailed)

```text
1. New email arrives:
   "Congratulations! Claim your free iPhone now"

2. Model extracts features:
   - Contains spam keywords: "free", "claim"
   - Unknown sender email
   - Contains suspicious link
   - Many capital letters

3. Model compares these features with historical spam emails

4. Model calculates probability:
   Spam = 96%
   Not Spam = 4%

5. Final Prediction:
   Spam

6. Email moves to spam folder
```

---

## 2.2.4 Example B: Animal Classification (Detailed)

```text
1. User uploads animal image

2. Model extracts features:
   - Ear shape
   - Fur texture
   - Body size
   - Tail shape

3. Model compares image with training images

4. Model calculates probability:
   Cat = 88%
   Dog = 10%
   Bird = 2%

5. Final Prediction:
   Cat
```

---

# 2.3 Why Classification is Important

This section explains why businesses use classification.

| Problem | Manual Method | Classification Solution | Business Benefit | Example |
| --- | --- | --- | --- | --- |
| Loan approval | Human review | Approve/Reject | Faster decisions | Banking |
| Fraud detection | Manual investigation | Fraud prediction | Reduce losses | Credit cards |
| Medical diagnosis | Manual diagnosis | Disease classification | Faster treatment | Hospitals |

---

## 2.3.1 Example A: Loan Approval (Detailed)

```text
1. Customer applies for loan

2. Input data:
   - Salary = RM6,000
   - Credit score = High
   - Existing debt = Low

3. Model checks historical loan approvals

4. Model predicts:
   Approve

5. Bank processes application faster
```

---

## 2.3.2 Example B: Disease Diagnosis (Detailed)

```text
1. Patient enters symptoms

2. Input data:
   - Fever
   - Cough
   - Fatigue

3. Model compares symptoms with medical records

4. Model predicts:
   Flu

5. Doctor receives faster diagnosis support
```

---

# 2.4 Classification Input Components

This section explains required data before training begins.

---

## 2.4.1 Features

| Feature Type | Email Example | Fraud Example | Animal Example | Why Important |
| --- | --- | --- | --- | --- |
| Keywords | Free money | N/A | N/A | Text pattern detection |
| Transaction amount | N/A | RM5000 | N/A | Fraud detection |
| Image pixels | N/A | N/A | Animal image | Image recognition |
| Location | N/A | Overseas transaction | N/A | Detect suspicious activity |

---

## 2.4.2 Example A: Fraud Features (Detailed)

```text
1. Transaction occurs:
   RM8,000 purchase

2. Model extracts:
   - Transaction amount
   - Location
   - Purchase time
   - Merchant type

3. Model notices:
   - Unusual country
   - Late night transaction

4. Features sent for prediction
```

---

## 2.4.3 Labels

This section explains correct answers used during training.

| Input | Correct Label | Purpose | Example | Notes |
| --- | --- | --- | --- | --- |
| Email | Spam | Teach model | Spam filtering | Required |
| Transaction | Fraud | Teach model | Banking | Required |

---

## 2.4.4 Example A: Label Creation (Detailed)

```text
Transaction History:

Transaction 1 → Fraud
Transaction 2 → Not Fraud
Transaction 3 → Fraud

These labels teach the model correct answers
```

---

## 2.4.5 Dataset Splitting

| Dataset Type | Purpose | Percentage | Example | Notes |
| --- | --- | --- | --- | --- |
| Training Dataset | Teach model | 70–80% | Historical records | Largest portion |
| Validation Dataset | Tune model | 10–15% | Improve model | Optional |
| Testing Dataset | Final evaluation | 10–20% | Unseen data | Must remain unseen |

---

## 2.4.6 Example A: Dataset Split (Detailed)

```text
10,000 emails collected

Training:
8,000 emails

Validation:
1,000 emails

Testing:
1,000 emails
```

---

# 2.5 Types of Classification

This section explains different classification problem types.

| Type | Outputs | Example | Real Use Case | Rule |
| --- | --- | --- | --- | --- |
| Binary Classification | 2 | Spam/Not Spam | Fraud detection | Two outputs only |
| Multi-Class Classification | More than 2 | Cat/Dog/Bird | Image recognition | One final output |
| Multi-Label Classification | Multiple | Shoes + Sports + Men | E-commerce | Multiple outputs |

---

## 2.5.1 Example A: Binary Classification (Detailed)

```text
1. Email arrives

2. Model checks features

3. Two possible outputs:
   Spam
   Not Spam

4. Model selects:
   Spam
```

---

## 2.5.2 Example B: Multi-Class Classification (Detailed)

```text
1. Animal image uploaded

2. Model compares image

3. Possible outputs:
   Cat
   Dog
   Bird

4. Final prediction:
   Dog
```

---

## 2.5.3 Example C: Multi-Label Classification (Detailed)

```text
1. Product image uploaded

2. Model detects:
   Shoes
   Sportswear
   Men's fashion

3. Multiple labels assigned
```

---

# 2.6 How Classification Training Works

This section explains how the model learns.

---

## 2.6.1 Training Formula

```text
Input → Prediction → Error → Update → Repeat
```

---

## 2.6.2 Step-by-Step Training Process

```text
1. Input enters model
2. Model predicts class
3. Compare with actual label
4. Calculate error
5. Update model
6. Repeat many times
```

---

## 2.6.3 Example A: Spam Training (Detailed)

```text
1. Training email:
   "Claim free reward"

2. Actual label:
   Spam

3. Model prediction:
   Not Spam

4. Model is wrong

5. Model adjusts weights

6. Future prediction improves
```

---

## 2.6.4 Example B: Fraud Training (Detailed)

```text
1. Transaction:
   RM9,000 overseas purchase

2. Actual label:
   Fraud

3. Model predicts:
   Normal

4. Error detected

5. Model updates fraud patterns
```

---

# 2.7 Common Classification Algorithms

This section explains common algorithms.

| Algorithm | Full Form | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Logistic Regression (LR) | Logistic Regression | Uses probability | Loan approval | Weak with complex data |
| Decision Tree (DT) | Decision Tree | Rule splitting | Student grading | Overfitting |
| Random Forest (RF) | Random Forest | Multiple trees | Fraud detection | Slower |
| Support Vector Machine (SVM) | Support Vector Machine | Finds boundaries | Image classification | Hard for huge datasets |

---

## 2.7.1 Example A: Decision Tree (Detailed)

```text
1. Student marks entered

2. Rule:
   Marks > 50 → Pass

3. Student score = 80

4. Prediction:
   Pass
```

---

## 2.7.2 Example B: Random Forest (Detailed)

```text
1. Transaction entered

2. Multiple trees analyze fraud risk

3. Most trees vote:
   Fraud

4. Final prediction:
   Fraud
```

---

# 2.8 Classification Output Types

This section explains output forms.

| Output Type | Definition | Example | Business Use | Notes |
| --- | --- | --- | --- | --- |
| Predicted Label | Final category | Spam | Email filtering | Most common |
| Probability Score | Confidence score | Fraud = 92% | Risk analysis | Common |
| Ranking Output | Ranked output | Product ranking | Recommendation | Less common |

---

## 2.8.1 Example A: Probability Score (Detailed)

```text
Transaction Analysis:

Fraud = 92%
Normal = 8%

Final Output:
Fraud
```

---

# 2.9 Evaluation Metrics

This section explains how performance is measured.

| Metric | Measures | Example Use Case | Best Use |
| --- | --- | --- | --- |
| Accuracy | Overall correctness | Spam filtering | Balanced data |
| Precision | Correct positive predictions | Fraud detection | False alarms costly |
| Recall | Finds actual positives | Healthcare | Missing cases dangerous |
| F1 Score | Balance precision/recall | Imbalanced data | Balanced evaluation |

---

## 2.9.1 Example A: Accuracy (Detailed)

```text
100 emails tested

90 predicted correctly
10 predicted wrongly

Accuracy = 90%
```

---

## 2.9.2 Example B: Recall (Detailed)

```text
100 cancer patients

Model correctly finds:
95 patients

Recall = 95%
```

---

# 2.10 Common Problems in Classification

This section explains common issues.

| Problem | Cause | Example | Impact | Solution |
| --- | --- | --- | --- | --- |
| Overfitting | Too complex | Memorizes spam keywords | Poor new predictions | Regularization |
| Underfitting | Too simple | Poor fraud detection | Low accuracy | Better model |
| Imbalanced Dataset | Unequal classes | Few fraud cases | Bias | Resampling |

---

## 2.10.1 Example A: Overfitting (Detailed)

```text
Training:
Model memorizes old spam keywords

New email:
Uses different wording

Result:
Wrong prediction
```

---

# 2.11 Real-World Applications

This section shows real usage.

| Industry | Input | Output | Example | Value |
| --- | --- | --- | --- | --- |
| Banking | Credit data | Approve/Reject | Loans | Faster approval |
| Healthcare | Symptoms | Disease | Diagnosis | Faster treatment |
| Security | Face image | Identity | Face unlock | Security |

---

## 2.11.1 Example A: Face Unlock (Detailed)

```text
1. User scans face

2. Model compares with saved face data

3. Match found

4. Output:
   Phone unlocks
```

---

# 2.12 End-to-End Example: Fraud Detection System

This section connects everything.

| Step | Input | Process | Output | Purpose |
| --- | --- | --- | --- | --- |
| 1 | Transactions | Collect data | Dataset | Prepare training |
| 2 | Labels | Add labels | Labeled data | Teach model |
| 3 | Training | Learn patterns | Model | Build classifier |
| 4 | Testing | Evaluate | Metrics | Check performance |
| 5 | New transaction | Predict | Fraud | Real usage |

---

## 2.12.1 Full Pipeline

```text
Collect Data
→ Create Features
→ Add Labels
→ Train Model
→ Evaluate Model
→ Improve Model
→ Deploy Model
→ Predict New Data
```

---

# 2.13 Classification vs Regression

This section explains the difference.

| Classification | Regression | Example | Output |
| --- | --- | --- | --- |
| Predict categories | Predict numbers | Spam vs House price | Category vs Number |

---

## 2.13.1 Example A: Classification

```text
Email → Spam
```

---

## 2.13.2 Example B: Regression

```text
House → RM500,000
```

---

# 2.14 Final Summary

This section summarizes classification.

```text
Input → Learn Patterns → Predict Category
```

Examples:

```text
Email → Spam
Animal → Dog
Transaction → Fraud
Product → Multiple Labels
```

Next topic:

```text
Regression
```
