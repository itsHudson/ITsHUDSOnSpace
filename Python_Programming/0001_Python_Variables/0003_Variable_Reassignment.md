# Python Lesson — Variable Reassignment

---

# 1. What is Variable Reassignment?

This section explains what variable reassignment means in Python.

Variable Reassignment means changing the value of an existing variable.

The variable name remains the same.

The value it refers to changes.

Basic example:

```python
x = 10
x = 20
```

Final value of `x`:

```python
20
```

Why?

Because the second assignment replaces the first value.

---

## 1.1 Assignment vs Reassignment

This section explains the difference between first-time assignment and reassignment.

### Assignment

Creating a variable for the first time.

```python
x = 10
```

Python:

- Creates variable `x`
- Assigns value `10`

---

### Reassignment

Changing an existing variable’s value.

```python
x = 20
```

Python:

- Finds existing variable `x`
- Updates it to new value `20`

---

### Comparison Table

| Feature | Assignment | Reassignment |
| --- | --- | --- |
| Creates variable | Yes | No |
| Updates existing variable | No | Yes |
| First-time creation | Yes | No |
| Replaces old value | No | Yes |

Example:

```python
x = 10   # Assignment
x = 20   # Reassignment
```

---

# 2. Why Variable Reassignment is Needed

This section explains why reassignment is important.

Programs often need updated values.

Examples:

- Updating score
- Updating bank balance
- Updating inventory
- Updating user progress
- Updating calculation results

Without reassignment:

```python
score1 = 50
score2 = 60
score3 = 70
```

This becomes messy.

Better:

```python
score = 50
score = 60
score = 70
```

Benefits:

| Benefit | Explanation |
| --- | --- |
| Updates data easily | Change value anytime |
| Saves memory of naming | No need many variables |
| Cleaner code | Less unnecessary variables |
| Supports dynamic programs | Needed in loops/functions |

---

# 3. Syntax of Reassignment

This section explains reassignment syntax.

General syntax:

```python
existing_variable = new_value
```

Example:

```python
x = 10
x = 20
```

Structure:

| Part | Meaning |
| --- | --- |
| Left side | Existing variable |
| `=` | Reassignment operator |
| Right side | New value/expression |

---

# 4. How Reassignment Works Internally

This section explains what happens behind the scenes.

Example:

```python
x = 10
x = 20
```

Step-by-step:

| Step | Process | Explanation |
| --- | --- | --- |
| 1 | Python creates `10` | First object created |
| 2 | `x → 10` | Variable linked |
| 3 | Python creates `20` | New object created |
| 4 | `x → 20` | Reference updated |
| 5 | Old value unused | `x` no longer points to `10` |

Final result:

```python
x = 20
```

---

# 5. Output Flow

This section explains how output changes after reassignment.

Example:

```python
x = 10
print(x)

x = 20
print(x)
```

Step-by-step:

| Step | Code | Output |
| --- | --- | --- |
| 1 | `x = 10` | Store value |
| 2 | `print(x)` | `10` |
| 3 | `x = 20` | Replace value |
| 4 | `print(x)` | `20` |

Final output:

```python
10
20
```

---

# 6. Reassignment Using Expressions

This section explains updating variables using calculations.

Example:

```python
x = 5
x = x + 2

print(x)
```

Step-by-step:

| Step | Process |
| --- | --- |
| 1 | `x = 5` |
| 2 | Python reads right side first |
| 3 | `x + 2 → 7` |
| 4 | Reassign `x = 7` |

Output:

```python
7
```

Important:

Python evaluates:

Right side first → then updates left side.

---

# 7. Reassign Different Data Types

This section explains Python’s dynamic typing during reassignment.

Python allows changing data types.

Example:

```python
x = 10
print(x)

x = "hello"
print(x)
```

Step-by-step:

| Step | Value Type |
| --- | --- |
| `x = 10` | Integer |
| `x = "hello"` | String |

Output:

```python
10
hello
```

---

# 8. Common Reassignment Scenarios

This section explains common real coding situations.

---

## 8.1 Updating Score

```python
score = 50
score = score + 10

print(score)
```

Output:

```python
60
```

---

## 8.2 Updating Bank Balance

```python
balance = 1000
balance = balance - 200

print(balance)
```

Output:

```python
800
```

---

## 8.3 Updating Shopping Cart Total

```python
total = 100
total = total + 50

print(total)
```

Output:

```python
150
```

---

## 8.4 Updating Game Health

```python
health = 100
health = health - 25

print(health)
```

Output:

```python
75
```

---

## 8.5 Updating User Name

```python
name = "Ali"
name = "John"

print(name)
```

Output:

```python
John
```

---

# 9. Reassignment in Loops

This section explains why reassignment is heavily used in loops.

Example:

```python
total = 0

for i in range(5):
    total = total + i

print(total)
```

Step-by-step:

| Loop Value | Updated Total |
| --- | --- |
| 0 | 0 |
| 1 | 1 |
| 2 | 3 |
| 3 | 6 |
| 4 | 10 |

Output:

```python
10
```

This is extremely common in programming.

---

# 10. Common Errors in Reassignment

This section explains beginner mistakes.

---

## 10.1 Using Variable Before Assignment

Wrong:

```python
print(x)
x = 10
```

Error:

```python
NameError
```

---

## 10.2 Forgetting Existing Variable

Wrong:

```python
x = x + 5
```

If `x` was never created before:

Error:

```python
NameError
```

---

## 10.3 Unexpected Overwriting

```python
name = "Ali"
name = "John"
```

Problem:

Old value is lost.

Final output:

```python
John
```

---

# 11. Real-World Usage

This section explains where reassignment is used in real systems.

| Industry | Example |
| --- | --- |
| Banking | Update balance |
| Gaming | Update player health |
| E-commerce | Update cart total |
| School systems | Update marks |
| Machine Learning | Update training loss |

Example:

```python
cart_total = 500
cart_total = cart_total + 100

print(cart_total)
```

Output:

```python
600
```

---

# 12. Full Reassignment Workflow

This section explains the complete process.

Example: Student marks system

---

## Step 1 Input

```python
marks = 70
bonus = 5
```

---

## Step 2 Processing

```python
marks = marks + bonus
```

---

## Step 3 Output

```python
print(marks)
```

Output:

```python
75
```

---

## Full Flow

```text
Initial Value
→ Reassignment
→ Updated Value
→ Output
```

---

# 13. Evaluation Checklist

This section explains how to verify reassignment is correct.

| Check | Question |
| --- | --- |
| Variable exists first? | Was it assigned earlier? |
| Right side valid? | Correct calculation/value? |
| Correct output? | Expected result? |
| Overwriting intentional? | Old value okay to replace? |
| Proper naming? | Variable understandable? |

---

# 14. Reassignment vs Multiple Assignment

This section compares two concepts.

| Feature | Reassignment | Multiple Assignment |
| --- | --- | --- |
| Updates existing variable | Yes | Sometimes |
| Multiple variables | No | Yes |
| Replaces value | Yes | Yes |
| Common in loops | Very common | Less common |

Example:

Reassignment:

```python
x = 10
x = 20
```

Multiple Assignment:

```python
a, b = 1, 2
```

---

# 15. Summary

This section summarizes everything.

| Key Point | Explanation |
| --- | --- |
| Reassignment updates value | Changes existing variable |
| Old value replaced | New value becomes active |
| Right side runs first | Then left side updates |
| Supports dynamic programs | Very important concept |
| Used everywhere | Loops, apps, systems |

Final concept:

```text
Create Variable
→ Assign Value
→ Update Value
→ Use Latest Value
→ Output
```

Example:

```python
x = 10
x = 20
print(x)
```

Output:

```python
20
```
