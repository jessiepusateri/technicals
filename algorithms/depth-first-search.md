# Depth-First Search (DFS)

Start at the root (or other arbitrarily selected node) and explore each branch completely before moving on 
to the next branch. That is, we go deep before we go wide.

DFS is preferred if we want to visit every node in the graph.

**Time Complexity**: Worst O(|V| + |E|)

**Space**: Worst O(|V|)

## Recursive (CTC)

```python
def search(root):
  if root is None:
    return
  root.visited = true
  for each node in root.adjacent:
    if n.visited == false:
      search(n)
```

## Recursive (Wiki)
```python
def DFS(G,v):
      label v as discovered
      for all edges from v to w in G.adjacentEdges(v) do
          if vertex w is not labeled as discovered then
              recursively call DFS(G,w)
```
              
