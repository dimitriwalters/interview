# interview

As recommended by "Cracking the Coding Interview", I will go into detail descrbing the following material:

[Data Structures](#data-structures)
* Linked Lists
* Trees, Tries, & Graphs
* Stacks & Queues
* Heaps
* Vectors / ArrayLists
* [Hash Tables](#hash-tables)

[Algorithms](#algorithms)
* Breadth-First Search
* Depth-First Search
* [Binary Search](#binary-search)
* Merge Sort
* Quick Sort

[Concepts](#concepts)
* [Bit Manipulation](#bit-manipulation)
* Memory (Stack vs. Heap)
* Recursion
* Dynamic Programming
* Big O Time & Space

## Data Structures

### Hash Tables

Very useful data structure in algorithms - it should probably be the first data structure thought of when designing an algorithm. A hash table is a data structure that maps keys to values, but can be thought of as an array with constant access time to elements. Whereas a normal array would require linear scanning (or binary search if sorted), values are inserted into a fixed index using a *hashing function*. So given a value, one can always find the index of that value in a hash table.

Note: The time complexity is not *exactly* constant. In cases where hashes of two values are the same, called *collisions*, the hash table would have to either expand or have some other type of implementation to deal with it (could use a linked list, or place values in another available spot).

Python dictionaries are implemented as hash tables:

```python
ht = {}
not_ht = []
for i in range(0, 5):
    ht[i] = 1
    not_ht.append(i)
print 4 in ht # constant
print 4 in not_ht # not constant
```

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

## Concepts

### Big Manipulation

Bit Shifting
* Airthmetic shift - dividing a number by two (keep signed bit)
* Logical shift - shifting bits by one (don't keep signed bit)
