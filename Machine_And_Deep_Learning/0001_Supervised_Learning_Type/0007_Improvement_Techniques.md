# 7. IMPROVEMENT TECHNIQUES

This section explains methods used to improve Machine Learning (ML) model performance after building the first model.

Most first models are not perfect:

- Low accuracy
- Overfitting
- Underfitting
- Unstable predictions
- Slow training
- Weak features

This section answers:

```text
"How do we improve a weak model and make it more reliable?"
```

---

# 7.1 Improvement Examples Used Throughout This Section

This section introduces the examples reused throughout this topic.

| Example | ML Task | Problem | Improvement Goal | Real Use Case |
| --- | --- | --- | --- | --- |
| House Price Prediction | Regression | Weak features | Improve price prediction | Real estate |
| Spam Detection | Classification | Overfitting | Better generalization | Gmail |
| Fraud Detection | Classification | Imbalanced data | Better detection | Banking |
| Image Classification | Deep Learning | Small dataset | Improve accuracy | Computer vision |

---

# 7.2 Feature Engineering

This section explains how to create better input features.

Better features often improve model performance more than changing algorithms.

---

## 7.2.1 Feature Engineering Methods

| Method | Meaning | Example | Benefit | Risk |
| --- | --- | --- | --- | --- |
| Feature Creation | Create new features | Price per sqft | Better signal | Wrong assumptions |
| Feature Removal | Remove useless features | Remove customer ID | Less noise | Remove useful info |
| Feature Transformation | Change format | Date → Month | Easier learning | Data loss |

---

## 7.2.2 Example A: House Price Feature Engineering (Detailed)

```text
Original features:
- House size
- Total price

Problem:
Model ignores pricing efficiency

Improvement:
Create new feature:
Price per square foot

Result:
Better house pricing predictions
```

---

## 7.2.3 Example B: Fraud Feature Engineering (Detailed)

```text
Original features:
- Transaction amount

Improvement:
Add:
- Transaction frequency
- Location change
- Time difference

Result:
Better fraud detection
```

---

# 7.3 Feature Scaling

This section explains making features similar in size.

Some algorithms struggle when feature values are very different.

---

## 7.3.1 Example A: Salary vs Age Problem

```text
Age:
25

Salary:
100,000

Problem:
Salary dominates model learning

Solution:
Scale both features
```

---

## 7.3.2 Step-by-Step Scaling Flow

```text
1. Detect large feature differences
2. Apply scaling
3. Retrain model
4. Improve performance
```

---

# 7.4 Normalization

This section explains scaling values between 0 and 1.

---

## 7.4.1 Normalization Formula

```text
(x - min) / (max - min)
```

---

## 7.4.2 Example A: Age Normalization (Detailed)

```text
Original age:
65

Dataset age range:
20 → 80

Normalized result:
0.75
```

---

# 7.5 Standardization

This section explains scaling values around mean = 0.

---

## 7.5.1 Standardization Formula

```text
(x - mean) / standard deviation
```

---

## 7.5.2 Example A: Salary Standardization (Detailed)

```text
Original salary:
RM8,000

Dataset mean:
RM5,000

After standardization:
Positive value above average
```

---

# 7.6 Cross Validation (CV)

This section explains more reliable evaluation.

Instead of testing once, test multiple times.

---

## 7.6.1 Cross Validation Process

```text
1. Split dataset multiple times
2. Train model
3. Validate model
4. Repeat
5. Average results
```

---

## 7.6.2 Example A: House Price Cross Validation

```text
Dataset:
1,000 houses

Split 1:
Train/Test

Split 2:
Train/Test

Split 3:
Train/Test

Final average accuracy calculated
```

---

# 7.7 K-Fold Cross Validation

This section explains the most common cross-validation method.

---

## 7.7.1 K-Fold Process

| Step | Process | Input | Output | Purpose |
| --- | --- | --- | --- | --- |
| 1 | Split dataset | Full dataset | K groups | Create folds |
| 2 | Train model | K-1 groups | Model | Learn |
| 3 | Validate | Remaining fold | Score | Evaluate |
| 4 | Repeat | Different folds | Multiple scores | Reliability |
| 5 | Average | All scores | Final score | Better evaluation |

---

## 7.7.2 Example A: 5-Fold Validation (Detailed)

```text
Dataset:
1000 rows

Split into:
5 groups of 200

Train on:
800 rows

Validate on:
200 rows

Repeat 5 times
```

---

# 7.8 Hyperparameter Tuning

This section explains finding better model settings.

Hyperparameters are settings chosen before training.

---

## 7.8.1 Common Hyperparameters

| Hyperparameter | Example | Affects | Model Type | Importance |
| --- | --- | --- | --- | --- |
| Learning Rate | 0.01 | Training speed | Neural Networks | High |
| Tree Depth | 10 | Complexity | Decision Trees | High |
| Batch Size | 64 | Training speed | Deep Learning | Medium |

---

## 7.8.2 Example A: Decision Tree Tuning

```text
Depth = 2:
Underfitting

Depth = 100:
Overfitting

Depth = 10:
Balanced model
```

---

# 7.9 Grid Search

This section explains exhaustive hyperparameter testing.

---

## 7.9.1 Example A: Grid Search (Detailed)

```text
Test combinations:

Learning Rate:
0.01
0.1

Tree Depth:
5
10

Total combinations:
4

Best combination selected
```

---

# 7.10 Random Search

This section explains random hyperparameter testing.

Faster than Grid Search.

---

## 7.10.1 Example A: Random Search (Detailed)

```text
Instead of testing all 100 combinations

Model randomly tests:
10 combinations

Finds good settings faster
```

---

# 7.11 Ensemble Methods

This section explains combining multiple models.

Multiple weak models can create one stronger model.

---

## 7.11.1 Ensemble Types

| Method | How It Works | Example | Benefit | Risk |
| --- | --- | --- | --- | --- |
| Voting | Multiple models vote | Classification | Better accuracy | Slower |
| Averaging | Average predictions | Regression | Stable output | More computation |

---

## 7.11.2 Example A: House Prediction Ensemble

```text
Model A predicts:
RM500,000

Model B predicts:
RM520,000

Model C predicts:
RM510,000

Final average:
RM510,000
```

---

# 7.12 Bagging (Bootstrap Aggregating)

This section explains independent model training.

---

## 7.12.1 Example A: Random Forest Bagging

```text
1. Create multiple datasets

2. Train multiple decision trees

3. Combine predictions

Result:
Better stability
```

---

# 7.13 Boosting

This section explains sequential learning.

Each new model fixes previous mistakes.

---

## 7.13.1 Example A: Gradient Boosting (Detailed)

```text
Model 1:
Makes mistakes

Model 2:
Fixes previous mistakes

Model 3:
Improves again

Final model:
Higher accuracy
```

---

# 7.14 Regularization

This section explains reducing overfitting.

---

## 7.14.1 Regularization Types

| Type | Full Form | How It Works | Example | Result |
| --- | --- | --- | --- | --- |
| L1 Regularization | Lasso | Removes weak features | Feature selection | Simpler model |
| L2 Regularization | Ridge | Shrinks weights | House pricing | Reduces overfitting |

---

## 7.14.2 Example A: Overfitting Fix

```text
Model memorizes training data

Apply Ridge Regression

Model becomes simpler

Test accuracy improves
```

---

# 7.15 Early Stopping

This section explains stopping training before overfitting happens.

---

## 7.15.1 Example A: Neural Network Training

```text
Epoch 10:
Validation improves

Epoch 20:
Validation improves

Epoch 30:
Validation gets worse

Stop training at epoch 20
```

---

# 7.16 Data Augmentation

This section explains creating more training data.

Very common in image learning.

---

## 7.16.1 Example A: Image Augmentation

```text
Original image:
Cat image

Create:
- Rotated image
- Flipped image
- Brightness adjusted image

Dataset becomes larger
```

---

# 7.17 Dimensionality Reduction

This section explains reducing unnecessary features.

---

## 7.17.1 Example A: Customer Dataset

```text
Original features:
500 columns

Problem:
Too slow

Apply Principal Component Analysis (PCA)

Reduce to:
50 important features
```

---

# 7.18 Improvement Technique Selection Guide

This section helps choose the right fix.

| Problem | Solution | Example | Why It Works | Result |
| --- | --- | --- | --- | --- |
| Overfitting | Regularization | Ridge | Reduce complexity | Better generalization |
| Underfitting | Better model | Deeper tree | Learn better | Higher accuracy |
| Weak features | Feature engineering | New features | Better inputs | Better predictions |
| Unstable results | Cross validation | K-Fold | Reliable evaluation | Stable model |
| Small dataset | Data augmentation | More images | More training data | Better performance |

---

# 7.19 Real-World Example: House Price Model Improvement

This section connects everything.

| Problem | Solution | Result | Example | Outcome |
| --- | --- | --- | --- | --- |
| Weak features | Feature engineering | Better signals | Price/sqft | Better predictions |
| Overfitting | Regularization | Better generalization | Ridge | Stable model |
| Weak algorithm | Ensemble | Stronger predictions | Random Forest | Higher accuracy |

---

## 7.19.1 Full Improvement Flow

```text
Build First Model
→ Detect Problems
→ Choose Fix
→ Retrain Model
→ Evaluate Again
→ Deploy Better Model
```

---

# 7.20 Final Summary

This section summarizes improvement techniques.

```text
Weak Model
→ Better Features
→ Better Tuning
→ Better Validation
→ Better Model
```

Core lesson:

```text
Improving ML models is iterative.
```

You rarely build a perfect model on the first attempt.

Next topic:

```text
Deployment & Usage
```
