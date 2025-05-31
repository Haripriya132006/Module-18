# 📘 Stack Operations Using Array in C
## 📌 Overview
This program implements a stack data structure using an array in C. It includes four essential operations:

push() – Add an element to the top of the stack.

pop() – Remove the top element from the stack.

peek() – View the top element of the stack without removing it.

display() – Print all stack elements from top to bottom.



## 💡 Implementation
```
char stack[100];
int size = 3, top = -1, i;

void push(char ch) {
    if (top >= size - 1) {  
        printf("stack is full\n");
        return;
    }
    stack[++top] = ch;  
}

void pop() {
    top--;  
}

void peek() {
    printf("%c ", stack[top]);
}

void display() {
    if (top == -1) {  
        printf("stack is empty\n");
        return;
    }
    for (i = top; i >= 0; i--) {
        printf("%c ", stack[i]);
    }
}

```

## 📥 How to Run
### Save the code in a file (e.g., stack_array.c)

### Compile using a C compiler:

```
gcc stack_array.c -o stack_array
```
### Run the executable:

```
./stack_array
```
## 📚 Features
Fixed-size stack with maximum capacity (size = 3)

Handles overflow (stack is full) and underflow (stack is empty) cases gracefully

Supports character-based stack elements

## 🧠 Learning Objectives
Understand stack fundamentals using arrays

Implement basic stack operations (push, pop, peek, display)

Learn how to handle edge cases like overflow and underflow
## 🧪 Sample Output
![alt text](image-2.png)
## 🔁 Example Stack Flow
```
push('a') → a
push('e') → e a
push('i') → i e a
peek()    → i
push('o') → stack is full
pop()     → e a
pop()     → a
pop()     → stack is empty
```
## 📝 Notes
You can change size to increase the maximum capacity of the stack.

Make sure to always check for stack overflow/underflow before push/pop.
