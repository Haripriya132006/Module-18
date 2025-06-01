# Connect nodes in a Graph using an Adjacency Matrix
## 🏁 Aim
Write a C program to represent a graph using an adjacency matrix. The program takes the number of vertices and edges as input and constructs the matrix accordingly.

## Example Graph
![alt text](image-1.png)
## 🔍 Algorithm
Input the number of vertices V.

Initialize a V x V adjacency matrix with all elements set to 0.

Continuously read edges (e1, e2) until (-1, -1) is entered.

For each valid edge:

Mark adjMatrix[e1][e2] = 1

For undirected graphs, also mark adjMatrix[e2][e1] = 1

Finally, print the adjacency matrix.

## 💻 Program
```
/*#include <stdio.h>
int V;
// Initialize the matrix to zero
void init(int arr[][V]) 
{
  int i, j;
  for (i = 0; i < V; i++)
    for (j = 0; j < V; j++)
      arr[i][j] = 0;
}*/
int main()
{ int e1,e2,me,n,i;
    scanf("%d",&V);
    
    int adjMatrix[V][V];
    init(adjMatrix);
    
    n=V;
    me=n*(n-1)/2;
    
    
    for(i=0;i<=me;i++){
        scanf("%d %d",&e1,&e2);
        addEdge(adjMatrix,e1,e2);
        if((e1==-1)&&(e2==-1)){
            break;
        }
    }
    
    
    printAdjMatrix(adjMatrix);
  //type your code here...
}

```

## 📤 Output
![alt text](image.png)
## ✅ Result
This program successfully constructs and prints the adjacency matrix representation of an undirected graph by accepting user-defined vertices and edges.