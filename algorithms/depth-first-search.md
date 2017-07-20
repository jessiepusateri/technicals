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

## Iterative (HackerEarth)
```python
def DFS_iterative (G, s):                                   //Where G is graph and s is source vertex
  S = Stack()
  S.push(s) # inserting s in stack 
  visited = set()
  visited.add(s) # mark s as visited
  while (S is not empty):
    v = S.pop( ) # pop a vertex from stack to visit next
    //Push all the neighbours of v in stack that are not visited   
    for all neighbours w of v in Graph G:
      if w is not visited:
        S.push(w)
        visited.add(w) #mark w as visited
```

# Recursive (HackerEarth)
```python
visited = set()

def DFS_recursive(G, s):
    visited.add(s) //mark s as visited
        for all neighbours w of s in Graph G:
            if w is not visited:
                DFS-recursive(G, w)
```
