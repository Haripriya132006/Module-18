# Perform Topological Sorting of a Directed Graph
## 🏁 Aim
To write a C program that performs topological sorting of a directed graph using Kahn’s algorithm and detects cycles which prevent topological ordering.

## 🔍 Algorithm
Represent the graph using an adjacency matrix.

Compute the indegree of all vertices.

Enqueue all vertices with indegree = 0.

Repeat:

Dequeue a vertex and add it to topo_order.

For each neighbor, decrement its indegree.

If indegree becomes 0, enqueue it.

If total visited vertices < n, a cycle exists, and topological sorting fails.

💻 Program
```
//#include<stdio.h>
//#include<stdlib.h>

//#define MAX 6

//int n;    /*Number of vertices in the graph*/
//int adj[MAX][MAX]; /*Adjacency Matrix*/
//void create_graph();

//int queue[MAX], front = -1,rear = -1;
//void insert_queue(int v);
//int delete_queue();
//int isEmpty_queue();

//int indegree(int v);
int main()
{
        int i,v,count,topo_order[MAX],indeg[MAX];

        create_graph();

        /*Find the indegree of each vertex*/
        for(i=0;i<n;i++)
        {
                indeg[i] = indegree(i);
                if( indeg[i] == 0 )
                        insert_queue(i);
        }

        count = 0;
//type your code here...

while(!isEmpty_queue() && count < n)
    {
        v = delete_queue();
        topo_order[count++] = v; /* Add vertex v to topo_order array */

        /* Delete all edges going from vertex v */
        for(i = 0; i < n; i++)
        {
            if(adj[v][i] == 1)
            {
                adj[v][i] = 0;
                indeg[i]--;

                if(indeg[i] == 0)
                    insert_queue(i);
            }
        }
    }

    if(count < n)
    {
        printf("No topological ordering possible, graph contains cycle\n");
        exit(1);
    }

    printf("Topological order is: ");
    for(i = 0; i < count; i++)
        printf("%d ", topo_order[i]);
    printf("\n");

    return 0;
}
```
## 📤 Output
![alt text](image-4.png)
## ✅ Result 
The program successfully implements Kahn’s algorithm to perform topological sorting of a directed graph using an adjacency matrix representation. It calculates the indegree of each vertex, processes nodes in order, and detects the presence of a cycle. If a cycle exists, the program correctly aborts the topological ordering and notifies the user.