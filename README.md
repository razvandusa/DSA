# Data Structures and Algorithms in Python

This repository's goal is to help you pass your coding interviews by providing a comprehensive collection of data structures and algorithms.

# Data Structures
1. [Arrays](#arrays)

## Arrays
1. Creating
```python
a = [] # empty array
a = [1, 2, 3] # array with elements
a = [0] * 5 # array with 5 zeros
a = list("abc") # ['a', 'b', 'c']
a = list(range(5)) # [0, 1, 2, 3, 4]
```

2. Access & slicing
```python
a[0], a[-1] # first and last element
a[i:j] # subarray [i, j)
a[i:j:k] # subarray with step k
a[::-1] # reversed array
a[i:j] = [7,8] # replace subarray (can redimension the array)
len(a) # length of the array
```

3. Adding elements
```python
a.append(4) # add to the end
a.extend([5, 6, 7]) # add multiple elements to the end
a += [8, 9] # add multiple elements to the end
a.insert(i, 10) # insert at index i and shift elements to the right
a = a + [11, 12] # create a new array with added elements
```

4. Removing elements
```python
a.pop() # remove & return last element
a.pop(i) # remove & return element at index i
a.remove(3) # remove first occurrence of value 3
del a[i] # remove element at index i
del a[i:j] # remove subarray [i, j)
a.clear() # empty the array
```

5. Searching
```python
x in a # check if x is in the array
a.index(x) # first index of x (raises ValueError if not found)
a.index(x, start, end) # first index of x in the subarray [start, end)
a.count(x) # occurrences of x
min(a) # minimum value
max(a) # maximum value
sum(a) # sum of all elements
```

6. Sorting & reversing
```python
a.sort() # sort in place
a.sort(reverse=True) # sort in descending order
b = sorted(a) # return a new sorted array
a.sort(key=len) # sort by length of elements
a.sort(key=lambda p: p[1]) # sort by second element of each subarray
a.sort(key=lambda p: (p[1], p[0])) # sort by second element, then first
a.reverse() # reverse in place
```

7. Iterating
```python
for x in a: ... # values - when you don't need the index
for i in range(len(a)): ... # index only
for i, x in enumerate(a): ... # index + value
for i, x in enumerate(a, start=1): ... # index starting at 1
for x, y in zip(a, b): ... # iterate over two arrays in parallel - stops at the SHORTER one
for x in reversed(a): ... # iterate in reverse order
for i in range(len(a)-1, -1, -1): ... # iterate in reverse order using index
```

8. Comprehensions
```python
[x * x for x in a] # squares of elements
[x for x in a if x % 2 == 0] # even elements
[x * 2 for x in a if x > 0] # double positive elements
[x if x > 0 else 0 for x in a] # replace negative elements with 0
[(i, x) for i, x in enumerate(a)] # index + value pairs
[[0] * cols for _ in range(rows)] # 2D array of zeros
sum(x for x in a if x > 0) # sum of positive elements
any(x < 0 for x in a) # True if at least one element is negative
all(x < 0 for x in a) # True if all elements are negative
```

9. Unpacking & swapping
```python
a[i], a[j] = a[j], a[i] # swap elements
```

# Algorithms