# **🔢 List Comprehensions** 

## **What is the Problem?**

We are given three integers `x`, `y`, and `z` representing the dimensions of a cuboid, and an integer `n`. Our task is to generate a list of all possible coordinates `(i, j, k)` on a 3D grid where the sum `i + j + k` is **not equal** to `n`. We must solve this using **list comprehension** (no explicit loops) and print the result.

---

## **The Python Code** 

```python
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
    
    # List comprehension that generates all coordinates where sum is not equal to n
    coordinates = [[i, j, k] for i in range(x+1) for j in range(y+1) for k in range(z+1) if i + j + k != n]
    print(coordinates)
```

---

## **How It Works** 

| Part | Code | Explanation |
|------|------|-------------|
| 1 | `for i in range(x+1)` | Loop over all values from `0` to `x` (inclusive). |
| 2 | `for j in range(y+1)` | Nested loop over all values from `0` to `y`. |
| 3 | `for k in range(z+1)` | Innermost loop over all values from `0` to `z`. |
| 4 | `if i + j + k != n` | Condition that include coordinate only if sum is NOT `n`. |
| 5 | `[i, j, k]` | Create a list for each valid coordinate. |

---

## **How to Run**

1. Save the code as `list_comprehensions.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

   ```bash
   python list_comprehensions.py
   ```

4. Enter the number of commands, followed by each command on its own line.

---

## **Working Example**

**Sample Input:**

```
1
1
1
2
```

**Process:**
All coordinates from `(0,0,0)` to `(1,1,1)` are:
`(0,0,0)`, `(0,0,1)`, `(0,1,0)`, `(0,1,1)`, `(1,0,0)`, `(1,0,1)`, `(1,1,0)`, `(1,1,1)`

We exclude those where `i + j + k == 2`:

- `(0,1,1)` sum = 2 ❌
- `(1,0,1)` sum = 2 ❌
- `(1,1,0)` sum = 2 ❌

**Output:**

```
[[0, 0, 0], [0, 0, 1], [0, 1, 0], [1, 0, 0], [1, 1, 1]]
```

---

### Key Concepts Practiced

- **List comprehensions** – A concise way to create lists using a single line of code.
- **Nested loops in comprehensions** – The for clauses are nested in the same order as the loops.
- **Conditional filtering (`if`)** – Adding a condition to include only specific elements.
- **`range()`** – Using `range(x+1)` to include the endpoint value.

---

## **Same Code approch with Traditional Loops**

To help understand the list comprehension, here's the same logic using standard `for` loops:

```python
coordinates = []
for i in range(x+1):
    for j in range(y+1):
        for k in range(z+1):
            if i + j + k != n:
                coordinates.append([i, j, k])
print(coordinates)
```

---

### Why This Problem Matters

This challenge is our introduction to **list comprehensions*. This is one of Python's most loved features. It allows us to write cleaner, more readable code and it is a skill we'll use constantly in data processing and analysis. The problem also abut nested loops and conditional logic in a concise and elegant syntax.

> Problem originally from [HackerRank](https://www.hackerrank.com/challenges/list-comprehensions/problem)

---