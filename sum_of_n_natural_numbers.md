# 🧮 Sum of First N Natural Numbers using while Loop
## 📌 AIM
To write a C program to compute the sum of the first N natural numbers using a while loop.

## 📖 Description
Natural numbers are all the positive integers starting from 1 (i.e., 1, 2, 3, …, N). This program takes a positive integer n as input and calculates the sum of all natural numbers from 1 to n using a while loop.

For example:

Input: 5
Output: 15
(Because 1 + 2 + 3 + 4 + 5 = 15)

## 🧠 Algorithm
Start with initializing a counter i = 1 and sum = 0.

Take the input value of n from the user.

Use a while loop:

Continue the loop while i <= n.

In each iteration, add i to sum.

Increment i by 1.

After the loop ends, print the value of sum.

## 💻 Program
```
#include<stdio.h>
int main(){
    int i=1,n,sum=0;
    scanf("%d",&n);
    while (i<=n){
        sum+=i;
        i++;
    }
    printf("%d",sum);
}
```
## 🧪 Sample Input & Output
![alt text](image.png)
## ✅ Output Explanation
The program takes 25 as input.

It sums all natural numbers from 1 to 25.

The result, 325, is printed as the output.

## 📝 Result
Hence, the program successfully calculates the sum of the first N natural numbers using a while loop.

