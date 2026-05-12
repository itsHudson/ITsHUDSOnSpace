# 6. MODEL ISSUES

This section explains common problems that happen when training Machine Learning (ML) models.

Most models do **not work perfectly on the first try**.

Common problems:
- Model learns too little
- Model learns too much
- Model learns wrong patterns
- Model becomes unstable

This section helps answer:

**"Why is my model performing badly?"**

---

## 6.1 Underfitting

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Underfitting | Model is too simple and cannot learn real patterns | Model fails to capture important relationships | Straight line for complex house prices | Poor performance everywhere |
| Training Error | High training error | Model performs badly on training data | Wrong house predictions | Warning sign |
| Testing Error | High testing error | Performs badly on new data too | Wrong future predictions | Also high |
| Main Cause | Model too weak | Not enough learning power | Very simple algorithm | Common beginner issue |

---

## 6.2 Overfitting

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Overfitting | Model memorizes training data instead of learning patterns | Learns noise instead of useful information | Memorizing spam emails | Very common issue |
| Training Error | Very low training error | Looks excellent on training data | 99% training accuracy | Misleading |
| Testing Error | High testing error | Fails on new data | Poor generalization | Major warning sign |
| Main Cause | Model too complex | Too many parameters | Deep decision tree | Dangerous |

---

## 6.3 Good Fit (Balanced Model)

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Good Fit | Model learns real patterns correctly | Performs well on both training and testing data | Good house price prediction | Ideal outcome |
| Training Performance | Low training error | Learns properly | Strong training results | Healthy model |
| Testing Performance | Low testing error | Generalizes well | Good future predictions | Desired result |

---

## 6.4 Underfitting vs Overfitting vs Good Fit

| Model State | Training Error | Testing Error | Problem | Example |
| --- | --- | --- | --- | --- |
| Underfitting | High | High | Too simple | Weak regression model |
| Good Fit | Low | Low | Balanced | Strong prediction model |
| Overfitting | Low | High | Too complex | Memorized dataset |

---

## 6.5 Bias

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Bias | Error caused by overly simple assumptions | Model cannot capture complexity | Always predicting average salary | Often causes underfitting |
| High Bias | Model too simple | Weak learning | Basic linear model | Poor flexibility |
| Result | Consistent mistakes | Same wrong predictions | House price errors | Needs stronger model |

---

## 6.6 Variance

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Variance | Error caused by sensitivity to small changes | Model reacts too strongly | Different predictions for similar houses | Often causes overfitting |
| High Variance | Model unstable | Learns noise | Random predictions | Dangerous |
| Result | Inconsistent predictions | Poor generalization | Test failure | Needs simplification |

---

## 6.7 Bias vs Variance Tradeoff

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Bias-Variance Tradeoff | Balance between simple and complex models | Increase complexity → lower bias but higher variance | Decision tree depth | Core ML concept |
| Goal | Keep both low | Find balanced model | Good fit | Important tuning concept |

---

## 6.8 Model Complexity

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Model Complexity | How flexible a model is | More parameters = more flexibility | Deep neural network | Can overfit |
| Low Complexity | Simple model | Limited learning | Linear regression | High bias |
| High Complexity | Complex model | Learns detailed patterns | Deep tree | High variance |

---

## 6.9 Noise in Data

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Noise | Random incorrect data | Misleads learning | Wrong house price | Common issue |
| Data Errors | Wrong labels/values | Creates confusion | Spam marked normal | Reduces accuracy |
| Random Patterns | Model learns useless information | Overfitting risk | Outlier values | Needs cleaning |

---

## 6.10 Outliers

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Outliers | Extremely unusual values | Distorts learning | RM50 million house | Common in regression |
| Impact | Pulls predictions | Creates wrong patterns | Salary prediction issues | Must detect carefully |

---

## 6.11 Data Leakage

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Data Leakage | Model accidentally learns future/test information | Gets unfair advantage | Test data used in training | Fake high accuracy |
| Problem | Unrealistic performance | Fails in production | 99% test accuracy | Must avoid |

---

## 6.12 Class Imbalance

| Topic | Definition | How It Works | Example | Important Notes |
| --- | --- | --- | --- | --- |
| Class Imbalance | One class has much more data than another | Model ignores rare classes | Fraud detection | Common classification issue |
| Example | 99 normal transactions, 1 fraud | Predicts everything normal | High fake accuracy | Dangerous |

---

## 6.13 Training Curve Problem Detection

| Scenario | Training Error | Validation Error | Problem |
| --- | --- | --- | --- |
| High train + high validation | High | High | Underfitting |
| Low train + high validation | Low | High | Overfitting |
| Low train + low validation | Low | Low | Good fit |

---

## 6.14 Real World Example

### House Price Model

| Situation | Problem | Result | Example | Fix |
| --- | --- | --- | --- | --- |
| Very simple model | Underfitting | Poor predictions | Straight line for complex pricing | Use better model |
| Very complex model | Overfitting | Memorization | Deep tree | Regularization |
| Balanced model | Good fit | Strong predictions | Stable pricing model | Maintain balance |

---

## 6.15 Why Model Issues Matter

| Reason | Explanation | Example | Business Impact | Notes |
| --- | --- | --- | --- | --- |
| Prevent bad models | Detect problems early | Overfitting detection | Save money | Important |
| Improve accuracy | Fix weak models | Better fraud detection | Better business decisions | Critical |
| Better generalization | Perform well on new data | New customers | Real-world success | Required |

---

## 6.16 Final Summary

| Question | Answer | Example | Notes | Importance |
| --- | --- | --- | --- | --- |
| What is underfitting? | Model too simple | Weak predictions | High errors | Important |
| What is overfitting? | Model memorizes data | Bad future predictions | Low train/high test error | Very important |
| What is bias? | Too simple assumptions | Underfitting | Low flexibility | Core concept |
| What is variance? | Too sensitive to data | Overfitting | Unstable predictions | Core concept |
| Why learn this? | Most models fail here first | Real-world ML debugging | Essential skill | Critical |
