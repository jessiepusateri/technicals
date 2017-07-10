# Breadth-First Search


## Adjacency List

```javascript
graph = {'A': ['B', 'C'],
         'B': ['A', 'D', 'E'],
         'C': ['A', 'F'],
         'D': ['B'],
         'E': ['B', 'F'],
         'F': ['C', 'E']}
```

```python
def dfs(graph, start):
    visited = set()
    frontier = [start]
    
    while frontier:
        curr = frontier.pop()
        if curr not in visited:
            visited.add(curr)
            for adj in graph[curr]: # get adjacent
                frontier.insert(0, adj)
```

## Node

``` python
def dfs(start):
    visited = set()
    frontier = [start]
    
    while frontier:
        curr = frontier.pop()
        if curr not in visited:
            visited.add(curr)
            for adj in curr.children: # get children
                frontier.insert(0, adj)
```
