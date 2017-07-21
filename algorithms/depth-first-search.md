# Depth-First Search (DFS)

Start at the root (or other arbitrarily selected node) and explore each branch completely before moving on 
to the next branch. That is, we go deep before we go wide.

DFS is preferred if we want to visit every node in the graph.

**Time Complexity**: Worst O(|V| + |E|)

**Space**: Worst O(|V|)

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
    for all_neighbors_w_of_v_in_graph_g*:
      if w is not visited:
        S.push(w)
        visited.add(w) #mark w as visited
```

Different Variations of the neighbors_w_of_v_in_graph_g:

### 2D Matrix
```python
def find_neighbors_w_of_v(2d_graph):
  max_x = len(2d_graph) - 1
  max_y = len(2d_graph[0]) - 1
  
  all_neighbors = []
  
  directions = {{-1,-1,},{-1,0,},{-1,1},{0,-1},{0,1},{1,-1},{1,0},{1,1}}
  for i in len(directions):
    adjacent_x = v.x + directions[i][0]
    adjacent_y = v.y + directions[i][1]
    if adjacent_x >= 0 and adjacent_x <= max_x:
      if adjacent_y >= 0 and adjacent_y <= max_y:
        all_neighbors.append([adjacent_x, adjacent_y])
    
```

### Adjacency List
```python
graph[v]
```

### Binary Tree
```python
[v.left_child, v.right_child]
```

### Node
```python
v.children
```

## Recursive (HackerEarth)
```python
visited = set()

def DFS_recursive(G, s):
    visited.add(s) //mark s as visited
        for all_neighbours_w_of_s in Graph G:
            if w is not visited:
                DFS_recursive(G, w)
```

# Plain Language

1. Pick a starting node and push all of its adjacent nodes into a stack.
2. Pop a node from stack to select the node to visit.
3. Push all its adjacent nodes into a stack.
4. Repeat this process until the stack is empty.

Note: Mark visited nodes in order to avoid infinite loops and visited the same node twice.

# Use Cases
