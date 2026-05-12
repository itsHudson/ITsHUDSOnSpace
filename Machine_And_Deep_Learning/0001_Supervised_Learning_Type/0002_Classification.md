# 2. CLASSIFICATION (PREDICT CATEGORIES / LABELS / DECISIONS)

This section explains Classification, which is one of the two major branches of Supervised Learning.

Classification predicts:

```text
Category
Label
Decision
Class
```

Instead of predicting numbers.

---

## Two examples used throughout this section

### Example 1: Email Spam Detection

```text
Input: Email content
Output: Spam / Not Spam
Type: Binary Classification
```

---

### Example 2: Animal Image Classification

```text
Input: Animal image
Output: Cat / Dog / Bird
Type: Multi-Class Classification
```

---

# 2.1 What is Classification?

Classification means predicting which category something belongs to.

---

## Formula

```text
Input (X) → Model → Category Output (Y)
```

```text
f(X) = Y
```

---

## What it predicts

| Input | Output Type | Example |
| --- | --- | --- |
| Email | Category | Spam |
| Medical data | Category | Sick |
| Transaction | Category | Fraud |
| Student scores | Category | Pass/Fail |

---

## Step-by-step

```text
1. Collect historical labeled data
2. Train model using past examples
3. Learn patterns of each category
4. Receive new unseen input
5. Predict correct category
```

---

## Example

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

# 2.2 Why Classification is Important

Classification is used when businesses need fast decisions.

---

| Problem | Manual Method | Classification Solution |
| --- | --- | --- |
| Loan approval | Human review | Approve/Reject automatically |
| Spam filtering | Manual email checking | Automatic spam detection |
| Medical diagnosis | Manual review | Disease prediction |
| Fraud detection | Manual investigation | Fraud alert |

---

## Step-by-step

```text
1. Business has repetitive decisions
2. Historical decision data exists
3. Model learns past decisions
4. New case arrives
5. Model makes faster decisions
```

---

## Example

```text
Bank receives 10,000 loan applications

Instead of manually reviewing all:
Model predicts:

Approve
Reject
```

---

# 2.3 Classification Input Components

This section explains what classification needs before training.

---

## Features (Input Variables)

| Feature | Spam Example | Animal Example |
| --- | --- | --- |
| Words | Free money | N/A |
| Links | Number of links | N/A |
| Image pixels | N/A | Animal image pixels |
| Shape | N/A | Ear shape |

---

## Labels

| Input | Correct Label |
| --- | --- |
| Email | Spam |
| Animal Image | Dog |

---

## Dataset Split

| Dataset Type | Purpose |
| --- | --- |
| Training Set | Learn patterns |
| Validation Set | Tune model |
| Testing Set | Final evaluation |

---

## Step-by-step

```text
1. Collect raw data
2. Create features
3. Add correct labels
4. Split dataset
5. Prepare for training
```

---

## Example

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

# 2.4 Types of Classification

---

## Binary Classification

Only two possible outputs.

```text
Yes / No
Spam / Not Spam
Fraud / Not Fraud
```

### Example

```text
Email → Spam / Not Spam
```

---

## Multi-Class Classification

Many possible classes but only one final output.

```text
Cat
Dog
Bird
```

### Example

```text
Animal image → Dog
```

---

## Multi-Label Classification

One input can have multiple labels.

### Example

```text
Image contains:
Dog + Car + Tree
```

---

## Step-by-step

```text
1. Identify number of possible outputs
2. Choose classification type
3. Train model
4. Predict categories
```

---

# 2.5 How Classification Training Works

This section explains how the model learns.

---

## Training Formula

```text
Input → Prediction → Error → Update → Repeat
```

---

## Step-by-step

```text
1. Input training data enters model
2. Model predicts class
3. Compare prediction with actual label
4. Calculate error
5. Update model
6. Repeat many times
```

---

## Example 1: Spam Classification

```text
Input:
"Claim free prize"

Actual Label:
Spam

Model Prediction:
Not Spam

Result:
Wrong → update model
```

---

## Example 2: Animal Classification

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

# 2.6 Common Classification Algorithms

This section explains common models used for classification.

---

## Logistic Regression

Best for simple classification problems.

Example:

```text
Loan approval
```

---

## Decision Tree

Uses rule splitting.

Example:

```text
Student Pass/Fail
```

---

## Random Forest

Many trees combined.

Example:

```text
Fraud detection
```

---

## SVM

Finds best separation boundary.

Example:

```text
Image classification
```

---

## Naive Bayes

Probability-based.

Example:

```text
Spam detection
```

---

## Neural Networks

Used for complex classification.

Example:

```text
Face recognition
```

---

# 2.7 Classification Output

Models may produce multiple outputs.

---

## Predicted Label

```text
Spam
```

---

## Probability Score

```text
Spam = 95%
Not Spam = 5%
```

---

## Ranking Output

```text
Top product recommendations
```

---

## Step-by-step

```text
1. New input arrives
2. Model calculates probabilities
3. Highest category selected
4. Final output returned
```

---

# 2.8 How We Evaluate Classification Models

This section explains how we measure performance.

---

## Accuracy

How often model is correct.

```text
95 correct out of 100
```

---

## Precision

How many predicted positives are actually correct.

Used in:

```text
Fraud detection
```

---

## Recall

How many actual positives are found.

Used in:

```text
Disease detection
```

---

## F1 Score

Balances precision + recall.

---

## Confusion Matrix

Shows mistakes.

---

# Confusion Matrix Example

| Actual | Predicted |
| --- | --- |
| Spam | Spam → TP |
| Spam | Not Spam → FN |
| Not Spam | Spam → FP |
| Not Spam | Not Spam → TN |

---

## Step-by-step

```text
1. Make predictions
2. Compare actual labels
3. Calculate metrics
4. Identify weaknesses
```

---

# 2.9 Common Problems in Classification

---

## Overfitting

Memorizes training data.

Example:

```text
Spam model only recognizes old spam words
```

---

## Underfitting

Too simple.

Example:

```text
Fails to detect fraud
```

---

## Imbalanced Dataset

One class dominates.

Example:

```text
99 normal transactions
1 fraud transaction
```

---

## Noisy Labels

Wrong labels.

Example:

```text
Spam email labeled as Not Spam
```

---

# 2.10 Real-World Applications

| Industry | Input | Output |
| --- | --- | --- |
| Banking | Customer data | Approve/Reject |
| Healthcare | Symptoms | Disease category |
| Retail | Customer behavior | Buy/Not Buy |
| Security | Face image | Person identity |
| Email | Email content | Spam/Not Spam |

---

## Step-by-step real-world usage

```text
1. Collect historical data
2. Train classification model
3. Deploy system
4. Predict future cases
5. Business uses prediction
```

---

# 2.11 End-to-End Example: Fraud Detection System

This connects everything together.

---

## Step 1: Collect Data

```text
Past transactions
```

---

## Step 2: Add Labels

```text
Fraud / Not Fraud
```

---

## Step 3: Train Model

Learn fraud patterns

---

## Step 4: Evaluate Model

Check accuracy, recall, precision

---

## Step 5: Deploy Model

Real-time fraud monitoring

---

## Step 6: Predict New Transaction

```text
New transaction → Fraud
```

---

# Full Flow

```text
Collect Data
→ Create Features
→ Add Labels
→ Train Model
→ Evaluate Model
→ Improve Model
→ Deploy
→ Predict New Data
```

---

# 2.12 Classification vs Regression

| Classification | Regression |
| --- | --- |
| Predict categories | Predict numbers |
| Spam/Not Spam | House price |
| Fraud/Not Fraud | Temperature prediction |

---

# 2.13 Final Summary

Classification predicts categories, labels, or decisions.

```text
Input → Learn Patterns → Predict Category
```

Examples:

```text
Email → Spam
```

```text
Animal Image → Dog
```

```text
Transaction → Fraud
```

After this topic, the next section naturally connects to:

```text
Regression
```

which predicts continuous numerical values instead of categories.
