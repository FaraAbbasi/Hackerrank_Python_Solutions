# **Finding the Percentage**

## **What Is This Problem?**

We are given a dictionary where each student's name is a key and their list of marks is the value. Our task is to look up a student by name, calculate the average of their marks, and print it with exactly two decimal places.

---

## **The Starter Code (provided by HackerRank)**

```python

if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()

```

### **What It Does**

| Step | Code | Explanation |
|------|------|-------------|
| 1 | `n = int(input())` | Read number of students. |
| 2 | `name, *line = input().split()` | Read name and marks. `*line` collects all remaining items into a list of strings. |
| 3 | `scores = list(map(float, line))` | Convert marks from strings to floats. |
| 4 | `student_marks[name] = scores` | Store marks in dictionary with name as key. |
| 5 | `query_name = input()` | reads the student name whose average we need to calculate. |

---

## **The  Solution (the missing code)**

```python

# Get the list of marks for the queried student
marks = student_marks[query_name]

# Calculate the average
total = sum(marks)
n = len(marks)
average = total / n

# Print with 2 decimal places
print(f'{average:.2f}')

```

---

## **How It Works (Step by Step)**

Let's go through with the sample input:

**Input:**

```
3
Krishna 67 68 69
Arjun 70 98 63
Malika 52 56 60
Malika
```

**Step 1: Building the dictionary**

- `student_marks` becomes:

```python
  {   'Krishna': [67.0, 68.0, 69.0],
      'Arjun': [70.0, 98.0, 63.0],
      'Malika': [52.0, 56.0, 60.0]    }
```

**Step 2: Looking up the query**

- `query_name = 'Malika'`
- `marks = student_marks['Malika']` → `[52.0, 56.0, 60.0]`

**Step 3: Calculating the average**

- `total = 52 + 56 + 60 = 168`
- `n = 3`
- `average = 168 / 3 = 56.0`

**Step 4: Formatting the output**

- `f'{average:.2f}'` formats to 2 decimal places → `56.00`

**Output:**

```
56.00
```

---

## **How to Run**

1. Save the code as `finding_the_percenntage.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

   ```bash
   python finding_the_percenntage.py
   ```

4. Enter the number of commands, followed by each command on its own line.

---

### Key Concepts Practiced

| Concept | Explanation |
|---------|-------------|
| **Dictionaries** | Storing data as `{name: [marks]}` pairs for quick lookup. |
| **`*line` (unpacking)** | The `*` collects all remaining items after the name into a list. |
| **`map(float, line)`** | Converts each mark from string to float (handles decimals like `26.5`). |
| **`sum()` & `len()`** | Clean way to calculate the total and count of marks. |
| **f-string formatting** | `f'{average:.2f}'` rounds to exactly 2 decimal places. |

---

### Why This Problem Matters

This challenge is about working with dictionaries and list manipulations, both essential tools in Python. Using *line for unpacking is a convenient trick for handling variable length inputs. It also practices data formatting for clean, professional output.


> Problem from [HackerRank](https://www.hackerrank.com/challenges/finding-the-percentage/problem)

---

That's it! A clean, focused solution to a common real-world task: **calculating averages from stored data**. 😊