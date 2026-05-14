# Python Lesson — Variable Naming & Identifiers

---

# 1. What are Variable Names and Identifiers?

This section explains what variable names and identifiers mean in Python.

A **variable name** is the name used to identify a variable.

An **identifier** is the official programming term for names used to identify things in Python such as:

- Variables
- Functions
- Classes
- Modules
- Objects

For this lesson, we focus on **variable identifiers**.

Example:

```python
age = 20
student_name = "Ali"
```

Explanation:

| Part | Meaning | Explanation |
| --- | --- | --- |
| `age` | Identifier | Name of variable |
| `20` | Value | Stored value |
| `student_name` | Identifier | Name used to access text |
| `"Ali"` | Value | Stored string |

---

## 1.1 Simple Beginner Meaning

This section explains identifiers in beginner-friendly language.

Think of variable names as labels.

Example:

```python
price = 100
```

Real-life analogy:

| Real Object | Label |
| --- | --- |
| Water bottle | "Water" |
| Student file | "Student Record" |
| Product price | `price` |

Without labels:

You won't know what each value means.

---

## 1.2 Technical Meaning

This section explains the technical definition.

An identifier is a valid name recognized by Python.

Python uses identifiers to reference objects stored in memory.

Example:

```python
score = 100
```

Python:

- Reads identifier `score`
- Validates identifier rules
- Creates value `100`
- Links `score → 100`

---

# 2. Why Good Variable Naming is Important

This section explains why naming matters.

Poor names create confusing code.

Bad example:

```python
x = 100
y = 5
z = x * y
print(z)
```

Problem:

What do `x`, `y`, and `z` mean?

---

Better example:

```python
price = 100
quantity = 5
total_price = price * quantity

print(total_price)
```

Output:

```python
500
```

Benefits:

| Benefit | Explanation |
| --- | --- |
| Easier to read | Code explains itself |
| Easier debugging | Easier to find issues |
| Easier teamwork | Others understand code |
| Easier maintenance | Easier future updates |

---

# 3. Syntax of Variable Naming

This section explains how variable names appear in syntax.

General syntax:

```python
variable_name = value
```

Structure:

| Part | Explanation |
| --- | --- |
| Left side | Identifier |
| `=` | Assignment operator |
| Right side | Value |

Example:

```python
student_name = "Ali"
```

---

# 4. How Python Processes Variable Names

This section explains what happens internally.

Example:

```python
score = 100
```

Step-by-step:

| Step | Process | Explanation |
| --- | --- | --- |
| 1 | Python reads `score` | Detects identifier |
| 2 | Checks naming rules | Ensures valid name |
| 3 | Creates value `100` | Integer object created |
| 4 | Links identifier | `score → 100` |
| 5 | Stores reference | Variable ready to use |

Example:

```python
print(score)
```

Output:

```python
100
```

---

# 5. Rules for Variable Naming

This section explains official Python naming rules.

---

## 5.1 Must Start with Letter or Underscore

Correct:

```python
name = "Ali"
_age = 20
```

Wrong:

```python
1name = "Ali"
```

Why wrong?

Python does not allow numbers at the beginning.

---

## 5.2 Cannot Contain Spaces

Correct:

```python
full_name = "Ali"
```

Wrong:

```python
full name = "Ali"
```

Why wrong?

Python treats spaces as separators.

---

## 5.3 Only Letters, Numbers, Underscores Allowed

Correct:

```python
user1 = "Ali"
```

Wrong:

```python
user@ = "Ali"
```

Why wrong?

Special symbols are not allowed.

---

## 5.4 Cannot Use Reserved Keywords

Python keywords have special meanings.

Wrong:

```python
class = 10
```

Correct:

```python
class_name = 10
```

Common keywords:

| Keyword |
| --- |
| `if` |
| `else` |
| `for` |
| `while` |
| `class` |
| `def` |
| `return` |

---

## 5.5 Variable Names Are Case-Sensitive

Python treats uppercase and lowercase differently.

Example:

```python
age = 20
Age = 30

print(age)
print(Age)
```

Output:

```python
20
30
```

---

# 6. Naming Conventions (Best Practices)

This section explains recommended naming styles.

---

## 6.1 Snake Case (Recommended in Python)

Python commonly uses snake_case.

Example:

```python
student_name = "Ali"
total_price = 500
```

Format:

```text
word_word_word
```

---

## 6.2 Camel Case

Less common in Python.

Example:

```python
studentName = "Ali"
```

Format:

```text
wordWordWord
```

---

## 6.3 Pascal Case

Usually used for class names.

Example:

```python
StudentName
```

---

# 7. Good vs Bad Variable Names

This section explains naming quality.

| Bad Name | Good Name | Why Better |
| --- | --- | --- |
| `x` | `price` | More meaningful |
| `a1` | `student_age` | More descriptive |
| `tp` | `total_price` | Easier understanding |
| `n` | `customer_name` | More readable |

Bad example:

```python
x = 100
y = 5
z = x * y
```

Better example:

```python
price = 100
quantity = 5
total_price = price * quantity
```

---

# 8. Valid vs Invalid Identifiers

This section compares valid and invalid names.

| Variable Name | Valid? | Reason |
| --- | --- | --- |
| `user_name` | ✅ | Correct format |
| `_score` | ✅ | Starts with underscore |
| `age1` | ✅ | Number at end allowed |
| `1age` | ❌ | Starts with number |
| `user-name` | ❌ | Hyphen not allowed |
| `full name` | ❌ | Space not allowed |
| `class` | ❌ | Reserved keyword |

---

# 9. Common Naming Scenarios

This section explains real coding situations.

---

## 9.1 Student Information

```python
student_name = "Ali"
student_age = 20
student_score = 90
```

Output:

```python
Ali
20
90
```

---

## 9.2 E-commerce System

```python
product_name = "Laptop"
product_price = 3000
stock_quantity = 20
```

---

## 9.3 Banking System

```python
account_balance = 5000
customer_name = "John"
```

---

## 9.4 Game Development

```python
player_score = 100
player_health = 80
```

---

# 10. Common Naming Errors

This section explains beginner mistakes.

---

## 10.1 Starting With Number

Wrong:

```python
1score = 100
```

Error:

```python
SyntaxError
```

---

## 10.2 Using Spaces

Wrong:

```python
student name = "Ali"
```

Error:

```python
SyntaxError
```

---

## 10.3 Using Special Characters

Wrong:

```python
price$ = 100
```

Error:

```python
SyntaxError
```

---

## 10.4 Using Reserved Keywords

Wrong:

```python
for = 10
```

Error:

```python
SyntaxError
```

---

## 10.5 Using Unclear Names

Bad:

```python
a = 100
b = 5
c = a * b
```

Better:

```python
price = 100
quantity = 5
total_price = price * quantity
```

---

# 11. Real-World Usage

This section explains where naming matters professionally.

| Industry | Example Identifier |
| --- | --- |
| Banking | `account_balance` |
| Healthcare | `patient_name` |
| E-commerce | `product_price` |
| Education | `student_grade` |
| Machine Learning | `training_accuracy` |
| Web Development | `user_email` |

---

# 12. Full Naming Workflow

This section explains proper naming process.

Example: Shopping system

---

## Step 1 Identify data

- Product price
- Quantity
- Discount

---

## Step 2 Create meaningful names

```python
product_price
product_quantity
discount_amount
```

---

## Step 3 Store values

```python
product_price = 100
product_quantity = 5
discount_amount = 20
```

---

## Step 4 Process values

```python
final_price = (product_price * product_quantity) - discount_amount
```

---

## Step 5 Output result

```python
print(final_price)
```

Output:

```python
480
```

---

# 13. Evaluation Checklist

This section explains how to verify good variable naming.

| Check | Question |
| --- | --- |
| Valid syntax | Does it follow naming rules? |
| Meaningful | Does name explain purpose? |
| Readable | Easy to understand? |
| Consistent style | Uses snake_case? |
| No keywords | Avoid reserved words? |

---

# 14. Variable Names vs Identifiers vs Keywords

This section compares important terms.

| Term | Meaning |
| --- | --- |
| Variable Name | Name of a variable |
| Identifier | General name for programmable objects |
| Keyword | Reserved Python word |

Example:

```python
age = 20
```

- `age` → Variable name
- `age` → Identifier
- `if` → Keyword

---

# 15. Summary

This section summarizes everything.

| Key Point | Explanation |
| --- | --- |
| Identifiers name variables | Used to access values |
| Must follow naming rules | Invalid names cause errors |
| Use meaningful names | Makes code readable |
| Snake case preferred | Python standard |
| Avoid keywords | Prevent syntax errors |

Final concept:

```text
Choose Good Name
→ Follow Rules
→ Assign Value
→ Use Variable
→ Improve Readability
```

Example:

```python
student_score = 95
print(student_score)
```

Output:

```python
95
```
