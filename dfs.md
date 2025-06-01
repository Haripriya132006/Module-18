# DFS traversal of the Graph
## 🏁 Aim
Write a C program to traverse a graph using the Depth-First Search (DFS) algorithm starting from a given vertex.

## 🔍 Algorithm
Represent the graph using an adjacency list.

Maintain a visited array to mark which vertices have been visited.

Define the DFS recursive function:

Mark the current vertex as visited.

Print the current vertex.

Recursively call DFS for all its unvisited adjacent vertices.

## 💻 Program
```
/*#include <stdio.h>
#include <stdlib.h>

struct node {
  int vertex;
  struct node* next;
};

struct node* createNode(int v);

struct Graph {
  int numVertices;
  int* visited;

  // We need int** to store a two dimensional array.
  // Similary, we need struct node** to store an array of Linked lists
  struct node** adjLists;
};*/

void DFS(struct Graph* graph, int vertex) {
  //type your code here....
  
  struct node* adjList = graph->adjLists[vertex];
    struct node* temp = adjList;

    graph->visited[vertex] = 1;
    printf("Visited %d\n", vertex);

    while (temp != NULL) {
        int connectedVertex = temp->vertex;

        if (graph->visited[connectedVertex] == 0) {
            DFS(graph, connectedVertex);
        }
        temp = temp->next;
    }
}
```
## 📤 Output
![alt text](image-3.png)
## ✅ Result
The DFS traversal of the graph is correctly performed. Each node is visited in a depth-first manner, starting from the given source vertex and exploring as far as possible before backtracking.