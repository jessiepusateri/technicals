# Binary Search Tree

### Time Complexity (Average)

| Function      | Time Complexity    | Space Complexity |
| ------------- |:------------------:|:----------------:|
| Insert        | O(h) - h* is height|                  |
| Search        | O(h)               |                  |
| Delete        |                    |                  |
| Find-Min/Max  |                    |                  |
| Find Successor|                    |                  |

* h is log(n) when the tree is perfectly balanced. The height of a binary search tree can range from lgn to n depending on the order of insertion. On average, the height is log(n).


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
    if self.root:
      res = self._get(key, self.root)
      if res:
        return res.value
      else:
        return None
    else:
      return None
  
  def _search(self, key, curr_node):
    if curr_node is None:
      return None
    if curr_node.key == key:
      return curr_node
    if k > curr_node.key: # current value is smaller
      return search(key, curr_node.right)
    if k < root.key: # current value is higher
      return search(key, curr_node.left)
  
  def delete(self, root, k):
    # case 1: zero children
    # case 2: one child
    # case 3: two children
    
  # the maximum element is the same except that it is the rightmost descendent of the root
  def find_min(self, root):
    if root is None:
      return None
    min = root
    while min.left is not None:
      min = min.left
    return min
  
  def find_successor(self, node):
```

### traversal

Sorted Order: In-order Traversal

Array Order: ???
