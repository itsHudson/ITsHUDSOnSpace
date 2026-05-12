# 2. CLASSIFICATION (PREDICT CATEGORIES / LABELS / DECISIONS)

This section explains how Classification works in Supervised Learning.

Classification is used when a model needs to predict:

- Category
- Label
- Class
- Decision

Instead of predicting continuous numerical values.

---

## 2.1 Classification Examples Used Throughout This Section

This section introduces the examples used throughout this topic so beginners can connect every concept to real-world scenarios.

| Example | Input | Output | Classification Type | Real Use Case |
| --- | --- | --- | --- | --- |
| Email Spam Detection | Email content | Spam / Not Spam | Binary Classification | Gmail spam filtering |
| Animal Image Classification | Animal image | Cat / Dog / Bird | Multi-Class Classification | Image recognition |
| Product Tagging | Product image | Shoes + Sports + Men | Multi-Label Classification | E-commerce tagging |

---

# 2.2 What is Classification?

This section explains the basic meaning of classification.

Classification predicts which category an input belongs to.

---

## 2.2.1 Core Formula

This section explains the basic classification formula.

```text
Input (X) → Model → Category Output (Y)
```

```text
f(X) = Y
```

---

## 2.2.2 What Classification Predicts

This section shows common classification outputs.

| Input | Predicted Output | Classification Type | Industry Example | Purpose |
| --- | --- | --- | --- | --- |
| Email | Spam | Binary | Email | Filter unwanted emails |
| Transaction | Fraud | Binary | Banking | Prevent fraud |
| Medical data | Disease category | Multi-Class | Healthcare | Diagnose patients |
| Student scores | Pass/Fail | Binary | Education | Academic decisions |
| Image | Cat/Dog/Bird | Multi-Class | Computer Vision | Object recognition |

---

## 2.2.3 Step-by-Step Classification Process

This section explains the overall classification workflow.

```text
1. Collect labeled historical data
2. Train classification model
3. Learn category patterns
4. Receive new unseen input
5. Predict category
```

---

## 2.2.4 Example

### Email Example

```text
Input:
"Win free money now"

Prediction:
Spam
```

---

### Animal Example

```text
Input:
Animal image

Prediction:
Dog
```

---

# 2.3 Why Classification is Important

This section explains why classification is widely used.

| Problem | Traditional Method | Classification Solution | Business Benefit | Example |
| --- | --- | --- | --- | --- |
| Loan approval | Manual review | Approve/Reject prediction | Faster decisions | Banking |
| Fraud detection | Human investigation | Fraud prediction | Reduce losses | Credit cards |
| Medical diagnosis | Manual diagnosis | Disease classification | Faster treatment | Hospitals |
| Spam filtering | Manual email checking | Spam prediction | Cleaner inbox | Gmail |
| Product recommendation | Manual tagging | Category prediction | Better marketing | E-commerce |

---

## 2.3.1 Step-by-Step Business Flow

```text
1. Business has repetitive decisions
2. Historical labeled data exists
3. Model learns from past decisions
4. New case arrives
5. Model predicts faster
```

---

# 2.4 Classification Input Components

This section explains the required components before training begins.

---

## 2.4.1 Features

This section explains input variables.

| Feature Type | Email Example | Animal Example | Why Important | Notes |
| --- | --- | --- | --- | --- |
| Keywords | Free money | N/A | Detect spam signals | Text classification |
| Links | Number of links | N/A | Identify suspicious emails | Useful in spam filtering |
| Image Pixels | N/A | Raw image data | Detect visual patterns | Computer vision |
| Shape Features | N/A | Ear shape | Improve recognition | Image classification |

---

## 2.4.2 Labels

This section explains correct answers.

| Input | Correct Label | Purpose | Example | Notes |
| --- | --- | --- | --- | --- |
| Email | Spam | Teach model | Spam detection | Required |
| Animal image | Dog | Teach model | Image recognition | Required |

---

## 2.4.3 Dataset Splitting

This section explains dataset division.

| Dataset Type | Purpose | Typical Percentage | Example | Notes |
| --- | --- | --- | --- | --- |
| Training Dataset | Teach model | 70–80% | Historical emails | Largest portion |
| Validation Dataset | Tune model | 10–15% | Adjust settings | Optional but common |
| Testing Dataset | Final evaluation | 10–20% | New emails | Must be unseen |

---

## 2.4.4 Step-by-Step Data Preparation

```text
1. Collect raw data
2. Extract features
3. Add labels
4. Split dataset
5. Prepare training data
```

---

# 2.5 Types of Classification

This section explains different classification problem types.

| Type | Number of Outputs | Example | Real Use Case | Important Rule |
| --- | --- | --- | --- | --- |
| Binary Classification | 2 | Spam / Not Spam | Fraud detection | Only two outputs |
| Multi-Class Classification | More than 2 | Cat/Dog/Bird | Image recognition | Only one final output |
| Multi-Label Classification | Multiple outputs | Dog + Tree + Car | Product tagging | Multiple labels allowed |

---

## 2.5.1 Step-by-Step Type Selection

```text
1. Check number of outputs
2. Determine if multiple labels are possible
3. Select correct classification type
4. Train model
```

---

# 2.6 How Classification Training Works

This section explains how models learn.

---

## 2.6.1 Training Formula

```text
Input → Prediction → Error → Update → Repeat
```

---

## 2.6.2 Step-by-Step Training Process

```text
1. Input training data enters model
2. Model predicts category
3. Compare prediction with actual label
4. Calculate error
5. Update model parameters
6. Repeat many times
```

---

## 2.6.3 Example

| Step | Email Spam Example | Animal Example | Result | Purpose |
| --- | --- | --- | --- | --- |
| Input | "Claim free prize" | Dog image | Raw input | Start prediction |
| Actual Label | Spam | Dog | Correct answer | Compare result |
| Prediction | Not Spam | Cat | Wrong prediction | Find error |
| Update | Adjust model | Adjust model | Improve future prediction | Learning process |

---

# 2.7 Common Classification Algorithms

This section explains common algorithms.

| Algorithm | Full Form | How It Works | Example | Limitation |
| --- | --- | --- | --- | --- |
| Logistic Regression (LR) | Logistic Regression | Uses probability | Loan approval | Weak for complex patterns |
| Decision Tree (DT) | Decision Tree | Rule splitting | Student pass/fail | Can overfit |
| Random Forest (RF) | Random Forest | Multiple trees combined | Fraud detection | Slower |
| Support Vector Machine (SVM) | Support Vector Machine | Finds best boundary | Image classification | Hard with huge data |
| K-Nearest Neighbors (KNN) | K-Nearest Neighbors | Finds similar neighbors | Fruit classification | Slow |
| Naive Bayes (NB) | Naive Bayes | Probability-based | Spam detection | Assumes independence |
| Neural Network (NN) | Neural Network | Layer-based learning | Face recognition | Needs large data |

---

# 2.8 Classification Output Types

This section explains possible outputs.

| Output Type | Definition | Example | Why Useful | Notes |
| --- | --- | --- | --- | --- |
| Predicted Label | Final category | Spam | Easy decisions | Most common |
| Probability Score | Confidence score | Spam = 95% | Risk analysis | Common in finance |
| Ranking Output | Ranked outputs | Product recommendations | Better recommendations | Less common |

---

## 2.8.1 Step-by-Step Prediction Flow

```text
1. New input arrives
2. Model calculates probabilities
3. Select highest category
4. Return final output
```

---

# 2.9 Evaluation Metrics

This section explains how classification performance is measured.

| Metric | Full Form | What It Measures | Example | Best Use Case |
| --- | --- | --- | --- | --- |
| Accuracy | Accuracy | Overall correctness | 95/100 correct | Balanced datasets |
| Precision | Precision | Correct positive predictions | Fraud alerts | False positives costly |
| Recall | Recall | Finds actual positives | Disease detection | Missing cases dangerous |
| F1 Score | F1 Score | Balance precision + recall | Fraud detection | Imbalanced datasets |
| Confusion Matrix | Confusion Matrix | Detailed error breakdown | TP/TN/FP/FN | Error analysis |

---

## 2.9.1 Confusion Matrix Terms

| Term | Full Form | Meaning | Example | Notes |
| --- | --- | --- | --- | --- |
| TP | True Positive | Correct positive prediction | Fraud predicted as fraud | Good |
| TN | True Negative | Correct negative prediction | Normal predicted normal | Good |
| FP | False Positive | Wrong positive prediction | Normal predicted fraud | False alarm |
| FN | False Negative | Wrong negative prediction | Fraud predicted normal | Dangerous |

---

# 2.10 Common Problems in Classification

This section explains common model problems.

| Problem | Definition | Cause | Example | Solution |
| --- | --- | --- | --- | --- |
| Overfitting | Memorizes training data | Model too complex | High train accuracy only | Regularization |
| Underfitting | Model too simple | Weak learning | Poor predictions | Better model |
| Imbalanced Dataset | One class dominates | Unequal data | 99 normal, 1 fraud | Resampling |
| Noisy Data | Poor quality data | Wrong labels | Incorrect labels | Data cleaning |

---

# 2.11 Real-World Applications

This section shows practical applications.

| Industry | Input | Output | Example | Business Value |
| --- | --- | --- | --- | --- |
| Banking | Credit score | Approve/Reject | Loan approval | Faster decisions |
| Healthcare | Symptoms | Disease category | Diagnosis | Faster treatment |
| Retail | Customer behavior | Buy/Not Buy | Marketing | Better targeting |
| Security | Face image | Person identity | Face unlock | Security |
| Email | Email text | Spam/Not Spam | Gmail | Cleaner inbox |

---

# 2.12 End-to-End Example: Fraud Detection System

This section connects everything together.

| Step | Input | Process | Output | Purpose |
| --- | --- | --- | --- | --- |
| 1 | Transaction history | Collect data | Dataset | Prepare training |
| 2 | Fraud labels | Add labels | Labeled dataset | Teach model |
| 3 | Training data | Train model | Trained classifier | Learn fraud patterns |
| 4 | Testing data | Evaluate model | Performance metrics | Check quality |
| 5 | New transaction | Predict fraud | Fraud / Not Fraud | Real-time usage |

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

This section explains the difference between classification and regression.

| Classification | Regression | Similarity | Example | Output Type |
| --- | --- | --- | --- | --- |
| Predict categories | Predict numbers | Both are supervised learning | Spam vs House price | Category vs Number |

---

# 2.14 Final Summary

This section summarizes classification.

```text
Input → Learn Patterns → Predict Category
```

Examples:

```text
Email → Spam
Animal Image → Dog
Transaction → Fraud
```

Next topic:

```text
Regression
```
