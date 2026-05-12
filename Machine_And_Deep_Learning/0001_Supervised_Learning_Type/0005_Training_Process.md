# 5. TRAINING PROCESS

This section explains how a Machine Learning (ML) model actually learns from data.

Before training:

- Model knows nothing
- Parameters may start randomly
- Predictions are usually bad

During training:

- Model makes predictions
- Measures mistakes
- Learns from mistakes
- Updates itself
- Improves over time

Training answers:

```text
"How does a model become smarter?"
```

---

## 5.1 Training Examples Used Throughout This Section

This section introduces the examples reused throughout the entire training topic.

| Example | Input | Output | ML Type | Real Use Case |
| --- | --- | --- | --- | --- |
| House Price Prediction | House features | House price | Regression | Real estate |
| Spam Detection | Email features | Spam/Not Spam | Classification | Gmail |
| Fraud Detection | Transaction data | Fraud/Not Fraud | Classification | Banking |
| Image Classification | Image pixels | Cat/Dog/Bird | Classification | Computer vision |

---

# 5.2 What is Training Process?

This section explains the overall learning process.

Training is when the model learns patterns from historical data.

---

## 5.2.1 Step-by-Step Training Flow

```text
1. Receive input features (X)
2. Make prediction (ŷ)
3. Compare prediction with actual output (Y)
4. Calculate error/loss
5. Update model parameters
6. Repeat many times
7. Improve model performance
```

---

## 5.2.2 Example A: House Price Training (Detailed)

```text
1. Input house:
   - Size = 2,000 sqft
   - Location = Kuala Lumpur
   - Bedrooms = 4

2. Model predicts:
   RM780,000

3. Actual house price:
   RM850,000

4. Error:
   RM70,000

5. Model updates parameters

6. Future prediction becomes better
```

---

## 5.2.3 Example B: Spam Detection Training (Detailed)

```text
1. Input email:
   "Claim your free reward"

2. Model predicts:
   Not Spam

3. Actual label:
   Spam

4. Model made mistake

5. Model updates spam detection rules
```

---

# 5.3 Model Fitting

This section explains how models adjust themselves to match training data.

---

## 5.3.1 Model Fitting Types

| Type | Meaning | Example | Problem | Result |
| --- | --- | --- | --- | --- |
| Good Fit | Learns useful patterns | Accurate pricing | None | Best result |
| Overfitting | Memorizes training data | Memorizes spam keywords | Poor future performance | Bad |
| Underfitting | Learns too little | Poor fraud detection | Weak model | Bad |

---

## 5.3.2 Example A: Good Fit (Detailed)

```text
Training data:
Many different houses

Model learns:
- Bigger house → higher price
- Better location → higher price

Result:
Accurate future predictions
```

---

## 5.3.3 Example B: Overfitting (Detailed)

```text
Training spam emails:
Contains keyword "free"

Model memorizes:
Every email with "free" = spam

Problem:
Normal email:
"Free meeting room available"

Wrongly predicted as spam
```

---

# 5.4 Prediction (ŷ / Y-Hat)

This section explains predicted output during training.

ŷ (Y-hat) means predicted output.

---

## 5.4.1 Example A: Regression Prediction (Detailed)

```text
Input:
House details

Predicted output (ŷ):
RM480,000
```

---

## 5.4.2 Example B: Classification Prediction (Detailed)

```text
Input:
Email text

Predicted output (ŷ):
Spam
```

---

# 5.5 Actual Output (Y)

This section explains the real correct answer.

Y = actual correct output.

---

## 5.5.1 Example A: House Price Actual Output

```text
Actual selling price:
RM500,000
```

---

## 5.5.2 Example B: Spam Actual Output

```text
Actual email label:
Spam
```

---

# 5.6 Loss Function

This section explains how prediction mistakes are measured.

Loss tells the model how wrong it is.

---

## 5.6.1 Common Loss Functions

| Loss Function | Full Form | Used For | Example | Why Important |
| --- | --- | --- | --- | --- |
| Mean Squared Error (MSE) | Mean Squared Error | Regression | House price | Punishes large errors |
| Mean Absolute Error (MAE) | Mean Absolute Error | Regression | Salary prediction | Easy interpretation |
| Cross Entropy Loss | Cross Entropy Loss | Classification | Spam detection | Common for classification |

---

## 5.6.2 Example A: House Loss (Detailed)

```text
Predicted:
RM480,000

Actual:
RM500,000

Loss:
RM20,000 difference
```

---

## 5.6.3 Example B: Spam Loss (Detailed)

```text
Prediction:
Not Spam

Actual:
Spam

Loss:
Classification error detected
```

---

# 5.7 Optimization

This section explains how the model improves after calculating loss.

Optimization reduces loss.

---

## 5.7.1 Step-by-Step Optimization Flow

```text
1. Model makes prediction
2. Loss is calculated
3. Optimization algorithm updates parameters
4. Loss reduces
5. Predictions improve
```

---

## 5.7.2 Example A: House Optimization (Detailed)

```text
Initial prediction:
RM400,000

Actual:
RM500,000

Model updates weights

New prediction:
RM470,000
```

---

# 5.8 Gradient Descent (GD)

This section explains the most common optimization algorithm.

Gradient Descent (GD) moves model parameters toward lower loss.

---

## 5.8.1 Gradient Descent Formula

```text
New Weight = Old Weight - Learning Rate × Gradient
```

---

## 5.8.2 Example A: Walking Downhill Analogy

```text
You are on a mountain

Goal:
Reach lowest point

Gradient:
Shows direction

Learning rate:
Controls step size
```

---

## 5.8.3 Example B: House Price Training

```text
Prediction:
RM450,000

Actual:
RM500,000

Gradient Descent updates model

New prediction:
RM490,000
```

---

# 5.9 Learning Rate

This section explains update speed.

Learning Rate controls how large each update step is.

---

## 5.9.1 Learning Rate Types

| Learning Rate | Behavior | Example | Problem | Result |
| --- | --- | --- | --- | --- |
| Very Small | Slow learning | 0.0001 | Training slow | Stable |
| Balanced | Normal learning | 0.01 | Good balance | Best |
| Very Large | Huge jumps | 1.0 | Unstable training | Dangerous |

---

## 5.9.2 Example A: Small Learning Rate

```text
Loss reduces very slowly

Training takes many hours
```

---

## 5.9.3 Example B: Large Learning Rate

```text
Loss jumps wildly

Model fails to converge
```

---

# 5.10 Epoch

This section explains full dataset training cycles.

One Epoch = one full pass through all training data.

---

## 5.10.1 Example A: Epoch (Detailed)

```text
Dataset:
10,000 rows

Epoch 1:
Model sees all 10,000 rows once

Epoch 2:
Model repeats again
```

---

# 5.11 Batch

This section explains smaller training groups.

A batch is a small chunk of data.

---

## 5.11.1 Batch Types

| Batch Type | Example | Usage | Advantage | Limitation |
| --- | --- | --- | --- | --- |
| Full Batch | All 10,000 rows | Rare | Stable | Slow |
| Mini Batch | 64 rows | Common | Efficient | Most used |
| Small Batch | 16 rows | Small memory | Fast updates | Noisy |

---

## 5.11.2 Example A: Mini Batch

```text
10,000 rows

Batch size:
100

100 rows processed at one time
```

---

# 5.12 Iteration

This section explains individual updates.

One iteration = one batch update.

---

## 5.12.1 Example A: Iteration (Detailed)

```text
10,000 rows
Batch size = 100

Iterations per epoch:
100
```

---

# 5.13 Epoch vs Batch vs Iteration

This section explains their relationship.

| Concept | Meaning | Example | Relationship | Notes |
| --- | --- | --- | --- | --- |
| Epoch | Full dataset pass | 10,000 rows | Largest unit | Contains iterations |
| Batch | Small chunk | 100 rows | Medium unit | Inside epoch |
| Iteration | One update step | One batch | Smallest unit | Updates model |

---

## 5.13.1 Full Example (Detailed)

```text
Dataset:
1,000 rows

Batch size:
100

1 Epoch:
10 iterations
```

---

# 5.14 Training Progress

This section explains model improvement over time.

| Stage | What Happens | Performance | Example | Notes |
| --- | --- | --- | --- | --- |
| Beginning | Random predictions | Poor | Wrong spam labels | Normal |
| Middle | Learns patterns | Improving | Better predictions | Expected |
| Final | Stable performance | Good | Accurate model | Ready for testing |

---

## 5.14.1 Example A: Training Progress (Detailed)

```text
Epoch 1:
Accuracy = 50%

Epoch 20:
Accuracy = 85%

Epoch 50:
Accuracy = 94%
```

---

# 5.15 Common Training Problems

This section explains common issues.

| Problem | Cause | Example | Impact | Solution |
| --- | --- | --- | --- | --- |
| Overfitting | Too much training | Memorizes spam | Poor future prediction | Regularization |
| Underfitting | Weak model | Poor fraud detection | Low accuracy | Better model |
| Slow Training | Small learning rate | Long training time | Delays | Tune learning rate |
| Unstable Training | Large learning rate | Loss jumps | No convergence | Reduce learning rate |

---

## 5.15.1 Example A: Overfitting Problem (Detailed)

```text
Training accuracy:
99%

Testing accuracy:
70%

Problem:
Model memorized training data
```

---

## 5.15.2 Example B: Unstable Training (Detailed)

```text
Loss:
0.5 → 5 → 0.2 → 8

Problem:
Learning rate too high
```

---

# 5.16 End-to-End Example: House Price Model Training

This section connects everything.

| Step | Input | Process | Output | Purpose |
| --- | --- | --- | --- | --- |
| 1 | House features | Input data | Prediction | Start |
| 2 | Compare actual price | Calculate loss | Error | Measure |
| 3 | Optimize model | Update weights | Better prediction | Learn |
| 4 | Repeat epochs | Final model | Accurate predictions | Deployment |

---

## 5.16.1 Full Training Pipeline

```text
Input Data
→ Prediction
→ Compare Actual Output
→ Calculate Loss
→ Optimize
→ Update Parameters
→ Repeat
→ Better Model
```

---

# 5.17 Final Summary

This section summarizes training.

```text
Model learns through mistakes
```

Full learning flow:

```text
Input
→ Prediction
→ Error
→ Loss
→ Optimization
→ Improvement
```
