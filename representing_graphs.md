# Representing Graphs

Three things to keep in mind:
- Memory (space) used
- How long it takes to determine whether a given edge is in a graph
- How long it takes to find the neighbors of a given vertex

<p align="center">
          <img src="https://s3.amazonaws.com/ka-cs-algorithms/social_network_num.png">
</p>

## Edge Lists
Array of the |E| edges.

- Space: O(E)
- Edge Lookup: linear search through |E| edges.
- Neighbor Lookup: linear search through |E| edges.

```python
graph = [ [0,1], [0,6], [0,8], [1,4], [1,6], [1,9], [2,4], [2,6], [3,4], [3,5],
          [3,8], [4,5], [4,9], [7,8], [7,9] ]
```

## Adjacency Matrices

A |V| x |V| matrix of Os and 1s, where the entry in row i and column j is 1 if and only if the edge (i, j) is in the graph.

Tip: Replace 1s with the weights and the 0s with null if you want to represent a weighted graph.

- Space:
- Edge Lookup:
- Neighbor Lookup:

```python
graph = [ [0, 1, 0, 0, 0, 0, 1, 0, 1, 0],
          [1, 0, 0, 0, 1, 0, 1, 0, 0, 1],
          [0, 0, 0, 0, 1, 0, 1, 0, 0, 0],
          [0, 0, 0, 0, 1, 1, 0, 0, 1, 0],
          [0, 1, 1, 1, 0, 1, 0, 0, 0, 1],
          [0, 0, 0, 1, 1, 0, 0, 0, 0, 0],
          [1, 1, 1, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 1, 1],
          [1, 0, 0, 1, 0, 0, 0, 1, 0, 0],
          [0, 1, 0, 0, 1, 0, 0, 1, 0, 0] ]
```

## Adjacency Lists

Combines adjacency matrices with edge lists. For each vertex i, store an array of the vertices adjacent to it. Typically, there is an array of |V| adjacency lists, one adjacency list per vertex.

- Space: undirected: 2|E| (each edge appears twice), directed: |E|, one element per directed edge
- Edge Lookup: O(d) where d is the degree of the vertex. Range: 0 - |V| - 1
- Neighbor Lookup: constant time (index into an array)

```python
graph = [ [1, 6, 8],
          [0, 4, 6, 9],
          [4, 6],
          [4, 5, 8],
          [1, 2, 3, 5, 9],
          [3, 4],
          [0, 1, 2],
          [8, 9],
          [0, 3, 7],
          [1, 4, 7] ]
```