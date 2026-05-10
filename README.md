# Assignment 4 


Name: Abdirasul Inzhu
Course: SE-2512  

---

<img width="1445" height="1235" alt="Снимок экрана 2026-05-10 172824" src="https://github.com/user-attachments/assets/9dd289a1-b955-4a7e-b906-b084b6977ab8" />


<img width="1428" height="1121" alt="Снимок экрана 2026-05-10 172815" src="https://github.com/user-attachments/assets/b8025053-048e-44ff-a007-3b2b80cce729" />

<img width="1790" height="953" alt="Снимок экрана 2026-05-10 172810" src="https://github.com/user-attachments/assets/51ebad4d-f3a7-4fb5-9d8b-1db13c88ae0d" />

<img width="1560" height="802" alt="Снимок экрана 2026-05-10 172802" src="https://github.com/user-attachments/assets/9cac7663-68e5-4c4a-8036-5eb70108b05d" />


<img width="1909" height="832" alt="Снимок экрана 2026-05-10 172757" src="https://github.com/user-attachments/assets/71b3ce2d-41b8-407c-9fe5-5165fefecd0c" />


<img width="2559" height="1599" alt="Снимок экрана 2026-05-10 172749" src="https://github.com/user-attachments/assets/b20f141b-2731-468d-98e2-61246a1801c9" />
How does graph size affect BFS and DFS performance?

As graph size increases, traversal time also increases because the algorithms need to visit more vertices and edges.

Which traversal was faster?

In this experiment DFS was slightly faster than BFS.

Do the results match O(V + E)?

Yes, the results match the expected complexity because execution time increased proportionally with graph size.

How does graph structure affect traversal order?

Traversal order depends on how vertices are connected in the graph.

Different edge connections produce different traversal paths.

When is BFS preferred over DFS?

BFS is preferred when:

shortest path is needed
level-by-level traversal is required
What are the limitations of DFS?

DFS:

may use more recursion memory
does not guarantee shortest path
can go very deep in large graphs

# Project Overview
.

The graph consists of:
- vertices (nodes)
- edges (connections)

- Breadth-First Search (BFS)
- Depth-First Search (DFS)


---

# Graph Structure

A graph is a data structure that contains:
- Vertices
- Edges

Example:

0 -> 1, 2  
1 -> 0, 3  
2 -> 0, 4


# Classes Description

## Vertex Class

The `Vertex` class represents a graph vertex.

### Fields
- `id` — unique identifier of a vertex

### Methods
- Constructor
- Getter
- `toString()`

### Purpose
This class is used to create graph nodes.

---

## Edge Class

The `Edge` class represents a connection between two vertices.

### Fields
- `source`
- `destination`

### Methods
- Constructor
- Getters
- `toString()`

### Purpose
This class stores information about graph edges.

---

## Graph Class

The `Graph` class stores the graph using an adjacency list.

### Methods
- `addVertex()`
- `addEdge()`
- `printGraph()`
- `bfs()`
- `dfs()`

### Purpose
This class manages graph operations and traversal algorithms.

---

## Experiment Class

The `Experiment` class is responsible for running BFS and DFS traversals and measuring execution time.

### Methods
- `runTraversals()`
- `printResults()`

### Purpose
This class compares traversal performance.


## Description

Breadth-First Search visits graph vertices level by level.

It starts from one vertex and explores all neighboring vertices first.

BFS uses a Queue data structure.

---

## Step-by-Step BFS

1. Start from the first vertex
2. Mark the vertex as visited
3. Add it to the queue
4. Remove a vertex from the queue
5. Visit all unvisited neighbors
6. Repeat until the queue becomes empty

---

## BFS Complexity

O(V + E)

Where:
- V = number of vertices
- E = number of edges

---

## BFS Use Cases

- shortest path search
- social networks
- web crawling
- network broadcasting

---

# Depth-First Search (DFS)

## Description

Depth-First Search visits vertices deeply before backtracking.

DFS uses recursion or a stack.

---

## Step-by-Step DFS

1. Start from a vertex
2. Mark it as visited
3. Visit one neighbor deeply
4. Continue until no unvisited neighbors remain
5. Backtrack
6. Repeat for remaining vertices

---

## DFS Complexity

O(V + E)

Where:
- V = number of vertices
- E = number of edges

---

## DFS Use Cases

- path finding
- cycle detection
- maze solving
- topological sorting

---

# Experimental Results

The program was tested on graphs with:
- 10 vertices
- 30 vertices
- 100 vertices

Execution time was measured using:

```java
long start = System.nanoTime();
long end = System.nanoTime();
