# **Python Lists** 

## **What is this problem?**

In this challenge we will be working with lists. The list is, like a box where we can put things in it and take things out of it. We will start with an empty list and then execute a series of commands that will modify our list. Working with lists is good practice because it helps us get used to doing the things that people do with lists all the time in Python.

---

## **The Problem Statement**

1. We are given an integer `N`. `N` is the number of commands to process.

2. Next to `N` each line has a command. We do what the command says like `insert`, `remove`, `append`.

3. For each command, you must perform the exact list operation.

4. Whenever you see the print command, you output the current state of the list.

---

## **The Python Code**

```python
if __name__ == '__main__':
    N = int(input().strip())
    
    list = []
    
    for _ in range(N):
        command = input().strip().split()
        if command[0] == 'insert':
            list.insert(int(command[1]), int(command[2]))
        elif command[0] == 'print':
            print(list)
        elif command[0] == 'remove':
            list.remove(int(command[1]))
        elif command[0] == 'append':
            list.append(int(command[1]))
        elif command[0] == 'pop':
            list.pop()
        elif command[0] == 'sort':
            list.sort()
        elif command[0] == 'reverse':
            list.reverse()    
```

---

## **How It Works**

**1. Reading Input**

- `N = int(input())` reads the number of commands.  
- The for loop `for _ in range(N):` runs exactly `N` times.

**2. Splitting Each Command**

- `command = input().split()` splits the line into a list of strings.  
- For example, `"insert 0 5"` becomes `["insert", "0", "5"]`.  
- The first element (`command[0]`) is the action, and the rest are arguments.

**3. Executing the Command**

A series of `if-elif` statements decides what to do:

| Command            | Action                                                                         |
| ------------------ | ------------------------------------------------------------------------------ |
| `insert 0 5`       | `my_list.insert(int(command[1]), int(command[2]))` – inserts `5` at index `0`. |
| `print`            | `print(my_list)` – outputs the current list.                                   |
| `remove 5`         | `my_list.remove(int(command[1]))` – deletes the first occurrence of `5`.       |
| `append 5`         | `my_list.append(int(command[1]))` – adds `5` to the end.                       |
| `sort`             | `my_list.sort()` – sorts the list in ascending order.                          |
| `pop`              | `my_list.pop()` – removes and returns the last element.                        |
| `reverse`          | `my_list.reverse()` – reverses the order of the list.                          |

---

## **How to Run**

1. Save the code as `list_operations.py`.
2. Open a terminal in the folder containing the file.
3. Run the command:

   ```bash
   python list_operations.py
   ```

4. Enter the number of commands, followed by each command on its own line.

---

## **Working Example**

Let's use the sample input from HackerRank:

```
12
insert 0 5
insert 1 10
insert 0 6
print
remove 6
append 9
append 1
sort
print
pop
reverse
print
```

Let's see what will happen step by step:

- Start with an empty list: `[]`
- `insert 0 5` → insert 5 at position 0: `[5]`
- `insert 1 10` → insert 10 at position 1: `[5, 10]`
- `insert 0 6` → insert 6 at position 0: `[6, 5, 10]`
- `print` → output `[6, 5, 10]`
- `remove 6` → remove the first occurrence of 6: `[5, 10]`
- `append 9` → add 9 at the end: `[5, 10, 9]`
- `append 1` → add 1 at the end: `[5, 10, 9, 1]`
- `sort` → sort in ascending order: `[1, 5, 9, 10]`
- `print` → output `[1, 5, 9, 10]`
- `pop` → remove the last element (10): `[1, 5, 9]`
- `reverse` → reverse the list: `[9, 5, 1]`
- `print` → output `[9, 5, 1]`

**Sample Output:**

```
[6, 5, 10]
[1, 5, 9, 10]
[9, 5, 1]
```

---

## **Key Concepts Practiced**

1. **Processing multiple commands with a loop**:
 A for loop automates repetition by executing a sequence of instructions exactly `N` times one after the other.

2. **Using `split()` to parse input**: When we get input it comes as one line. The `split()` function breaks it into a list of strings. This makes it easy to get the command and its arguments.

3. **Conditional logic with `if-elif`**: The chain of conditions checks the command name and executes the appropriate list operation.

4. **Essential list methods** – We practiced the most common list operations:
   - `insert(i, e)` – adds an element at a specific position
   - `print(my_list)` – displays the list 
   - `remove(e)` – deletes the first occurrence of an element
   - `append(e)` – adds an element to the end
   - `sort()` – orders the list in ascending order
   - `pop()` – removes the last element
   - `reverse()` – reverses the list order

5. **Type conversion** – Command arguments are read as strings, so we must convert them to integers with `int()` function.

---

## **Why This Problem Matters**

Lists are one of the most versatile and frequently used data structures in Python. This problem forces us to master the basic operations that we'll use in almost every Python program we write.

> Problem originally from [HackerRank](https://www.hackerrank.com/challenges/python-lists/problem).

---