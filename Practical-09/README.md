# Practical 9: Graph Traversal for Campus Navigation Using BFS and DFS

## 1. Problem Statement
To implement graph traversal techniques, Breadth-First Search (BFS) and Depth-First Search (DFS), for a campus navigation system. Buildings are represented as vertices, and paths between buildings are represented as edges. The program creates an adjacency matrix and displays the BFS and DFS traversal sequences from a specified starting building.

## 2. Objectives
- To understand graph representation using an adjacency matrix.
- To represent campus buildings as vertices and paths as edges.
- To implement Breadth-First Search (BFS).
- To implement Depth-First Search (DFS).
- To understand the use of queues, visited arrays, and recursion in graph traversal.

## 3. Data Structure and Concepts Used
- **Graph:** Represents buildings and the paths connecting them.
- **Vertex:** Represents a campus building.
- **Edge:** Represents a path between two buildings.
- **Adjacency Matrix:** A two-dimensional array that represents connections between vertices.
- **BFS:** Visits vertices level by level using a queue.
- **DFS:** Explores an unvisited adjacent vertex recursively before backtracking.
- **Visited Array:** Keeps track of visited vertices to prevent repeated visits.
- **Queue:** Stores vertices waiting to be processed during BFS.
- **Recursion:** Used to implement DFS.

## 4. Algorithm

### A. Create the Graph
1. Accept the number of buildings (`vrtx`) and paths (`edg`).
2. Initialize the adjacency matrix with zeros.
3. Accept the endpoints of each path.
4. Set `arr[x][y] = 1` and `arr[y][x] = 1` to represent an undirected connection.
5. Display the adjacency matrix.

### B. Breadth-First Search (BFS)
1. Initialize all vertices as unvisited.
2. Mark the starting vertex as visited and insert it into the queue.
3. Remove a vertex from the front of the queue and display it.
4. Check all its adjacent vertices.
5. Mark each unvisited adjacent vertex as visited and add it to the queue.
6. Repeat until the queue becomes empty.

### C. Depth-First Search (DFS)
1. Start from the selected vertex.
2. Mark the current vertex as visited and display it.
3. Visit each adjacent unvisited vertex recursively.
4. Continue until no unvisited adjacent vertices remain.
5. Backtrack to explore other available paths.

## 5. Test Cases

| Test Case | Input / Condition | Expected Result |
|---|---|---|
| 1 | Create a graph with 4 buildings and paths (0,1), (0,2), (1,3) | Adjacency matrix displays the connections |
| 2 | Start traversal from vertex 0 | BFS and DFS both begin at vertex 0 |
| 3 | Enter a graph with no paths | Both traversals display only the starting vertex |
| 4 | Use a connected graph | All vertices are visited by both traversals |
| 5 | Use a disconnected graph | Only vertices reachable from the starting vertex are visited |

## 6. Sample Input and Output

**Sample input:**
```text id="a1x5pk"
Enter Number of Buildings: 4
Enter Number of Paths: 3

Enter Path 1 (vertex numbers 0 to 3): 0 1
Enter Path 2 (vertex numbers 0 to 3): 0 2
Enter Path 3 (vertex numbers 0 to 3): 1 3

Enter Starting Building (0 to 3): 0
```

**Sample output:**
```text id="a2v6sk"
Adjacency Matrix for given data:
0 1 1 0
1 0 0 1
1 0 0 0
0 1 0 0

BFS Traversal: 0 1 2 3
DFS Traversal: 0 1 3 2
```

*Note: The traversal order depends on the graph connections and the order in which adjacent vertices are checked. This example matches the ascending vertex-index order used by the program.*

## 7. Time and Space Complexity

Let `V` be the number of vertices (buildings) and `E` be the number of edges (paths).

- **Graph Initialization:** O(V²)
- **Adding Paths:** O(E)
- **Displaying the Adjacency Matrix:** O(V²)
- **BFS:** O(V²) using an adjacency matrix.
- **DFS:** O(V²) using an adjacency matrix.
- **Space Complexity:** O(V²) for the adjacency matrix. BFS also uses O(V) space for its queue and visited array, while DFS uses O(V) auxiliary space for the visited array and recursion stack.

## 8. Conclusion
The campus navigation graph was implemented using an adjacency matrix. BFS was performed using a queue, while DFS was implemented using recursion. Both methods traverse vertices reachable from the selected starting building and demonstrate how graph traversal can be used to explore campus connections.

## Source Code
Refer to [`program.c`](program.c) for the complete implementation.
