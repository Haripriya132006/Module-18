# 🌟 Max of Four Numbers
## 📚 Task
Write a function in C called int max_of_four(int a, int b, int c, int d) that finds the greatest of four numbers.

🚫 Do not use any built-in max() function — you will write your own!

## 🧠 How It Works
The program takes four integers as input (one line each).

It checks which one is the biggest.

It prints the largest number.


## 🧑‍💻 Code
```
#include <stdio.h>

int max_of_four(int a, int b, int c, int d){
    if ((a>b)&&(a>b)&&(a>c)&&(a>d)){
        return a;
    }
    else if((b>c)&&(b>d)){
        return b;
    }
    else if(c>d){
        return c;
    }
    else{
        return d;
    }
    
}
int main(){
    int a,b,c,d;
    scanf("%d %d %d %d",&a,&b,&c,&d);
    printf("%d",max_of_four(a,  b, c,  d));
}
```

## 🧪 Output
![alt text](image.png)
## ✅ What You Learn
📥 How to take input in C

📈 How to compare numbers using if-else

🔁 How to reuse code by writing a function

