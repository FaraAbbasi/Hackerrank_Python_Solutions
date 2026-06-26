# **Find the Runner-Up Score!**

## **What is the Problem?**

We are given a list of scores (integers) for a competition. Our task is to find the second largest unique score – the runner-up score. The list can contain duplicates, so we need to ignore them when finding the second highest score.

---

## **The Python Code**

```python

if __name__ == '__main__':
    n = int(input())
    arr = list(map(int, input().split()))
    
    # Remove duplicates, sort in ascending order 
    unique_scores = sorted(set(arr))

    # Pick the second last element
    runner_up = unique_scores[-2]
    
    print(runner_up)

```

---

## **How It Works** 

| Step | Code | Explanation |
|------|------|-------------|
| 1 | `n = int(input())` | Read the number of scores (though we don't actually need `n` for the logic). |
| 2 | `arr = list(map(int, input().split()))` | Read all scores, convert them to integers, and store in a list. |
| 3 | `set(arr)` | Remove duplicate scores using a set. This leaves only unique scores. |
| 4 | `sorted(...)` | Sort the unique scores in ascending order (lowest to highest). |
| 5 | `unique_scores[-2]` | Access the **second last** element, which is the second highest unique score. |
| 6 | `print(runner_up)` | Output the runner-up score. |

---

## **How to Run**

1. Save the code as `runner_up_score.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

   ```bash
   python runner_up_score.py
   ```

4. Enter the number of commands, followed by each command on its own line.


---

## **Sample Example**

**Sample Input:**

```
5
2 3 6 6 5
```

**Process:**

- `arr = [2, 3, 6, 6, 5]`
- `set(arr) = {2, 3, 5, 6}`
- `sorted(...) = [2, 3, 5, 6]`
- `unique_scores[-2] = 5`

**Output:**

```
5
```

---

## **Key Concepts Practiced**

| Concept | Explanation |
|---------|-------------|
| **`set()`** | Removes duplicates from the list, giving only unique scores. |
| **`sorted()`** | Sorts the unique scores in ascending order. |
| **Negative indexing** | `[-2]` accesses the second element from the end. |
| **Chaining methods** | `sorted(set(arr))` is a clean, readable one-liner. |


## **Why This Problem Matters**

This problem is a good example of how to solve a common task in one line of code by using Python's powerful built-in data structures (set and sorted). It teaches us to think about data transformation as a pipeline (convert -> deduplicate -> sort -> access).

> Problem origionally from [HackerRank](https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem)

---