# Binary Tree Traversal

In-Order, Post-Order, and Pre-Order Traversal

Time Complexity:

- in_order: O(n)

- pre_order: O(n)

- post_order: O(n)

Running time is O(n) where n is the number of elements in the tree because it traverses the entire tree.


```python
class Node():
    def __init__(self, val, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right


class BinaryTreeTraversal():
    def visit(self, node):
        print node.val

    def in_order(self, node):
        if node is not None:
            self.in_order(node.left)
            self.visit(node)
            self.in_order(node.right)

    def pre_order(self, node):
        if node is not None:
            self.visit(node)
            self.pre_order(node.left)
            self.pre_order(node.right)

    def post_order(self, node):
        if node is not None:
            self.post_order(node.left)
            self.post_order(node.right)
            self.visit(node)
```
