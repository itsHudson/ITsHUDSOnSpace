# Python Lesson — Assignment Between Variables (Reference Copy) 

---

# 1. What is Assignment Between Variables?

This section explains what happens when one variable is assigned to another variable.

Assignment Between Variables means assigning an existing variable’s value/reference to another variable.

Example:

```python
a = 10
b = a
```

Meaning:

- `a` already refers to value `10`
- `b = a` makes `b` refer to the same value

Final result:

```python
a → 10
b → 10
```

Output:

```python
print(a)
print(b)
```

Output:

```python
10
10
```

---

## 1.1 Simple Beginner Meaning

This section explains it in an easier way.

Think of it as:

"Take whatever value `a` currently has and assign it to `b`"

Example:

```python
a = 50
b = a
```

Result:

```python
a = 50
b = 50
```

---

## 1.2 Technical Meaning (Reference Copy)

This section explains what actually happens internally.

Python does NOT copy the variable name.

Python copies the reference to the value/object.

Example:

```python
a = 10
b = a
```

Internal behavior:

| Variable | References |
| --- | --- |
| `a` | `10` |
| `b` | `10` |

Both variables point to the same object at that moment.

---

# 2. Why Assignment Between Variables is Needed

This section explains why programmers use this.

Without it:

```python
price = 100
discount_price = 100
```

Problem:

- Repeating values manually
- Hard to maintain
- Easy to make mistakes

Better:

```python
price = 100
discount_price = price
```

Benefits:

| Benefit | Explanation |
| --- | --- |
| Avoid repetition | Reuse existing values |
| Cleaner code | Less duplication |
| Easier updates | Centralized value source |
| Improves readability | Clear relationships |

---

# 3. Syntax

This section explains the syntax structure.

General syntax:

```python
new_variable = existing_variable
```

Structure:

| Part | Meaning |
| --- | --- |
| Left side | New variable |
| `=` | Assignment operator |
| Right side | Existing variable |

Example:

```python
a = 10
b = a
```

---

# 4. How It Works Internally

This section explains what happens step-by-step.

Example:

```python
a = 10
b = a
```

Step-by-step:

| Step | Process | Explanation |
| --- | --- | --- |
| 1 | Create `10` | Integer object created |
| 2 | `a → 10` | `a` references value |
| 3 | Python reads `b = a` | Existing variable used |
| 4 | `b → 10` | `b` points to same value |

Final memory view:

```text
a → 10
b → 10
```

---

# 5. Output Flow

This section explains output behavior.

Example:

```python
a = 10
b = a

print(a)
print(b)
```

Step-by-step:

| Step | Code | Output |
| --- | --- | --- |
| 1 | `a = 10` | Store value |
| 2 | `b = a` | Copy reference |
| 3 | `print(a)` | `10` |
| 4 | `print(b)` | `10` |

Final Output:

```python
10
10
```

---

# 6. Reassignment After Variable Copy

This section explains what happens after changing one variable later.

Example:

```python
a = 5
b = a

a = 10

print(a)
print(b)
```

Step-by-step:

| Step | Result |
| --- | --- |
| `a = 5` | `a → 5` |
| `b = a` | `b → 5` |
| `a = 10` | `a → 10` |
| `b` remains | `b → 5` |

Output:

```python
10
5
```

Important:

For immutable types like:

- Integer
- Float
- String
- Boolean
- Tuple

Changing one variable later usually does NOT affect the other.

---

# 7. Assignment with Mutable Objects

This section explains an important advanced behavior.

Mutable objects can behave differently.

Example with list:

```python
a = [1, 2, 3]
b = a

a.append(4)

print(a)
print(b)
```

Step-by-step:

| Step | Result |
| --- | --- |
| Create list | `[1,2,3]` |
| `a → list` | Reference created |
| `b = a` | Same reference |
| `a.append(4)` | Original list changes |

Output:

```python
[1, 2, 3, 4]
[1, 2, 3, 4]
```

Why?

Both variables point to the SAME list object.

---

# 8. Common Assignment Scenarios

This section explains common real coding examples.

---

## 8.1 Copy Product Price

```python
price = 100
discount_price = price

print(discount_price)
```

Output:

```python
100
```

---

## 8.2 Copy Username

```python
username = "Ali"
backup_username = username

print(backup_username)
```

Output:

```python
Ali
```

---

## 8.3 Copy Calculation Result

```python
total = 500
final_total = total

print(final_total)
```

Output:

```python
500
```

---

## 8.4 Copy Boolean Value

```python
is_active = True
status = is_active

print(status)
```

Output:

```python
True
```

---

## 8.5 Copy List Reference

```python
numbers = [1,2]
backup = numbers

print(backup)
```

Output:

```python
[1, 2]
```

---

# 9. Common Errors

This section explains beginner mistakes.

---

## 9.1 Using Undefined Variable

Wrong:

```python
b = a
```

If `a` does not exist:

Error:

```python
NameError
```

---

## 9.2 Confusing Copy vs Independent Value

Many beginners think this:

```python
a = [1,2]
b = a
```

Creates separate lists.

It does NOT.

They share the same list.

---

## 9.3 Accidentally Modifying Shared List

```python
a = [1,2]
b = a

b.append(3)
```

Output:

```python
a → [1,2,3]
b → [1,2,3]
```

---

# 10. Real-World Usage

This section explains where this concept is used.

| Industry | Example |
| --- | --- |
| E-commerce | Copy pricing |
| Banking | Duplicate balances |
| Gaming | Copy player stats |
| Data Science | Copy datasets |
| Machine Learning | Copy model variables |

Example:

```python
current_balance = 1000
backup_balance = current_balance
```

---

# 11. Full Workflow

This section explains complete process flow.

Example: Shopping system

---

## Step 1 Input

```python
price = 100
```

---

## Step 2 Assignment Between Variables

```python
discount_price = price
```

---

## Step 3 Processing

```python
discount_price = discount_price - 20
```

---

## Step 4 Output

```python
print(price)
print(discount_price)
```

Output:

```python
100
80
```

---

## Full Flow

```text
Create Original Variable
→ Assign to New Variable
→ Process New Variable
→ Output Final Results
```

---

# 12. Evaluation Checklist

This section explains how to verify correctness.

| Check | Question |
| --- | --- |
| Original variable exists? | Created first? |
| Correct assignment? | Used valid variable? |
| Mutable object issue? | Shared reference understood? |
| Output expected? | Correct final result? |
| Reassignment handled? | Logic correct? |

---

# 13. Assignment Between Variables vs Reassignment

This section compares both concepts.

| Feature | Assignment Between Variables | Reassignment |
| --- | --- | --- |
| Uses another variable | Yes |
| Changes existing variable | No | Yes |
| Creates new variable | Usually yes | No |
| May share references | Yes | No |

Example:

Assignment Between Variables:

```python
a = 10
b = a
```

Reassignment:

```python
a = 10
a = 20
```

---

# 14. Summary

This section summarizes everything.

| Key Point | Explanation |
| --- | --- |
| One variable can be assigned to another | Reuse values |
| Python copies references | Not variable names |
| Immutable types behave independently after reassignment | Integers, strings, etc. |
| Mutable objects can share changes | Lists, dictionaries |
| Very common in real programs | Used everywhere |

Final concept:

```text
Original Variable
→ Reference Assignment
→ Shared Value/Object
→ Processing
→ Output
```

Example:

```python
a = 10
b = a

print(a)
print(b)
```

Output:

```python
10
10
```
