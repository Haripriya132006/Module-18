# Travelling Salesman Problem (TSP) using C
## 🎯 Aim:
To implement the Travelling Salesman Problem using a heuristic approach in C, finding the minimum cost path visiting all cities exactly once and returning to the starting city.

## 📚 Algorithm:
Initialize all cities as unvisited except the starting city.

Start from the initial city (usually city 0).

From the current city, select the next city that:

Is not yet visited, and

Has the least cost (distance) to travel.

Mark the chosen city as visited and add the cost to the total.

Repeat the process for the newly chosen city.

If all cities are visited, return to the starting city to complete the cycle.

Print the path taken and the minimum total cost.

## 🧾 Program:
```
#include<stdio.h>
int ary[10][10],completed[10],n,cost=0;
void takeInput()
{
int i,j;
scanf("%d",&n);
for(i=0;i < n;i++)
{
for( j=0;j < n;j++)
scanf("%d",&ary[i][j]);
completed[i]=0;
}
}
void mincost(int city)
{
int ncity;
int least(int);
completed[city]=1;
printf("%d--->",city+1);
ncity=least(city);
if(ncity==999)
{
ncity=0;
printf("%d",ncity+1);
cost+=ary[city][ncity];
return;
}
mincost(ncity);
}
int least(int c)
{
int i,nc=999;
int min=999,kmin;
for(i=0;i < n;i++)
{
if((ary[c][i]!=0)&&(completed[i]==0))
if(ary[c][i]+ary[i][c] < min)
{
min=ary[i][0]+ary[c][i];
kmin=ary[c][i];
nc=i;
}
}
if(min!=999)
cost+=kmin;
return nc;
}
int main()
{
takeInput();
mincost(0); //passing 0 because starting vertex
printf("\n\nMinimum cost is %d\n ",cost);
 
return 0;
}

```

## 📤 Output:

![alt text](image-3.png)


## ✅ Result:
The program successfully implements a heuristic method for the Travelling Salesman Problem, finding a path that visits each city once and returns to the starting city with a minimum travel cost. Although this approach may not guarantee the absolute minimum cost for large inputs, it works efficiently for small datasets, demonstrating the core idea of TSP.