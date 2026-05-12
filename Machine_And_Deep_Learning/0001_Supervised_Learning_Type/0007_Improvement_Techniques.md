# 7. IMPROVEMENT TECHNIQUES

This section explains how to improve Machine Learning (ML) model performance.

Building a model is only the beginning.

Most first models are:
- inaccurate
- unstable
- overfitted
- underfitted
- slow

This section answers:

**"How do we make a model better?"**

---

## 7.1 Feature Engineering

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Feature Engineering | Creating better input features for models | Create, remove, transform features | Price per square foot | Improves model quality |
| Feature Creation | Create new useful variables | Combine raw data | Age + income ratio | Adds better signals |
| Feature Removal | Remove useless variables | Delete irrelevant features | Remove customer ID | Reduces noise |
| Feature Transformation | Change feature format | Convert raw values | Date → month/year | Makes data useful |

---

## 7.2 Feature Scaling

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Feature Scaling | Adjust feature values into similar ranges | Scale large/small values | Age vs salary | Helps fair learning |
| Why Needed | Prevent large values dominating | Equal importance | Income = 100000 | Important for many models |

---

## 7.3 Normalization

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Normalization | Scales values between 0 and 1 | Uses min-max scaling | Age → 0.65 | Common scaling method |
| Formula | `(x-min)/(max-min)` | Converts range | 0 to 1 output | Easy interpretation |

---

## 7.4 Standardization

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Standardization | Converts data to mean = 0 and standard deviation = 1 | Centers data | Salary values | Common in ML |
| Formula | `(x-mean)/standard deviation` | Standard scale | Around 0 | Useful for normal distributions |

---

## 7.5 Cross Validation (CV)

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Cross Validation (CV) | Evaluates model using multiple splits | Train/test repeatedly | 5-fold CV | More reliable evaluation |
| Goal | Reduce overfitting risk | Better validation | Stable scores | Common technique |


### 7.5.1 K-Fold Cross Validation

| Step | Process | Input | Output | Purpose |
| --- | --- | --- | --- | --- |
| 1 | Split dataset | Full dataset | K groups | Create folds |
| 2 | Train model | K-1 groups | Trained model | Learn |
| 3 | Validate model | Remaining group | Validation score | Evaluate |
| 4 | Repeat process | Different folds | Multiple scores | Better reliability |
| 5 | Average scores | All results | Final score | Final evaluation |

---

## 7.6 Hyperparameter Tuning

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Hyperparameter Tuning | Finding best model settings | Test different configurations | Tree depth | Improves performance |
| Examples | Learning rate, batch size | Try multiple values | Neural network tuning | Common task |

---

## 7.7 Grid Search

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Grid Search | Tests all parameter combinations | Exhaustive search | Tree depth + learning rate | Accurate but slow |
| Best For | Small parameter space | Limited combinations | Small datasets | Computationally expensive |

---

## 7.8 Random Search

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Random Search | Tests random parameter combinations | Random sampling | Random tree depth | Faster than grid search |
| Best For | Large parameter space | Many combinations | Deep learning tuning | Saves time |

---

## 7.9 Ensemble Methods

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Ensemble Methods | Combine multiple models | Voting/averaging predictions | Random Forest | Improves accuracy |
| Goal | Reduce weaknesses of single model | Stronger predictions | Fraud detection | Common technique |

---

## 7.10 Bagging

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Bagging | Train models independently | Different random datasets | Random Forest | Reduces variance |
| Full Form | Bootstrap Aggregating | Combine predictions | Tree models | Common interview question |

---

## 7.11 Boosting

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Boosting | Train models sequentially | Fix previous model errors | Gradient Boosting | Improves accuracy |
| Goal | Focus on difficult examples | Better performance | XGBoost | Powerful method |

---

## 7.12 Regularization

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Regularization | Reduces model complexity | Penalizes large weights | Ridge Regression | Prevents overfitting |
| L1 Regularization | Removes features | Some weights become zero | Lasso | Feature selection |
| L2 Regularization | Shrinks weights | Smaller weights | Ridge | Keeps all features |

---

## 7.13 Early Stopping

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Early Stopping | Stops training before overfitting | Monitor validation score | Neural networks | Prevents over-training |
| Trigger | Validation performance worsens | Stop training | Best epoch | Saves time |

---

## 7.14 Data Augmentation

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Data Augmentation | Create extra training data | Modify existing data | Rotate images | Common in deep learning |
| Goal | Increase dataset size | More training examples | Image recognition | Helps small datasets |

---

## 7.15 Dimensionality Reduction

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Dimensionality Reduction | Reduce number of features | Keep important information | Principal Component Analysis (PCA) | Reduces complexity |
| Goal | Faster training | Less noise | Large datasets | Useful for many features |

---

## 7.16 Improvement Technique Selection Guide

| Problem | Solution | Example | Why It Helps | Notes |
| --- | --- | --- | --- | --- |
| Overfitting | Regularization | Ridge | Reduces complexity | Common fix |
| Underfitting | Better model | Deeper tree | Learns better | Common fix |
| Poor features | Feature engineering | New variables | Better inputs | Important |
| Unstable results | Cross validation | K-fold | Better evaluation | Reliable |
| Slow tuning | Random search | Random parameters | Saves time | Faster |

---

## 7.17 Real World Example

### House Price Prediction Improvement

| Problem | Solution | Result | Example | Outcome |
| --- | --- | --- | --- | --- |
| Poor features | Feature engineering | Better inputs | Price per sqft | Better accuracy |
| Overfitting | Regularization | Better generalization | Ridge | Stable predictions |
| Weak model | Ensemble method | Stronger predictions | Random Forest | Higher accuracy |

---

## 7.18 Final Summary

| Question | Answer | Example | Notes | Importance |
| --- | --- | --- | --- | --- |
| How improve model performance? | Better data + better tuning | House pricing | Continuous process | Very important |
| Why use scaling? | Fair feature comparison | Age vs salary | Important for some models | Common |
| Why use regularization? | Prevent overfitting | Ridge/Lasso | Better generalization | Critical |
| Why use ensemble methods? | Combine strengths | Random Forest | Higher accuracy | Powerful |
