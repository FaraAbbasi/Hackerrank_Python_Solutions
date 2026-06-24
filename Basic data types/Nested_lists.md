## **Nested Lists**

### **What Is This Problem?**

The "Nested Lists" problem is a classic data-processing challenge where we need to parse student data and find specific information.

We are given the names and grades for each student in a class, and our task is to store them in a nested list and print the name(s) of any student(s) with the second lowest grade. If multiple students share that grade, we must order their names alphabetically.
 
This challenge is the perfect next step after mastering list operations because it introduces nested data structures and combines multiple concepts you've already learned: reading input, using loops, extracting data from a list of lists, working with set to find unique grades, sorting, and filtering.

---

### **The Problem Statement** 

1. We are given the number of students in the class, followed by each student's name and grade.

2. We need to store all this information in a nested list (a list where each entry is itself a list containing `[name, grade]`).

3. Our task is to find the second lowest grade among all students.

4. We have to find the names of students who have this lowest grade. These names need to be sorted in order. Each name should be on a line when we output them. The names of students who have the lowest grade will be listed one, by one.

---

### The Python Code

There are multiple ways to solve this problem. Here is a simple solution that is broken down into easy to follow steps. This solution is straightforward and easy to understand.

```python

students = []
for _ in range(int(input())):
    name = input()
    score = float(input())
    students.append([name, score])
    
# Find the second lowest grade
scores = [student[1] for student in students]  # Extract all grades
unique_scores = sorted(set(scores))            # Get unique grades, sorted
second_lowest = unique_scores[1]               # The second element is second lowest score
    
# Find all students with that grade
result = [student[0] for student in students if student[1] == second_lowest]
    
# Output the names sorted alphabetically
for name in sorted(result):
    print(name)
```

---

### **How It Works** 

Let's break down the code into logical sections, so that it will easy to understand it:

1. **Building the Nested List:**

```python
students = []
for _ in range(int(input())):
    name = input()
    score = float(input())
    students.append([name, score])
```

* `students = []`: Creates an empty list to hold the data.
* `for _ in range(int(input())):`: Asks the user how many students to add and starts a loop that repeats that many times.
* `name = input()`: Reads the student's name from the user.
* `score = float(input())`: Reads the student's grade and converts it into a float.
* `students.append([name, score])`: Saves each pair as a small list inside the main students list.

2. **Finding the Second Lowest Grade:**

```python
scores = [student[1] for student in students]  # Extract all grades
unique_scores = sorted(set(scores))            # Get unique grades, sorted
second_lowest = unique_scores[1]               # The second element is our target
```

* `scores = [student[1] for student in students]`: This uses list comprehension to loop through every student in the students list and extracts the item at index 1 (which represents the grades).

* `unique_scores = sorted(set(scores))`: This removes duplicate grades by converting the list into a set(), then sorts those unique grades in ascending order.

* `second_lowest = unique_scores[1]`: Because Python lists are 0-indexed, this grabs the second value in the sorted, unique list—giving you the second lowest grade.

3. **Collecting the Result:**

```python
result = [student[0] for student in students if student[1] == second_lowest]
```

* This list comprehension iterates over students again, but this time extracts `student[0]` (the name) only when `student[1]` (the grade) matches the second_lowest value.

4. **Printing Alphabetically:**

```python
for name in sorted(result):
    print(name)
```

* We use `sorted(result)` to sort the list of names alphabetically before printing.

* The for loop then prints each name on a new line, which is exactly what the problem requires.

---

### **How to Run**

1. Save the code as `nested_lists.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

    ```bash
    python nested_lists.py
    ```

4. Follow the prompts to enter the number of students, then each student's name and grade.

---
  
### **Example**

**Input:**

```
5
Harry
37.21
Berry
37.21
Tina
37.2
Akriti
41
Harsh
39
```

**Output:**

```
Berry
Harry
```

---

### **Key Concepts Practiced**

| Concept                                                                     | Description                                                                                                    |
| --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Reading multiple lines of input with a `for` loop                          | The loop runs N times, where N is the number of students.                                                      |
| Building nested lists                                                      | Each student is stored as `[name, score]`, and the entire class is a list of these `[name, score]` pairs.     |
| List comprehensions                                                         | `[student[1] for student in students]` extracts grades; `[student[0] for student in students if ...]` filters. |
| Using `set()` to remove duplicates                                          | `set(scores)` collapses the list of grades into a set of unique grades.                                        |
| Sorting with `sorted()`                                                     | `sorted(unique_scores)` sorts the unique grades; `sorted(result)` sorts the names alphabetically.             |
| Conditional filtering in list comprehensions                                | The `if` clause inside the list comprehension filters students by grade.                                      |
| Using `join()` for output (in the compact version)                          | `"\n".join(sorted(names))` combines a list of strings into a single string, each separated by a newline.      |
| Handling floating-point grades                                              | The problem uses `float(input())` to read grades.                                                              |

---

### **Why This Problem Matters**

This challenge is a milestone, as it introduces **nested data structures** (lists of lists) and an important **data processing pipeline**: extract, transform, filter and output. It builds directly on our knowledge from the “Lists” problem and pushes us to write clean, efficient code that gracefully handles real-world edge cases like duplicate grades.

> Problem originally from [HackerRank](https://www.hackerrank.com/challenges/nested-list/problem?isFullScreen=true)

---