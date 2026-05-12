# 2. CLASSIFICATION (PREDICT CATEGORIES / LABELS / DECISIONS)

This section explains how Classification works in Supervised Learning. Classification is used when the model needs to predict a fixed category, label, class, or decision instead of a continuous number.

Classification predicts:

```text
Category
Label
Decision
Class
```

---

## 2.1 Classification Examples Used Throughout This Section

This section introduces the main examples that will be reused throughout the classification topic so beginners can connect every concept to real situations.

### 2.1.1 Example A: Email Spam Detection

This example shows binary classification because the model only chooses between two possible categories.

```text
Input: Email content
Output: Spam / Not Spam
Type: Binary Classification
```

---

### 2.1.2 Example B: Animal Image Classification

This example shows multi-class classification because the model chooses one category from more than two possible classes.

```text
Input: Animal image
Output: Cat / Dog / Bird
Type: Multi-Class Classification
```

---

# 2.2 What is Classification?

This section explains the basic meaning of classification and how it connects input data to category-based output.

## 2.2.1 Core Formula

This section shows the basic formula behind classification.

```text
Input (X) → Model → Category Output (Y)
```

```text
f(X) = Y
```

---

## 2.2.2 What Classification Predicts

This section shows examples of category-based outputs.

| Input | Output |
| --- | --- |
| Email | Spam |
| Transaction | Fraud |
| Medical data | Sick |
| Student scores | Pass/Fail |

---

## 2.2.3 Step-by-Step Classification Process

This section explains the general flow of how classification works.

```text
1. Collect labeled historical data
2. Train model using past examples
3. Learn category patterns
4. Receive new input
5. Predict correct category
```

---

## 2.2.4 Example

This section shows simple classification predictions.

### Spam Example

```text
Input:
"Win free money now"

Prediction:
Spam
```

### Animal Example

```text
Input:
Animal image

Prediction:
Cat
```

---

# 2.3 Why Classification is Important

This section explains why classification is useful for real-world decision-making problems.

## 2.3.1 Business Problems Solved

This section shows problems that classification can automate.

| Problem | Manual Method | Classification Solution |
| --- | --- | --- |
| Loan approval | Human review | Approve/Reject |
| Spam filtering | Manual checking | Spam detection |
| Fraud detection | Manual investigation | Fraud alert |
| Disease diagnosis | Doctor review | Disease prediction |

---

## 2.3.2 Step-by-Step Business Flow

This section explains how classification is used in business systems.

```text
1. Business has repetitive decisions
2. Historical decision data exists
3. Model learns past decisions
4. New case arrives
5. Model predicts outcome
```

---

## 2.3.3 Example

This section shows how classification reduces manual work.

```text
10,000 loan applications arrive

Instead of manually reviewing all:
Model predicts:

Approve
Reject
```

---

# 2.4 Classification Input Components

This section explains the data components needed before a classification model can be trained.

## 2.4.1 Features

This section explains the input variables used by a classification model.

| Feature | Spam Example | Animal Example |
| --- | --- | --- |
| Keywords | Free money | N/A |
| Links | Number of links | N/A |
| Image pixels | N/A | Animal image |
| Shape | N/A | Ear shape |

---

## 2.4.2 Labels

This section explains the correct category answers used during training.

| Input | Label |
| --- | --- |
| Email | Spam |
| Animal image | Dog |

---

## 2.4.3 Dataset Splitting

This section explains how data is divided for learning and evaluation.

| Dataset Type | Purpose |
| --- | --- |
| Training Set | Learn patterns |
| Validation Set | Tune model |
| Test Set | Final evaluation |

---

## 2.4.4 Step-by-Step Data Preparation

This section explains how raw data becomes usable training data.

```text
1. Collect raw data
2. Create features
3. Add labels
4. Split dataset
5. Prepare training data
```

---

## 2.4.5 Example

This section shows how labeled classification datasets look.

### Spam Dataset

```text
"Free money" → Spam
"Meeting tomorrow" → Not Spam
```

### Animal Dataset

```text
Cat image → Cat
Dog image → Dog
Bird image → Bird
```

---

# 2.5 Types of Classification

This section explains the main types of classification based on how many outputs the model can predict.

## 2.5.1 Binary Classification

This section explains classification problems with only two possible outputs.

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

This section explains classification problems with more than two possible outputs, where only one final class is selected.

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

This section explains classification problems where one input can have multiple correct labels.

Example:

```text
Image → Dog + Tree + Car
```

---

## 2.5.4 Step-by-Step Type Selection

This section explains how to choose the correct classification type.

```text
1. Identify number of outputs
2. Determine if outputs are single or multiple
3. Select correct classification type
4. Train model
```

---

# 2.6 How Classification Training Works

This section explains how a classification model learns patterns from labeled examples.

## 2.6.1 Training Formula

This section shows the basic training cycle.

```text
Input → Prediction → Error → Update → Repeat
```

---

## 2.6.2 Step-by-Step Training Process

This section explains how the model learns from mistakes.

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

This section shows how a spam classifier learns from a wrong prediction.

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

This section shows how an image classifier learns from a wrong prediction.

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

This section introduces common algorithms used to build classification models.

## 2.7.1 Logistic Regression

This section explains a simple classification algorithm often used for binary decisions.

Used for simple classification.

Example:

```text
Loan approval
```

---

## 2.7.2 Decision Tree

This section explains a rule-based classification algorithm that splits data using decision rules.

Uses rule splitting.

Example:

```text
Student pass/fail
```

---

## 2.7.3 Random Forest

This section explains an algorithm that combines many decision trees to improve prediction reliability.

Combines multiple trees.

Example:

```text
Fraud detection
```

---

## 2.7.4 SVM

This section explains an algorithm that separates classes using the best decision boundary.

Finds best decision boundary.

Example:

```text
Image classification
```

---

## 2.7.5 Naive Bayes

This section explains a probability-based algorithm commonly used for text classification.

Probability-based classification.

Example:

```text
Spam detection
```

---

## 2.7.6 Neural Networks

This section explains models that learn complex patterns using connected layers.

Used for complex tasks.

Example:

```text
Face recognition
```

---

# 2.8 Classification Output Types

This section explains the different forms of output a classification model can produce.

## 2.8.1 Predicted Label

This section explains the final category selected by the model.

```text
Spam
```

---

## 2.8.2 Probability Score

This section explains the model’s confidence for each category.

```text
Spam = 95%
Not Spam = 5%
```

---

## 2.8.3 Ranking Output

This section explains outputs where possible classes or items are sorted by likelihood.

```text
Top product recommendations
```

---

## 2.8.4 Step-by-Step Prediction Flow

This section explains how the model produces a final classification result.

```text
1. New input arrives
2. Model calculates probabilities
3. Highest category selected
4. Final prediction returned
```

---

# 2.9 Evaluation Metrics

This section explains how classification model performance is measured.

## 2.9.1 Accuracy

This section explains the percentage of predictions that are correct.

```text
95 correct out of 100
```

---

## 2.9.2 Precision

This section explains how many predicted positive results are actually correct.

Example:

```text
Fraud detection
```

---

## 2.9.3 Recall

This section explains how many actual positive cases the model successfully finds.

Example:

```text
Disease detection
```

---

## 2.9.4 F1 Score

This section explains the metric used to balance precision and recall.

---

## 2.9.5 Confusion Matrix

This section explains the table used to inspect correct and wrong predictions.

---

## 2.9.6 Confusion Matrix Example

This section shows how prediction results are categorized.

| Actual | Predicted |
| --- | --- |
| Spam | Spam → TP |
| Spam | Not Spam → FN |
| Not Spam | Spam → FP |
| Not Spam | Not Spam → TN |

---

## 2.9.7 Step-by-Step Evaluation Flow

This section explains how to evaluate a trained classification model.

```text
1. Make predictions
2. Compare actual labels
3. Calculate metrics
4. Identify weaknesses
```

---

# 2.10 Common Problems in Classification

This section explains common issues that cause poor classification performance.

## 2.10.1 Overfitting

This section explains when the model memorizes training data instead of learning general patterns.

Example:

```text
Only detects old spam patterns
```

---

## 2.10.2 Underfitting

This section explains when the model is too simple and fails to learn useful patterns.

Example:

```text
Fails to detect fraud
```

---

## 2.10.3 Imbalanced Dataset

This section explains when one class appears much more often than another class.

Example:

```text
99 normal transactions
1 fraud transaction
```

---

## 2.10.4 Noisy Labels

This section explains when wrong labels confuse the model during training.

Example:

```text
Spam email labeled as normal
```

---

## 2.10.5 Step-by-Step Problem Solving

This section explains how to diagnose and improve classification problems.

```text
1. Train model
2. Test model
3. Identify issue
4. Improve data/model
5. Retrain
```

---

# 2.11 Real-World Applications

This section shows where classification is commonly used in real systems.

| Industry | Input | Output |
| --- | --- | --- |
| Banking | Customer data | Approve/Reject |
| Healthcare | Symptoms | Disease prediction |
| Retail | Customer behavior | Buy/Not Buy |
| Security | Face image | Person identity |
| Email | Email text | Spam/Not Spam |

---

## 2.11.1 Real-World Workflow

This section explains the general workflow for applying classification in real-world systems.

```text
1. Collect business data
2. Train model
3. Deploy model
4. Predict future cases
```

---

# 2.12 End-to-End Example: Fraud Detection System

This section connects all classification concepts into one full practical example.

## 2.12.1 Step 1: Collect Data

This section explains the first step of gathering past transaction records.

```text
Past transaction records
```

---

## 2.12.2 Step 2: Add Labels

This section explains how each transaction is marked with its correct class.

```text
Fraud / Not Fraud
```

---

## 2.12.3 Step 3: Train Model

This section explains how the classifier learns fraud patterns from labeled examples.

```text
Learn fraud patterns
```

---

## 2.12.4 Step 4: Evaluate Model

This section explains how the trained model is tested using classification metrics.

```text
Check accuracy, precision, recall, F1 score, and confusion matrix
```

---

## 2.12.5 Step 5: Deploy Model

This section explains how the final model is placed into a real system.

```text
Real-time fraud detection
```

---

## 2.12.6 Step 6: Predict New Transaction

This section explains how the deployed model classifies new unseen transactions.

```text
New transaction → Fraud
```

---

## 2.12.7 Full Pipeline

This section summarizes the complete classification workflow.

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

This section explains the main difference between classification and regression.

| Classification | Regression |
| --- | --- |
| Predict categories | Predict numbers |
| Spam detection | House price prediction |
| Fraud detection | Temperature prediction |

---

# 2.14 Final Summary

This section summarizes the most important classification ideas before moving to regression.

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
