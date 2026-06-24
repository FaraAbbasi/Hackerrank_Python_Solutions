# **Python Loops**

## **What is this problem?**

This HackerRank challenge focuses on automating repetitive tasks with loops. Instead of writing the same code multiple times, we write it once and let the loop manage the repetition. In this particular problem, we need to take an integer `n` and print the square of every non-negative integer less than `n` (i.e., `0², 1², 2², …, up to (n-1)²`).

---

## **The Problem Statement**

1. Read a single integer `n` (e.g., 5).

2. For every integer `i` from `0` up to (but not including) `n`:

   - Calculate `i * i` (the square of i).

   - Print the result on a new line.

---

## **The Python Code**

```python
# Read an integer from input
n = int(input())

# Loop through all numbers from 0 to n-1
for i in range(n):
    print(i ** 2)   # i**2 calculates the square of i
```

---

## **How It Works(Step by Step)**

Let’s break down how this works, as if we were the computer itself:

1. **Read the input.** Suppose we enter `5`. The variable `n` becomes `5`.

2. **Start the loop.** The `range(n)` function gives us the sequence `0, 1, 2, 3, 4`.

3. Now, let’s **Repeat the process** for each value of i

    - For `i = 0`: we calculate `0² = 0`, and then print `0`.
    - For `i = 1`: we calculate `1² = 1`, and then print `1`.
    - For `i = 2`: we calculate `2² = 4`, and then print `4`.
    - For `i = 3`: we calculate `3² = 9`, and then print `9`.
    - For `i = 4`: we calculate `4² = 16`, and then print `16`.

3. Once we hit `i = 4`, the loop wraps up automatically.

---

## **How to Run**

1. Save the code as `loops.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

   ```bash
   python loops.py
   ```

4. Enter an integer when prompted.

---

## **Working Example:**

**Input:**

```text
5
```

**Process:**

* The loop runs i = 0, 1, 2, 3, 4.
* It prints i² for each iteration.

**Output:**

```text
0
1
4
9
16
```

---

## **Key Concepts Practiced**

* **`for` loops**: Perfect when you know exactly how many times to repeat an action.

* **`range()`**: A handy function that creates a sequence of numbers (it starts at `0` by default and `stops before the given number`).

* **`**` operator**: Raises a number to a power (e.g., `i ** 2` means `i squared`).

* **Printing in a loop**: Each call to `print()` automatically starts a new line.

---

## **Why This Problem Matters**

This challenge is our first step into **automation**. Instead of writing `print(0)`, `print(1)`, `print(4)`... by hand, we write a few lines of code and let the computer do the boring work for us. That’s the beauty of programming!

> Problem originally from [HackerRank](https://www.hackerrank.com/challenges/python-loops/problem).

---