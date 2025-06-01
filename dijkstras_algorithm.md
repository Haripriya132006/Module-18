# 🛣️ Dijkstra's Algorithm in C
## 🎯 Aim:
To implement Dijkstra's Algorithm in C to find the shortest path and minimum distance from a given start node to all other nodes in a weighted graph.

## 📚 Algorithm:
Initialize distance array with distances from the start node to all other nodes. Set the distance to start node as 0.

Initialize a visited array to keep track of nodes whose shortest distance is finalized.

Initialize a pred[] array to store predecessors of each node to reconstruct the shortest path.

For each iteration:

Select the unvisited node with the smallest tentative distance (nextnode).

Mark it as visited.

Update the distance for all unvisited neighbors of this node by checking if the path through nextnode is shorter.

Repeat until all nodes are visited.

Print the shortest distance and path from the start node to every other node.

## 🧾 Program:
```
void dijkstra(int G[MAX][MAX],int n,int startnode)
{
 
int cost[MAX][MAX],distance[MAX],pred[MAX];
int visited[MAX],count,mindistance,nextnode,i,j;
//pred[] stores the predecessor of each node
//count gives the number of nodes seen so far
//create the cost matrix
for(i=0;i<n;i++)
for(j=0;j<n;j++)
if(G[i][j]==0)
cost[i][j]=INFINITY;
else
cost[i][j]=G[i][j];
//initialize pred[],distance[] and visited[]
for(i=0;i<n;i++)
{
distance[i]=cost[startnode][i];
pred[i]=startnode;
visited[i]=0;
}
distance[startnode]=0;
visited[startnode]=1;
count=1;
while(count<n-1)
{
mindistance=INFINITY;
//nextnode gives the node at minimum distance
for(i=0;i<n;i++)
if(distance[i]<mindistance&&!visited[i])
{
mindistance=distance[i];
nextnode=i;
}
//check if a better path exists through nextnode
visited[nextnode] = 1;

        for(i = 0; i < n; i++)
            if(!visited[i])
                if(mindistance + cost[nextnode][i] < distance[i])
                {
                    distance[i] = mindistance + cost[nextnode][i];
                    pred[i] = nextnode;
                }

        count++;
    }

// Text your code here
 
//print the path and distance of each node
for(i=0;i<n;i++)
if(i!=startnode)
{
printf("Distance of node%d=%d\n",i,distance[i]);
printf("Path=%d",i);
j=i;
do
{
j=pred[j];
printf("<-%d",j);
}while(j!=startnode);
}
}
```

## 📤 Output:
![alt text](image-2.png)

## ✅ Result / Conclusion:
The program correctly computes the shortest distances from the start node to all other nodes using Dijkstra's Algorithm. It efficiently tracks the minimum distance and reconstructs the path taken for each node, demonstrating the algorithm's greedy approach to solving shortest path problems in weighted graphs without negative edges.