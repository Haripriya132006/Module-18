## 📁 Repository Contents
dijkstras_algorithm.md

prims_algorithm.md

kruskals_algorithm.md

travelling_salesman_problem.md

Associated images for visual reference

## 🧭 Algorithms Overview
### 1. Dijkstra's Algorithm
Aim: To find the shortest path from a source node to all other nodes in a weighted graph.

#### Algorithm Steps:

Initialize distances from the source to all vertices as infinite and distance to the source itself as 0.

Set all vertices as unvisited.

For the current vertex, consider all its unvisited neighbors and calculate their tentative distances.

Once all neighbors are considered, mark the current vertex as visited.

Repeat steps 3 and 4 until all vertices are visited.

Program: Implemented in C, utilizing arrays to manage distances and visited status.

Output: Displays the shortest distances from the source to each vertex and the corresponding paths.

Result: Successfully computes the shortest paths in a weighted graph without negative weights.

### 2. Prim's Algorithm
Aim: To find the Minimum Spanning Tree (MST) of a connected, undirected, and weighted graph.

#### Algorithm Steps:

Initialize a tree with a single vertex, chosen arbitrarily from the graph.

Grow the tree by one edge: of the edges that connect the tree to vertices not yet in the tree, find the minimum-weight edge, and transfer the vertex to the tree.

Repeat step 2 until all vertices are included in the tree.

Program: Implemented in C, using adjacency matrices to represent the graph and track the MST.

Output: Lists the edges included in the MST and the total cost.

Result: Effectively constructs the MST with the minimum total edge weight.

### 3. Kruskal's Algorithm
Aim: To find the Minimum Spanning Tree (MST) of a connected, undirected, and weighted graph.

#### Algorithm Steps:

Sort all the edges in non-decreasing order of their weight.

Pick the smallest edge. Check if it forms a cycle with the spanning tree formed so far. If cycle is not formed, include this edge. Else, discard it.

Repeat step 2 until there are (V-1) edges in the spanning tree.

Program: Implemented in C, utilizing Union-Find data structure to detect cycles.

Output: Displays the edges included in the MST and the total cost.

Result: Accurately computes the MST by selecting the least weight edges while avoiding cycles.

### 4. Travelling Salesman Problem (TSP)
Aim: To find the shortest possible route that visits each city exactly once and returns to the origin city.

#### Algorithm Steps:

Start from the initial city.

At each step, visit the nearest unvisited city.

Repeat step 2 until all cities are visited.

Return to the starting city to complete the tour.

Program: Implemented in C, employing a greedy approach to approximate the solution.

Output: Shows the path taken and the total cost of the tour.

Result: Provides an approximate solution to the TSP, suitable for small datasets.

## 📥 Sample Input & Output
Each algorithm's Markdown file contains sample inputs and corresponding outputs to demonstrate functionality.

## ✅ Conclusion
The repository effectively demonstrates the implementation of fundamental graph algorithms in C. Each algorithm is accompanied by clear documentation and sample outputs, making it a valuable resource for understanding graph theory concepts and their practical applications.

