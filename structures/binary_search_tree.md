# Binary Search Tree

### Time Complexity (Average)

- Insert: O(lg(n))

- Search: O(lg(n))
          O(h) where h denotes the height of the tree.

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

### insert
```python

```

### search
```python
def search(root, k):
  if root is None:
    return None
  if root.value == k:
    return root
  if k > root.value: # current value is smaller
    return search(root.right, k)
  if k < root.value: # current value is higher
    return search(root.left, k)
```

### delete
```python

```

### traversal

Sorted Order: In-order Traversal

Array Order: ???
