## **Python: Write A Function**

### **What is this problem?**

This HackerRank challenge asks us to write a function that determines whether a given year is a leap year or not. It's a good step up from if-else statements because in this problem we will learn how to package our logic into a reusable block of code, basically a function.

---

### **The Problem Statement**

1. We are given a year (e.g., 1990 or 2000).

2. We need to write a function called is_leap(year) that returns:

   - True if the year is a leap year.

   - False if it's not.

---

### **The Python Code**

```python
def is_leap(year):
    leap = False
    
    if year % 4 == 0:
        leap = True
        if year % 100 == 0:
            leap = False
            if year % 400 == 0:
                leap = True
    
    return leap

year = int(input())
print(is_leap(year))
```

---

### **How It Works (Step by Step)**

**The Three Golden Rules of Leap Years**

The Gregorian calendar uses three specific rules to determine leap years:

1. A year is a leap year if it is **divisible by 4**.

2. However, if the year is **divisible by 100**, it is not a leap year.

3. **Except** if the year is also **divisible by 400** – then it is a leap year.

Here’s we can visualize it:
[Leap year function](Leap_year_function.png)


| Year | Divisible by 4? | Divisible by 100? | Divisible by 400? | Leap Year? |
|------|----------------|-------------------|-------------------|---------------------|
| 1990 | ❌ No | — | — | ❌ **False** |
| 2000 | ✅ Yes | ✅ Yes | ✅ Yes | ✅ **True** |
| 1900 | ✅ Yes | ✅ Yes | ❌ No | ❌ **False** |
| 2024 | ✅ Yes | ❌ No | — | ✅ **True** |


Let's walk through each case:

**Case 1: `year = 1990`**

- `1990 % 4` is **not 0` → `leap` stays `False`.
- Result: **`False`** (not a leap year).

**Case 2: `year = 2000`**

- `2000 % 4 == 0` → `leap = True` (temporarily).
- `2000 % 100 == 0` → `leap = False` (overrides the previous setting).
- `2000 % 400 == 0` → `leap = True` (restores it).
- Result: **`True`** (leap year).

**Case 3: `year = 1900`**

- `1900 % 4 == 0` → `leap = True`.
- `1900 % 100 == 0` → `leap = False`.
- `1900 % 400` is **not 0` → `leap` stays `False`.
- Result: **`False`** (not a leap year).

**Case 4: `year = 2024`**

- `2024 % 4 == 0` → `leap = True`.
- `2024 % 100` is **not 0` → the inner `if` block is skipped.
- Result: **`True`** (leap year).

---

### **Key Concepts Practiced**

**1. Defining a function with `def`**
By defining our own functions we learned how to **create our own reusable block of code** using `def` keyword. Functions let us write logic once and we can use that many times.

**2. Returning a value with `return`**
We used `return leap` to **send the result** (True or False) back to the part of the program that called the function. Without `return`, the function would calculate something but never give us the answer.

**3. Nested `if` statements to implement multi‑level logic**
We placed `if` statements **inside other `if` statements** to handle the leap year rules step by step. This is like a decision tree – each level asks a more specific question (divisible by 4? then by 100? then by 400?).

**4. Using the modulo operator (`%`) to test divisibility**
The `%` operator gives us the **remainder** after division. If `year % 4 == 0`, it means the year divides evenly by 4 (no remainder). This is how we check divisibility in programming.

**5. Working with boolean (`True`/`False`) values**
Booleans are the simplest data type – they represent **yes or no**, **on or off**. Our function returned either `True` (leap year) or `False` (not a leap year). This makes the answer easy to use in other conditions later.

---

### **Why This Problem Matters**

This challenge introduces **functions**, one of the most important building blocks in programming. Instead of writing the same leap‑year logic over and over, you can write it once inside a function and reuse it wherever you need it. It's the first step toward writing clean, modular code.

> Problem originally from [HackerRank](https://www.hackerrank.com/challenges/write-a-function/problem).

---