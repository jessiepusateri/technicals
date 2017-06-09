# Binary Heap - Extra Functions

### Time Complexity:

- max_heapify:

- build_max_heap: O(log n) where n = heap-size[A] − i
- heap_increase_key:
- heap_sort:
- parent: O(1)
- l_child: O(1)
- r_child: O(1)

### Implementation:
```python
def max_heapify():

# Input: A: an array where the left and right children of i root heaps (but i may not), i: an array index
# Output: A modified so that i roots a heap
# Running Time: O(log n) where n = heap-size[A] − i
def build_max_heap():

def heap_increase_key():

def heap_sort():

# Output: index of parent (if exists)
def parent(A, i):
  if i == 1:
      return None
  else:
     return i / 2

# Output: index of left child (if exists)
def l_child(A, i):
  if (i * 2) > A.current_size:
      return None
  else:
      return i * 2

# Output: index of right child (if exists)
def r_child(A, i):
  if (i * 2 + 1) > A.current_size:
      return None
  else:
      return i * 2 + 1
```
