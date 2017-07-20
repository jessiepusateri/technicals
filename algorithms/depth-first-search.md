# Depth-First Search (DFS)

Start at the root (or other arbitrarily selected node) and explore each branch completely before moving on 
to the next branch. That is, we go deep before we go wide.

DFS is preferred if we want to visit every node in the graph.

Time Complexity: 

```python
def search(root):
  if root is None:
    return
  root.visited = true
  for each node in root.adjacent:
    if n.visited == false:
      search(n)
