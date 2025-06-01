# 📘 Prim's Algorithm in C - Minimum Spanning Tree
This project contains a C program that implements Prim's Algorithm to compute the Minimum Spanning Tree (MST) of a weighted undirected graph and returns the total cost of the tree.

## 📌 Description
Prim's Algorithm is a classic greedy algorithm used to find the Minimum Spanning Tree (MST) for a connected weighted graph. The MST is a subset of the edges that connects all the vertices with the minimum possible total edge weight and no cycles.

## 🛠️ Features
Accepts input as a graph in adjacency matrix form.

Uses a greedy approach to construct MST.

Returns the total cost of the MST.

Includes sample test cases.
## Program: 
## 🔢 Input Format
First line: Number of vertices n

Next n lines: Each line contains n integers representing the adjacency matrix of the graph.

Note:
0 indicates no edge between nodes.
Non-zero entries indicate edge weights.


## 📥  Output
![alt text](image-1.png)
## 💡 Algorithm Highlights
Starts from vertex 0 and adds the smallest weight edge at each step.

Maintains a visited[] array to track vertices already in MST.

Maintains distance[] array to store the minimum weight edge that connects a vertex to the growing MST.

Continues until all vertices are included.

## 🧾 Result 
The program successfully implements Prim's Algorithm to construct a Minimum Spanning Tree (MST) from a given graph using an adjacency matrix. It calculates the total cost of the MST efficiently by greedily selecting the minimum weight edges while ensuring no cycles are formed.