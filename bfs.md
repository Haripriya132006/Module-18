# BFS traversal of the graph
## 🏁 Aim
Write a C program to traverse a graph using the Breadth-First Search (BFS) algorithm starting from a given vertex.

## 🔍 Algorithm
Create an adjacency list representation of the graph.

Maintain a visited array to mark visited vertices.

Create a queue for BFS traversal.

Start from the given vertex:

Mark it visited.

Enqueue it.

While the queue is not empty:

Dequeue the front element.

Print the visited vertex.

Enqueue all unvisited adjacent vertices and mark them visited.

## 💻 Program
```
void bfs(struct Graph* graph, int startVertex) {
  struct queue* q = createQueue();
 
  graph->visited[startVertex] = 1;
  enqueue(q, startVertex);
 
  while (!isEmpty(q)) {
    printQueue(q);
    int currentVertex = dequeue(q);
    printf("Visited %d\n ", currentVertex);
   
    struct node* temp = graph->adjLists[currentVertex];
 
    while (temp) {
      int adjVertex = temp->vertex;
 
      if (graph->visited[adjVertex] == 0) {
        graph->visited[adjVertex] = 1;
        enqueue(q, adjVertex);
      }
      temp = temp->next;
    }
  }
}
```

## 📤 Output
![alt text](image-2.png)
## ✅ Result
The BFS traversal of the graph is correctly performed starting from the given vertex. Each node is visited level by level using a queue-based approach.