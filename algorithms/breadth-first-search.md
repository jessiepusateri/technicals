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
            for adj in graph[curr]:
                frontier.insert(0, adj)
```


