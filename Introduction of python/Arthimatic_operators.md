# **Python Arithmetic Operators**

## **What is the problem?**

In this HackerRank problem we have to take two integers (whole numbers) from user and do three basic arithmetic operations:

1. Addition (+)

2. Subtraction (-) 

3. Multiplication ( * )

Then print the results on a new line.

---

## **The Problem Statement**

1. Read two integers, a and b (where 1 ≤ a, b ≤ 10¹⁰).

2. Print the sum of a and b.

3. Print the difference of a and b (first minus second).

4. Print the product of a and b.

---

## **The Python Code**

```python
# Read two integers from input
a = int(input())
b = int(input())

# Perform arithmetic operations
print(a + b)   # addition
print(a - b)   # subtraction
print(a * b)   # multiplication
```

---

## **How It Works (Step by Step)**

* `input()` reads a line of text from the user and returns it as a string.


* The `int()` function converts that string into an integer (whole number).

* `print()` displays the result.

The operations are easy :

* `+` adds two numbers.

* `-` subtracts the second from the first.

* `*` multiplies them

---

## **How to Run**

1. Save the code as `arithmetic_ops.py`.  
2. Open a terminal in the folder containing the file.  
3. Run the command:

   ```bash
   python arithmetic_ops.py
   ```

4. Enter two integers when prompted.

---

### **Working Example:**

**Input:**

```text
3
2
```

**Process:**

* a = 3, b = 2

* a + b = 5

* a - b = 1

* a * b = 6

**Output:**

```text
5
1
6
```

---

## **Why This Problem Matters**

* Teaches basic input/output in Python.
* Introduces integer conversion and arithmetic operators.
* Emphasizes that Python can handle very large integers (up to 10¹⁰) without special treatment.

---

## **Why I Solved This**

This problem helped me get comfortable with basic Python operations and input handling. It’s a small but important step in my coding journey!

> Problem originally from [HackerRank](https://www.hackerrank.com/challenges/python-arithmetic-operators/problem).

---