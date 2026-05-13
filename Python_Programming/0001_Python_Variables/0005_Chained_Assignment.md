# Python Lesson — Chained Assignment

---

# 1. What is Chained Assignment?

This section explains what chained assignment means in Python.

Chained Assignment means assigning the same value to multiple variables in a single line.

Instead of writing:

```python
a = 10
b = 10
c = 10
```

Python allows:

```python
a = b = c = 10
```

All variables receive the same value.

---

## 1.1 Basic Definition

This section explains the beginner-friendly meaning.

Chained assignment allows:

- Multiple variables
- Same value
- Single line assignment

Example:

```python
x = y = z = 100
```

Final result:

```python
x = 100
y = 100
z = 100
```

---

## 1.2 Technical Meaning

This section explains what happens internally.

Python evaluates the right side first.

Then assigns that same reference/value to each variable from right to left.

Example:

```python
a = b = c = 10
```

Internal reference:

```text
a → 10
b → 10
c → 10
```

All variables point to the same object/value at assignment time.

---

# 2. Why Chained Assignment is Needed

This section explains why programmers use chained assignment.

Without chained assignment:

```python
width = 100
height = 100
depth = 100
```

With chained assignment:

```python
width = height = depth = 100
```

Benefits:

| Benefit | Explanation |
| --- | --- |
| Less code | Fewer lines |
| Faster assignment | Assign quickly |
| Cleaner syntax | Easier to read |
| Useful for defaults | Common in initialization |

---

# 3. Syntax

This section explains the syntax structure.

General syntax:

```python
var1 = var2 = var3 = value
```

Structure:

| Part | Meaning |
| --- | --- |
| Left side | Multiple variables |
| `=` | Assignment operator |
| Right side | Single shared value |

Example:

```python
a = b = c = 10
```

---

# 4. How Chained Assignment Works Internally

This section explains internal execution.

Example:

```python
a = b = c = 10
```

Step-by-step:

| Step | Process | Explanation |
| --- | --- | --- |
| 1 | Python reads right side | Value `10` |
| 2 | Creates object | Integer object created |
| 3 | Assigns `c → 10` | Rightmost variable first |
| 4 | Assigns `b → 10` | Next variable |
| 5 | Assigns `a → 10` | Final variable |

Final state:

```text
a → 10
b → 10
c → 10
```

---

# 5. Output Flow

This section explains output behavior.

Example:

```python
a = b = c = 10

print(a)
print(b)
print(c)
```

Step-by-step:

| Step | Code | Output |
| --- | --- | --- |
| 1 | Assign values | Variables linked |
| 2 | Print `a` | `10` |
| 3 | Print `b` | `10` |
| 4 | Print `c` | `10` |

Final Output:

```python
10
10
10
```

---

# 6. Chained Assignment with Expressions

This section explains assigning expression results.

Example:

```python
a = b = 3 + 2

print(a)
print(b)
```

Step-by-step:

| Step | Process |
| --- | --- |
| 1 | Evaluate `3 + 2` |
| 2 | Result becomes `5` |
| 3 | Assign to both variables |

Output:

```python
5
5
```

---

# 7. Reassignment After Chained Assignment

This section explains what happens after changing one variable later.

Example:

```python
a = b = 10

a = 20

print(a)
print(b)
```

Step-by-step:

| Step | Result |
| --- | --- |
| Initial | `a → 10`, `b → 10` |
| Reassign `a` | `a → 20` |
| `b` remains | `b → 10` |

Output:

```python
20
10
```

For immutable values:

- Integer
- Float
- String
- Boolean
- Tuple

Changing one later usually does NOT affect others.

---

# 8. Mutable Object Problem (Very Important)

This section explains a major beginner mistake.

Example:

```python
a = b = [1, 2]

a.append(3)

print(a)
print(b)
```

Step-by-step:

| Step | Result |
| --- | --- |
| Create list | `[1,2]` |
| Both variables share same list | Same reference |
| Modify `a` | Original list changes |
| `b` affected too | Same object |

Output:

```python
[1, 2, 3]
[1, 2, 3]
```

Why?

Because both variables point to the SAME list object.

---

## Safer Alternative

```python
a = [1, 2]
b = [1, 2]
```

Now both lists are separate.

---

# 9. Common Chained Assignment Scenarios

This section explains common real-world examples.

---

## 9.1 Initialize Coordinates

```python
x = y = z = 0

print(x, y, z)
```

Output:

```python
0 0 0
```

---

## 9.2 Set Default Game Health

```python
player1 = player2 = player3 = 100
```

Output:

All players start with health `100`

---

## 9.3 Set Default Login Status

```python
user1 = user2 = False
```

Output:

```python
False False
```

---

## 9.4 Initialize Inventory Values

```python
warehouse1 = warehouse2 = warehouse3 = 500
```

Output:

All warehouses start at `500`

---

## 9.5 Assign String Values

```python
a = b = c = "Python"
```

Output:

```python
Python Python Python
```

---

# 10. Common Errors

This section explains beginner mistakes.

---

## 10.1 Invalid Variable Name

Wrong:

```python
1a = b = 10
```

Error:

```python
SyntaxError
```

---

## 10.2 Mutable Object Confusion

Wrong assumption:

```python
a = b = []
```

Many beginners think these are separate lists.

They are NOT.

---

## 10.3 Confusing with Multiple Assignment

Wrong expectation:

```python
a = b = 1, 2
```

This creates:

```python
a → (1,2)
b → (1,2)
```

Not:

```python
a = 1
b = 2
```

Correct multiple assignment:

```python
a, b = 1, 2
```

---

# 11. Real-World Usage

This section explains where chained assignment is used.

| Industry | Example |
| --- | --- |
| Gaming | Initialize players |
| Banking | Default account values |
| Web Development | Default settings |
| Machine Learning | Initialize variables |
| Data Processing | Reset counters |

Example:

```python
pending = approved = rejected = 0
```

---

# 12. Full Workflow

This section explains complete process flow.

Example: Online game initialization

---

## Step 1 Input

```python
player1 = player2 = player3 = 100
```

---

## Step 2 Processing

Players begin game.

---

## Step 3 Output

```python
print(player1)
print(player2)
print(player3)
```

Output:

```python
100
100
100
```

---

## Full Flow

```text
Create Value
→ Chained Assignment
→ Multiple Variables Receive Same Value
→ Processing
→ Output
```

---

# 13. Evaluation Checklist

This section explains how to verify correctness.

| Check | Question |
| --- | --- |
| Same value intended? | All variables should match? |
| Immutable or mutable? | Shared object risk? |
| Correct syntax? | Proper format? |
| Output correct? | Expected values? |
| Better than repeated assignment? | Cleaner code? |

---

# 14. Chained Assignment vs Multiple Assignment

This section compares both concepts.

| Feature | Chained Assignment | Multiple Assignment |
| --- | --- | --- |
| Number of values | One value |
| Multiple variables | Yes |
| Different values allowed | No |
| Common syntax | `a = b = c = 10` |

Multiple Assignment:

| Feature | Value |
| --- | --- |
| Multiple values | Yes |
| Example | `a, b = 1, 2` |

---

# 15. Summary

This section summarizes everything.

| Key Point | Explanation |
| --- | --- |
| Same value assigned | Multiple variables |
| Right-to-left evaluation | Python processes right side first |
| Great for initialization | Common use case |
| Mutable objects risky | Shared references |
| Cleaner code | Reduces repetition |

Final concept:

```text
Single Value
→ Chained Assignment
→ Multiple Variables
→ Processing
→ Output
```

Example:

```python
a = b = c = 10
print(a, b, c)
```

Output:

```python
10 10 10
```
