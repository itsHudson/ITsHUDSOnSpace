# 2. CLASSIFICATION (PREDICT CATEGORIES / LABELS / DECISIONS)

This section explains Classification, one of the two major branches of Supervised Learning.

Classification predicts:

- Categories
- Labels
- Decisions
- Classes

Instead of predicting numerical values.

---

## 2.1 Classification Examples Used Throughout This Section

To make learning easier, we will repeatedly use two examples:

### 2.1.1 Example A: Email Spam Detection

```text
Input: Email content
Output: Spam / Not Spam
Type: Binary Classification
```

---

### 2.1.2 Example B: Animal Image Classification

```text
Input: Animal image
Output: Cat / Dog / Bird
Type: Multi-Class Classification
```

---

# 2.2 What is Classification?

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

## 2.2.2 What Classification Predicts

| Input | Output |
| --- | --- |
| Email | Spam |
| Transaction | Fraud |
| Medical data | Sick |
| Student scores | Pass/Fail |

---

## 2.2.3 Step-by-Step Classification Process

```text
1. Collect labeled historical data
2. Train model using past examples
3. Learn category patterns
4. Receive new input
5. Predict correct category
```

---

## 2.2.4 Example

### Spam Example

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
Cat
```

---

# 2.3 Why Classification is Important

Classification helps automate repetitive decision-making.

---

## 2.3.1 Business Problems Solved

| Problem | Manual Method | Classification Solution |
| --- | --- | --- |
| Loan approval | Human review | Approve/Reject |
| Spam filtering | Manual checking | Spam detection |
| Fraud detection | Manual investigation | Fraud alert |
| Disease diagnosis | Doctor review | Disease prediction |

---

## 2.3.2 Step-by-Step Business Flow

```text
1. Business has repetitive decisions
2. Historical decision data exists
3. Model learns past decisions
4. New case arrives
5. Model predicts outcome
```

---

## 2.3.3 Example

```text
10,000 loan applications arrive

Instead of manually reviewing all:
Model predicts:

Approve
Reject
```

---

# 2.4 Classification Input Components

This section explains what classification needs before training begins.

---

## 2.4.1 Features

| Feature | Spam Example | Animal Example |
| --- | --- | --- |
| Keywords | Free money | N/A |
| Links | Number of links | N/A |
| Image pixels | N/A | Animal image |
| Shape | N/A | Ear shape |

---

## 2.4.2 Labels

| Input | Label |
| --- | --- |
| Email | Spam |
| Animal image | Dog |

---

## 2.4.3 Dataset Splitting

| Dataset Type | Purpose |
| --- | --- |
| Training Set | Learn patterns |
| Validation Set | Tune model |
| Test Set | Final evaluation |

---

## 2.4.4 Step-by-Step Data Preparation

```text
1. Collect raw data
2. Create features
3. Add labels
4. Split dataset
5. Prepare training data
```

---

## 2.4.5 Example

### Spam Dataset

```text
"Free money" → Spam
"Meeting tomorrow" → Not Spam
```

---

### Animal Dataset

```text
Cat image → Cat
Dog image → Dog
Bird image → Bird
```

---

# 2.5 Types of Classification

---

## 2.5.1 Binary Classification

Only two possible outputs.

```text
Yes / No
Spam / Not Spam
Fraud / Not Fraud
```

Example:

```text
Email → Spam / Not Spam
```

---

## 2.5.2 Multi-Class Classification

Many classes but only one final output.

```text
Cat
Dog
Bird
```

Example:

```text
Animal image → Dog
```

---

## 2.5.3 Multi-Label Classification

One input can have multiple labels.

Example:

```text
Image → Dog + Tree + Car
```

---

## 2.5.4 Step-by-Step Type Selection

```text
1. Identify number of outputs
2. Determine if outputs are single or multiple
3. Select correct classification type
4. Train model
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
1. Input training data enters model
2. Model predicts category
3. Compare prediction with actual label
4. Calculate error
5. Update model
6. Repeat many times
```

---

## 2.6.3 Spam Example

```text
Input:
"Claim free prize"

Actual Label:
Spam

Prediction:
Not Spam

Result:
Wrong → update model
```

---

## 2.6.4 Animal Example

```text
Input:
Dog image

Actual Label:
Dog

Prediction:
Cat

Result:
Wrong → update model
```

---

# 2.7 Common Classification Algorithms

This section explains commonly used algorithms.

---

## 2.7.1 Logistic Regression

Used for simple classification.

Example:

```text
Loan approval
```

---

## 2.7.2 Decision Tree

Uses rule splitting.

Example:

```text
Student pass/fail
```

---

## 2.7.3 Random Forest

Combines multiple trees.

Example:

```text
Fraud detection
```

---

## 2.7.4 SVM

Finds best decision boundary.

Example:

```text
Image classification
```

---

## 2.7.5 Naive Bayes

Probability-based classification.

Example:

```text
Spam detection
```

---

## 2.7.6 Neural Networks

Used for complex tasks.

Example:

```text
Face recognition
```

---

# 2.8 Classification Output Types

---

## 2.8.1 Predicted Label

```text
Spam
```

---

## 2.8.2 Probability Score

```text
Spam = 95%
Not Spam = 5%
```

---

## 2.8.3 Ranking Output

```text
Top product recommendations
```

---

## 2.8.4 Step-by-Step Prediction Flow

```text
1. New input arrives
2. Model calculates probabilities
3. Highest category selected
4. Final prediction returned
```

---

# 2.9 Evaluation Metrics

This section explains how classification performance is measured.

---

## 2.9.1 Accuracy

Measures overall correctness.

```text
95 correct out of 100
```

---

## 2.9.2 Precision

Measures how many predicted positives are actually correct.

Example:

```text
Fraud detection
```

---

## 2.9.3 Recall

Measures how many actual positives are found.

Example:

```text
Disease detection
```

---

## 2.9.4 F1 Score

Balances precision and recall.

---

## 2.9.5 Confusion Matrix

Shows detailed prediction mistakes.

---

## 2.9.6 Confusion Matrix Example

| Actual | Predicted |
| --- | --- |
| Spam | Spam → TP |
| Spam | Not Spam → FN |
| Not Spam | Spam → FP |
| Not Spam | Not Spam → TN |

---

## 2.9.7 Step-by-Step Evaluation Flow

```text
1. Make predictions
2. Compare actual labels
3. Calculate metrics
4. Identify weaknesses
```

---

# 2.10 Common Problems in Classification

---

## 2.10.1 Overfitting

Model memorizes training data.

Example:

```text
Only detects old spam patterns
```

---

## 2.10.2 Underfitting

Model is too simple.

Example:

```text
Fails to detect fraud
```

---

## 2.10.3 Imbalanced Dataset

One class dominates.

Example:

```text
99 normal transactions
1 fraud transaction
```

---

## 2.10.4 Noisy Labels

Wrong labels exist.

Example:

```text
Spam email labeled as normal
```

---

## 2.10.5 Step-by-Step Problem Solving

```text
1. Train model
2. Test model
3. Identify issue
4. Improve data/model
5. Retrain
```

---

# 2.11 Real-World Applications

| Industry | Input | Output |
| --- | --- | --- |
| Banking | Customer data | Approve/Reject |
| Healthcare | Symptoms | Disease prediction |
| Retail | Customer behavior | Buy/Not Buy |
| Security | Face image | Person identity |
| Email | Email text | Spam/Not Spam |

---

## 2.11.1 Real-World Workflow

```text
1. Collect business data
2. Train model
3. Deploy model
4. Predict future cases
```

---

# 2.12 End-to-End Example: Fraud Detection System

This section connects everything together.

---

## 2.12.1 Step 1: Collect Data

```text
Past transaction records
```

---

## 2.12.2 Step 2: Add Labels

```text
Fraud / Not Fraud
```

---

## 2.12.3 Step 3: Train Model

Learn fraud patterns

---

## 2.12.4 Step 4: Evaluate Model

Check metrics

---

## 2.12.5 Step 5: Deploy Model

Real-time fraud detection

---

## 2.12.6 Step 6: Predict New Transaction

```text
New transaction → Fraud
```

---

## 2.12.7 Full Pipeline

```text
Collect Data
→ Create Features
→ Add Labels
→ Train Model
→ Evaluate
→ Improve
→ Deploy
→ Predict
```

---

# 2.13 Classification vs Regression

| Classification | Regression |
| --- | --- |
| Predict categories | Predict numbers |
| Spam detection | House price prediction |
| Fraud detection | Temperature prediction |

---

# 2.14 Final Summary

Classification predicts categories, labels, or decisions.

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
