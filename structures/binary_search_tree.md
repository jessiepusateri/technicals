# Binary Search Tree

### Time Complexity (Average)

| Function      | Time Complexity   | Space Complexity |
| ------------- |:-----------------:|:----------------:|
| Insert        | O(h) - h is height|                  |
| Search        |                   |                  |
| Delete        |                   |                  |
| Find-Min/Max  |                   |                  |
| Find Successor|                   |                  |


- Insert: O(lg(n))

- Search: O(lg(n)) **OR** O(h) where h denotes the height of the tree.

- Delete: O(lg(n))

### node
```python
class BST_Node:
  def __init__(self, value, parent=None, left=None, right=None):
    self.value = value
    self.parent = parent # optional
    self.left = left
    self.right = right
```

### tree

```python
class BSTree:
  def __init__(self, root=None):
    self.root = None
  
  def insert(l, x, parent):
    if l is None:
      tmp = BST_Node(x, parent, None, None)

  def search(root, k):
    if root is None:
      return None
    if root.value == k:
      return root
    if k > root.value: # current value is smaller
      return search(root.right, k)
    if k < root.value: # current value is higher
      return search(root.left, k)

  ### find-min/find-max
  The maximum element is the same except that it is the rightmost descendent of the root.??

  def find_min(root):
    if root is None:
      return None
    min = root
    while min.left is not None:
      min = min.left
    return min
```

### traversal

Sorted Order: In-order Traversal

Array Order: ???
