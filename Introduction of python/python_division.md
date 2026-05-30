### **Python: Division**

#### **What is this problem?**

This HackerRank problem is based on the basic arithmetic that we already learned. It asks you to take two numbers and divide them in two different ways:

1. **Integer Division (//):** This gives you the whole number part of the quotient, ignoring any remainder.

2. **Float Division (`/`):** This is the "normal" division you're used to, giving you a precise decimal (floating-point) result.

#### **The Problem Statement**

1. Read two integers, a and b.

2. On the first line, print the result of integer division: a // b.

3. On the second line, print the result of float division: a / b.

#### **The Python Code**

```python
# Read two integers from input
a = int(input())
b = int(input())

# Perform and print the two types of division
print(a // b)  # Integer division (gives you the whole number part)
print(a / b)   # Float division (gives you the precise decimal result)
```

#### **How to Run**

1. Save the code as `division.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

   ```bash
   python division.py
   ```

4. Enter two integers when prompted.

#### **Working Exmaple**

Let's use the sample input from HackerRank: `4` and `3`.

**Input:**

```text
4
3
```

**Process:**

* `a = 4`, `b = 3`

* **Integer division (`//`)**: `4 // 3 = 1`. The exact quotient is `1.333...`, but the integer division simply returns the whole number part, `1`.

* **Float division (`/`)**: `4 / 3 = 1.33333333333`. This is the precise result as a decimal number.

**Output:**

```text
1
1.33333333333
```

#### **Key Concept Practiced: The Two Types of Division**

This is the most important part of the problem. Python has two different division operators:

* **`/` (Float Division):** This is the standard division you learn in school. It always returns a floating-point (decimal) number, even if the result is a whole number (e.g., `4 / 2` returns `2.0`, not `2`).

- **`//` (Integer Division):** Think of this as "floor division." It performs the division and then rounds the result down to the nearest whole number, completely discarding any remainder.
  - For example, if you divide 7 slices of pizza among 2 people, integer division would tell you each person gets 3 whole slices, ignoring the leftover slice.

#### **A Note on Division in Python**

Python has two kinds of division. We have the `/` operator that does division with points and the `//` operator that does division without decimal points.

 It is really important to know the difference between the division operators in Python because if you use them incorrectly you will get results and that can cause problems in your code.

  The division operators, in Python are used for many tasks so you need to use the `/` division operator when you want decimal points in your result and use the `//` division operator when you do not want decimal points in your result.

#### **Why This Problem Matters**

* It teaches the critical distinction between integer and floating-point arithmetic.

* It introduces floor division (//), an operator that is extremely useful in programming.

* It emphasizes proper handling of input/output in Python.

> Problem originally from [HackerRank](https://www.hackerrank.com/challenges/python-division/problem).