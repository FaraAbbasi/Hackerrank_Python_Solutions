# **Python Tuples**

## **What is the Problem?**

This problem generally asks us to read an integer n, then read n integers as a list, convert that list to a tuple, and then print the result of the hash() function on that tuple. It tests our understanding of tuples as immutable data structures and the hash() function.

---

## **The Python Code**

```python

if __name__ == '__main__':
    n = int(input())
    integer_list = map(int, input().split())

    # Convert interger list to immutable tuple
    t = tuple(integer_list)

    # Print hash value of tuple
    print(hash(t))

```

---

## **How It Works**

| Step | Code | Explanation |
|------|------|-------------|
| 1 | `n = int(input())` | Read the number of integers (this value is not actually used in the logic, but is required by the problem). |
| 2 | `integer_list = map(int, input().split())` | Read the integers and create a map object (an iterator). |
| 3 | `t = tuple(integer_list)` | Convert the map object into a **tuple**. Tuples are immutable—once created, they cannot be changed. |
| 4 | `print(hash(t))` | Print the hash value of the tuple. Hashing is a way to generate a unique integer for an object. |

---

## **How to Run**

1. Save the code as `tuple.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

   ```bash
   python tuple.py
   ```

4. Enter the number of commands, followed by each command on its own line.

---

## **Sample Example**

**Sample Input:**

```
2
1 2
```

**Process:**

- `n = 2`
- `integer_list = map(int, ['1', '2'])` → `[1, 2]`
- `t = tuple([1, 2])` → `(1, 2)`
- `hash((1, 2))` → some integer (e.g., `3713081631934410656`)

**Output:**

```
3713081631934410656
```

(Note: The exact hash value may vary depending on your Python version and environment. This is python 2 version.)

---

## **Key Concepts Practiced**

- **`map()`** – Applies a function (`int`) to each item in an iterable.
- **`tuple()`** – Creates an immutable tuple from an iterable.
- **`hash()`** – Returns a hash value for an object. In Python, `hash()` can only be called on **immutable** objects like tuples, not on lists.
- **Immutability** – Tuples cannot be changed after creation, making them hashable and suitable as dictionary keys.

---

## **Important Tip**

Always remember that tuples are **immutable**. If you try to modify a tuple after creation, Python will raise a `TypeError`. This immutability allows tuples to be hashed.

---

## **Why This Problem Matters**

This challenge introduces two important Python concepts:

1. **Tuples** – Immutable sequences that are memory-efficient and can be used as dictionary keys.

2. **Hashing** – A fundamental concept in computer science used in dictionaries, sets, and various algorithms.

> Problem origionally from [HackerRank](https://www.hackerrank.com/challenges/python-tuples/problem)

---
