# **Python If-Else**

## **What are if, elif, and else?**

Think of these as decision-makers.

* `if`: This is the first checkpoint. "If this condition is true, do this."

* `elif` (short for "else if"): If the previous `if` was false, you can provide another condition to check. "Otherwise, if this new condition is true, do this instead."

* `else`: This is the catch-all. If none of the previous conditions were true, then do this.

---

## **The Problem Statement**

The task is to write a program that reads a single integer `n` and, based on a set of rules, decides whether the number is "Weird" or "Not Weird".

Here are the rules:

1. If n is odd, it's instantly "Weird".

2. If n is even:

   - If 2 <= n <= 5, it's "Not Weird".

   - If 6 <= n <= 20, it's "Weird".

   - If n > 20, it's "Not Weird".

---

## **The Python Code**

```python
n = int(input().strip())

if n % 2 == 0:
    if n in range(2, 5):
        print('Not Weird')
    elif n in range(6, 21):
        print('Weird')
    elif n > 20:
        print('Not Weird')
else:
    print('Weird')
```

---

## **How to Run**

1. Save the code as `if_else.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

   ```bash
   python if_else.py
   ```

4. Enter an integer when prompted.

---

## **How It Works (Step-by-Step)**

Let's walk through the logic with the given examples.

**Example 1: n = 3 (Odd)**

1. `n` is assigned the value `3`.

2. The first if condition checks if `n` is even. Since `3 % 2` (the remainder) is `1`, it's odd. The condition is `False`.

3. The code moves to the else block and prints "Weird".

**Example 2: n = 4 (Even, in 2-5)**

1. `n` is `4`. The if n % 2 == 0` condition is `True` (it's even).

2. Inside the nested if, we check if `n` is in `range(2, 5)`. The `range (2, 5)` includes the numbers `2, 3, 4`. Since `4` is in that range, this condition is `True`.

3. The code prints "Not Weird".

**Example 3: n = 18 (Even, in 6-20)**

1. `n` is `18`. The outer if condition is `True`.

2. The first nested condition `(n in range(2, 5))` is `False`.

3. The code then checks the `elif n in range(6, 21):` condition. The `range (6, 21)` includes numbers from `6` to `20`. `18` is in that range, so it's `True`.

4. The code prints "Weird".

**Example 4: n = 24 (Even, greater than 20)**

1. `n` is `24`. The outer if condition is `True`.

2. Both `n in range(2, 5)` and `n in range(6, 21)` are `False`.

3. The code then checks the final `elif n > 20:` condition. Since `24 > 20` is `True`, it prints "Not Weird".

---

## **Key Concepts Practiced**

* **`if-elif-else` Statements:** The decision-making backbone of your code, allowing it to take different paths based on conditions.

* **`%` (Modulo) Operator:** A powerful tool that finds the remainder of a division. It's the standard way to check if a number is even `(n % 2 == 0)` or odd `(n % 2 != 0)`.

* `in range()`: A clean, readable way to check if a number falls within a specific, inclusive set of numbers.

* Nested `if` Statements: Placing one `if` statement inside another to create more specific checks.

---

## **Why This Problem Matters**

This challenge introduces conditional logic, one of the most essential concepts in programming. Mastering `if-else` statements allows your code to respond intelligently to different situations.

> Problem originally from [HackerRank](https://www.hackerrank.com/challenges/py-if-else/problem).

---