# 6. MODEL ISSUES

This section explains common problems that happen when training Machine Learning (ML) models.

Most models do **not work perfectly on the first try**.

Common problems:

- Model learns too little
- Model learns too much
- Model learns wrong patterns
- Model becomes unstable
- Model performs well in training but fails in real life

This section answers:

```text
"Why is my model performing badly?"
```

---

# 6.1 Problem Examples Used Throughout This Section

This section introduces the examples reused throughout this topic.

| Example | ML Task | Problem Type | Real Use Case | Output |
| --- | --- | --- | --- | --- |
| House Price Prediction | Regression | Overfitting/Underfitting | Real estate | House price |
| Spam Detection | Classification | Overfitting | Gmail | Spam/Not Spam |
| Fraud Detection | Classification | Class imbalance | Banking | Fraud/Normal |
| Medical Diagnosis | Classification | Data leakage | Healthcare | Disease prediction |

---

# 6.2 Underfitting

This section explains when the model is too simple to learn real patterns.

The model fails on both training data and new data.

---

## 6.2.1 Underfitting Symptoms

| Metric | Behavior | Problem | Result | Warning Level |
| --- | --- | --- | --- | --- |
| Training Error | High | Model cannot learn | Bad predictions | High |
| Testing Error | High | Poor generalization | Fails everywhere | High |
| Model Complexity | Too low | Too simple | Weak learning | Medium |

---

## 6.2.2 Example A: House Price Underfitting (Detailed)

```text
1. House data:
   - Size
   - Location
   - Bedrooms

2. Model used:
   Very simple Linear Regression

3. Real house prices are complex

4. Model predicts:
   Every house ≈ RM500,000

5. Result:
   Wrong predictions for expensive and cheap houses
```

---

## 6.2.3 Example B: Student Score Prediction (Detailed)

```text
Input:
Study hours

Missing feature:
Student intelligence
Attendance
Practice tests

Model predicts poorly because important information is missing
```

---

# 6.3 Overfitting

This section explains when the model memorizes training data instead of learning patterns.

Training performance looks amazing.

Real-world performance becomes bad.

---

## 6.3.1 Overfitting Symptoms

| Metric | Behavior | Problem | Result | Warning Level |
| --- | --- | --- | --- | --- |
| Training Accuracy | Very high | Looks great | Misleading | High |
| Testing Accuracy | Low | Poor generalization | Fails new data | High |
| Model Complexity | Too high | Too flexible | Memorization | High |

---

## 6.3.2 Example A: Spam Detection Overfitting (Detailed)

```text
1. Training spam emails contain:
   "Free"
   "Win"
   "Prize"

2. Model memorizes:
   Every email with "free" = spam

3. New email:
   "Free office meeting room available"

4. Model predicts:
   Spam

5. Result:
   Wrong prediction
```

---

## 6.3.3 Example B: House Price Overfitting (Detailed)

```text
1. Model memorizes exact training house prices

2. New house enters system

3. House is slightly different

4. Model fails to predict correctly
```

---

# 6.4 Good Fit (Balanced Model)

This section explains the ideal learning situation.

The model learns useful patterns and generalizes well.

---

## 6.4.1 Good Fit Characteristics

| Metric | Training Performance | Testing Performance | Result | Status |
| --- | --- | --- | --- | --- |
| Error | Low | Low | Good predictions | Healthy |
| Generalization | Strong | Strong | Real-world success | Best |

---

## 6.4.2 Example A: House Price Good Fit (Detailed)

```text
1. Model learns:
   Bigger house → higher price
   Better location → higher price

2. New house enters system

3. Model predicts accurately

4. Real-world prediction works well
```

---

# 6.5 Underfitting vs Overfitting vs Good Fit

This section compares the three major model states.

| Model State | Training Error | Testing Error | Problem | Example |
| --- | --- | --- | --- | --- |
| Underfitting | High | High | Too simple | Weak regression |
| Good Fit | Low | Low | Balanced | Stable model |
| Overfitting | Low | High | Too complex | Memorization |

---

## 6.5.1 Example Comparison (Detailed)

```text
Underfitting:
Predicts everything badly

Good Fit:
Predicts most cases correctly

Overfitting:
Perfect training results but fails new cases
```

---

# 6.6 Bias

This section explains error caused by overly simple assumptions.

High bias often causes underfitting.

---

## 6.6.1 Example A: High Bias (Detailed)

```text
Salary prediction model:

Only uses:
Years of experience

Ignores:
Education
Skills
Industry

Predictions become inaccurate
```

---

# 6.7 Variance

This section explains error caused by extreme sensitivity to training data.

High variance often causes overfitting.

---

## 6.7.1 Example A: High Variance (Detailed)

```text
House A:
RM500,000

Very similar House B:
RM510,000

Model predicts:
RM500,000 for A
RM900,000 for B

Model is unstable
```

---

# 6.8 Bias vs Variance Tradeoff

This section explains balancing simple vs complex models.

---

## 6.8.1 Tradeoff Table

| Model Complexity | Bias | Variance | Result | Risk |
| --- | --- | --- | --- | --- |
| Very Simple | High | Low | Underfitting | Weak model |
| Balanced | Medium | Medium | Good fit | Best |
| Very Complex | Low | High | Overfitting | Unstable |

---

## 6.8.2 Example A: Decision Tree Depth (Detailed)

```text
Tree depth = 2:
Too simple → underfitting

Tree depth = 100:
Too complex → overfitting

Tree depth = 10:
Balanced learning
```

---

# 6.9 Model Complexity

This section explains model flexibility.

---

## 6.9.1 Complexity Levels

| Complexity Level | Example Model | Learning Ability | Risk | Result |
| --- | --- | --- | --- | --- |
| Low | Linear Regression | Limited | Underfitting | Weak |
| Medium | Random Forest | Balanced | Lower | Better |
| High | Deep Neural Network | Very flexible | Overfitting | Risky |

---

## 6.9.2 Example A: Neural Network Complexity

```text
Small dataset:
1,000 rows

Huge neural network:
10 million parameters

Result:
Overfitting risk becomes high
```

---

# 6.10 Noise in Data

This section explains random bad data.

Noise confuses learning.

---

## 6.10.1 Example A: Wrong Label Noise

```text
Spam email labeled:
Not Spam

Model learns wrong pattern
```

---

## 6.10.2 Example B: Typing Error Noise

```text
House price:
RM500,000

Mistyped as:
RM5,000,000
```

---

# 6.11 Outliers

This section explains extremely unusual values.

---

## 6.11.1 Example A: House Price Outlier

```text
Most houses:
RM500,000

One house:
RM50,000,000

Model becomes distorted
```

---

## 6.11.2 Example B: Salary Outlier

```text
Most salaries:
RM5,000

One CEO salary:
RM500,000
```

---

# 6.12 Data Leakage

This section explains one of the most dangerous ML mistakes.

The model accidentally sees future information.

---

## 6.12.1 Example A: Medical Leakage (Detailed)

```text
Features include:
Final diagnosis report

Problem:
Diagnosis report already contains answer

Model gets fake high accuracy
```

---

## 6.12.2 Example B: Student Exam Leakage

```text
Training data accidentally contains test answers

Model scores:
99%

Real-world performance:
Poor
```

---

# 6.13 Class Imbalance

This section explains unequal class distribution.

Very common in fraud detection.

---

## 6.13.1 Class Imbalance Example (Detailed)

```text
1,000 transactions

990 Normal
10 Fraud

Model predicts:
Everything = Normal

Accuracy:
99%

Reality:
Fraud detection failed
```

---

# 6.14 Training Curve Problem Detection

This section explains how training metrics reveal problems.

| Training Error | Validation Error | Problem | Meaning | Action |
| --- | --- | --- | --- | --- |
| High | High | Underfitting | Weak model | Increase complexity |
| Low | High | Overfitting | Memorization | Regularization |
| Low | Low | Good Fit | Healthy model | Maintain |

---

## 6.14.1 Example A: Training Curve Reading

```text
Train accuracy:
99%

Validation accuracy:
70%

Problem:
Overfitting
```

---

# 6.15 Real-World Debugging Example

This section connects everything together.

### House Price Model Debugging

| Situation | Problem | Result | Example | Fix |
| --- | --- | --- | --- | --- |
| Very simple model | Underfitting | Poor predictions | Straight line pricing | Better model |
| Very complex model | Overfitting | Memorization | Deep tree | Regularization |
| Dirty dataset | Noise | Wrong learning | Wrong prices | Data cleaning |
| Leakage | Fake success | Production failure | Future data | Remove leakage |

---

## 6.15.1 Full Debugging Flow

```text
Bad performance
→ Identify issue
→ Diagnose cause
→ Apply fix
→ Retrain model
→ Re-evaluate
```

---

# 6.16 Why Model Issues Matter

This section explains why debugging skills matter.

| Reason | Example | Business Impact | Result | Importance |
| --- | --- | --- | --- | --- |
| Prevent bad deployment | Fraud model fails | Financial loss | Major issue | High |
| Improve accuracy | Better healthcare predictions | Better treatment | Stronger model | High |
| Better generalization | New customer predictions | Better business decisions | Reliable AI | Critical |

---

# 6.17 Final Summary

This section summarizes model issues.

```text
Underfitting → Too Simple

Overfitting → Too Complex

Good Fit → Balanced

Noise → Bad Data

Leakage → Fake Accuracy

Class Imbalance → Misleading Accuracy
```

Core lesson:

```text
Good model performance requires:

Good data
+ Balanced model complexity
+ Proper evaluation
```

Next topic:

```text
Improvement Techniques
```
