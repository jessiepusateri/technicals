# Depth-First Search (DFS)

Start at the root (or other arbitrarily selected node) and explore each branch completely before moving on 
to the next branch. That is, we go deep before we go wide.

DFS is preferred if we want to visit every node in the graph.

Marking visited nodes in not required in graphs without cycles (ex. trees)!

**Time Complexity**: Worst O(|V| + |E|)

**Space**: Worst O(|V|)

## Iterative (HackerEarth)
```python
def DFS_iterative (G, s): # where G is graph and s is source vertex
  stack = []
  stack.append(s) # inserting s in stack 
  visited = set()
  visited.add(s) # mark s as visited
  while stack:
    v = stack.pop() # pop a vertex from stack to visit next
    # Push all the neighbours of v in stack that are not visited   
    for neighbor in all_neighbors_of_v_in_graph_g*:
      if neighbor not in visited:
        stack.append(neighbor)
        visited.add(neighbor) # mark neighbor as visited
```


## Recursive (HackerEarth)
```python
visited = set()
def DFS_recursive(G, s):
    visited.add(s) # mark s as visited
        for neighbor in all_neighbours_of_v_in_graph_g*:
            if neighbor is not visited:
                DFS_recursive(G, neighbor)
```

## Different Variations of all_neighbors_of_v_in_graph_g:

### 2D Matrix
```python
def find_neighbors_w_of_v(graph):
  max_x = len(graph) - 1
  max_y = len(graph[0]) - 1
  
  all_neighbors = []
  
  directions = [[-1,-1],[-1,0],[-1,1],[0,-1],[0,1],[1,-1],[1,0],[1,1]]
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


# Plain Language

1. Pick a starting node and push all of its adjacent nodes into a stack.
2. Pop a node from stack to select the node to visit.
3. Push all its adjacent nodes into a stack.
4. Repeat this process until the stack is empty.

Note: Mark visited nodes in order to avoid infinite loops and visited the same node twice.

# Use Cases (Wikipedia)

- Finding/Counting connected components.
- Topological sorting.
- Finding 2-(edge or vertex)-connected components.
- Finding 3-(edge or vertex)-connected components.
- Finding the bridges of a graph.
- Generating words in order to plot the Limit Set of a Group.
- Finding strongly connected components.
- Planarity testing
- Solving puzzles with only one solution, such as mazes. (DFS can be adapted to find all solutions to a maze by only including nodes on the current path in the visited set.)
- Maze generation may use a randomized depth-first search.
- Finding biconnectivity in graphs.
