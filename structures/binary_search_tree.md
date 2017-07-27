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
  def __init__(self, key, value, parent=None, left=None, right=None):
    # REQUIRED
    self.key = key        # what it's sorted by
    self.value = value    # what it's storing (payload)
    # OPTIONAL
    self.parent = parent
    self.left = left
    self.right = right
```

### tree

```python
class BSTree:
  def __init__(self, root=None):
    self.root = None
  
  def insert(self, key, value):
    # first node
    if self.root is None:
      self.root = BST_Node(key, value) # parent is None
    # navigate the tree
    if self.root is not None:
      self._insert(key, value, self.root)
  
  # insert helper
  def _insert(self, key, value, curr_node):
    # insert left
    if key < curr_node.key:
      # go further left
      if curr_node.left is not None:
        self._insert(key,val,curr_node.left)
      # done going left, insert here
      else:
        curr_node.left = BST_Node(key,val,parent=curr_node)
    # insert right
    else:
      # go further right
      if currentNode.right is not None:
        self._insert(key,val,curr_node.right)
      # done going right, insert here
      else:
        curr_node.right = BST_Node(key,val,parent=curr_node)

  def search(self, root, k):
    if root is None:
      return None
    if root.key == k:
      return root
    if k > root.key: # current value is smaller
      return search(root.right, k)
    if k < root.key: # current value is higher
      return search(root.left, k)
  
  def delete(self, root, k):
    
  # the maximum element is the same except that it is the rightmost descendent of the root
  def find_min(self, root):
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
