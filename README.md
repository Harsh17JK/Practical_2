Here is the corrected code for performing set operations like intersection, union, and difference on lists without using NumPy. The indentation and logic are fixed:

```python
# Function to find intersection of two lists
def intersection(l1, l2):
    res = []
    for student in l1:
        if student in l2:
            res.append(student)
    return res

# Function to find union of two lists
def union(l1, l2):
    res = l2.copy()
    for student in l1:
        if student not in l2:
            res.append(student)
    return res

# Function to find difference of two lists (elements in l1 but not in l2)
def diff(l1, l2):
    res = []
    for student in l1:
        if student not in l2:
            res.append(student)
    return res

# List of students playing different sports
a = [1, 2, 3, 4, 5, 6, 7]
b = [2, 3, 6, 7, 9, 10]
c = [2, 4, 6, 8, 10, 12]

# Printing the results of set operations
print(f"A = {a} \nB = {b} \nC = {c} \n")
print(f"a. Intersection of A and B: {intersection(a, b)}")
print(f"b. Difference between the union of A and B, and their intersection: {diff(union(a, b), intersection(a, b))}")
print(f"c. Difference between the difference of C and B, and A: {diff(diff(c, b), a)}")
print(f"d. Difference between the union of A and C, and B: {diff(union(a, c), b)}")
```

### Explanation:
1. **Intersection**: Finds the common elements between two lists.
2. **Union**: Combines all unique elements from two lists.
3. **Difference**: Finds elements in the first list that are not in the second list.

