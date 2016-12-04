# interview

As recommended by "Cracking the Coding Interview", I will go into detail descrbing the following material:

Data Structures
* Linked Lists
* Trees, Tries, & Graphs
* Stacks & Queues
* Heaps
* Vectors / ArrayLists
* Hash Tables

[Algorithms](#algorithms)
* Breadth-First Search
* Depth-First Search
* [Binary Search](#binary-search)
* Merge Sort
* Quick Sort

Concepts
* Bit Manipulation
* Memory (Stack vs. Heap)
* Recursion
* Dynamic Programming
* Big O Time & Space

## Algorithms

### Binary Search

Probably the most widely-used algortihm in CS. Whereas searching an array by linear scanning takes O(n) time, binary search takes O(log n) time - the only condition being the array is sorted. The algorithm is as follow:

```python
def binsrch(a, x):
    if len(a) == 0: return 'not found!'
    mid = len(a) / 2
    if x == a[mid]: return 'found!'
    elif x < a[mid]: return binsrch(a[:mid], x)
    elif x > a[mid]: return binsrch(a[mid+1:], x)
```

It's the go-to algortihm for searching sorted arrays.
