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
    for all_neighbors_w_of_v in Graph G:
      if w is not visited:
        S.push(w)
        visited.add(w) #mark w as visited
```

all_neighbors_w_of_v

find neighbors

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
