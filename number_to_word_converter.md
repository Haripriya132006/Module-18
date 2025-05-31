# 🔢 Number to Word Converter (71–79)
## 📌 AIM
To write a C program that reads a positive integer and:

Prints the lowercase English word for numbers 71 through 79.

Prints "Greater than 79" if the number is greater than 79.

## 📖 Description
This program takes a positive integer n as input. Based on the value of n:

If n lies between 71 and 79 (inclusive), it prints the corresponding English word in lowercase.

If n is greater than 79, it prints "Greater than 79".

## 🧠 Algorithm
Start the program and declare an integer variable n.

Take input from the user.

Use a switch statement to match the number:

For each case from 71 to 79, print the corresponding word.

For all other numbers (especially greater than 79), use the default case to print "Greater than 79".

## 💻 Program
```
#include <stdio.h>
int main(){
    int n;
    scanf("%d",&n);
    
    switch(n){
        case 71:{
            printf("seventy one");
            break;
        }
        case 72:{
            printf("seventy two");
            break;
        }
        case 73:{
            printf("seventy three");
            break;
        }
        case 74:{
            printf("seventy four");
            break;
        }
        case 75:{
            printf("seventy five");
            break;
        }
        case 76:{
            printf("seventy six");
            break;
        }
        case 77:{
            printf("seventy seven");
            break;
        }
        case 78:{
            printf("seventy eight");
            break;
        }
        case 79:{
            printf("seventy nine");
            break;
        }
        default:{
            printf("Greater than 79");
        }
    }
    

}
```
## 🧪 Sample Input & Output
![alt text](image-1.png)
## ✅ Output Explanation
If the input is 71, the program matches it with the case and prints "seventy one".

If the input is greater than 79, the default case is executed.

## 📋 Constraints
The program assumes input is a positive integer.

It handles values from 71 upward, specifically targeting the 71–79 range.

## 📝 Result
The program correctly displays the English word for numbers between 71 and 79 and handles numbers greater than 79 with appropriate messaging.