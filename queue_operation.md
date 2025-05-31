# 📘 Queue Operations Using Array in C
## 📌 Overview
This program implements a queue data structure using an array in C. It supports four basic operations:

enqueue(data) – Add an element to the rear of the queue.

dequeue() – Remove an element from the front of the queue.

peek() – View the front element of the queue without removing it.

display() – Print all elements currently in the queue from front to rear.

## 💡 Implementation
```
int size=10, queue[50], rear=-1, front=-1;
void enqueue(int data){
    if(front==-1){ 
        front=0;
    }
    queue[++rear]=data;
}

void display(){
    if (front==-1||front>rear){
        printf("No elements to display\n");
        return;
    }
    for (int i=front;i<=rear;i++){
        printf("%d\n",queue[i]);
    }
    
}

void dequeue()
{
    if (front==-1||front>rear){
        printf("Queue Underflow\n");
        return;
    }
    front++;
}

void peek()
{
    printf("%d\n",queue[front]);
}
```
## 🧪 Sample Output
![alt text](image-2.png)


## 📥 How to Run
### Save the code as queue_array.c.

### Compile with a C compiler:
```
gcc queue_array.c -o queue_array
```
### Run the executable:
```
./queue_array
```
## 📚 Features
Fixed-size queue with configurable maximum capacity (size variable).

Handles underflow (empty queue) and overflow (full queue) gracefully.

Supports integer data elements.

Simple and efficient queue operations using arrays.

## 🧠 Learning Objectives
Understand queue implementation basics using arrays.

Learn to manage front and rear pointers effectively.

Handle overflow and underflow conditions correctly.

Implement core queue operations (enqueue, dequeue, peek, and display).

## 📝 Notes
This queue implementation does not support wrap-around (circular queue). For continuous enqueue/dequeue without size limits, consider implementing a circular queue.

Modify the size variable to change maximum queue capacity.