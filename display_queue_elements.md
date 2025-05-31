# 📘 Display Queue Elements Using Array (C Programming)
## 📌 Overview
This program demonstrates how to implement and display the elements of a queue using an array in C. It includes basic operations like enqueue and display, maintaining the front and rear pointers to track the queue.



## 📂 Code Snippet
```
int queue[50], rear=-1, front=-1,i;
void display()
{
    if (front==-1){
        printf("No elements to display");
    }
    for (i=0;i<=rear;i++){
        printf("%d\n",queue[i]);
    }
}
```

## 🧪 Sample output
![alt text](image.png)
## 🧠 Learning Objectives
Understand queue operations using a static array.

Learn how to use front and rear pointers to manage queue structure.

Implement display() functionality for queues.

## 🛠️ How to Run
### Copy the code into a .c file (e.g., queue_display.c)

### Compile using a C compiler:
```
gcc queue_display.c -o queue_display
```
### Run the executable:

```
./queue_display
```
## 📎 Notes
The queue[] has a fixed size of 50.

This is a simple linear queue and does not include dequeue or circular behavior.

Ensure to reset front and rear appropriately before new test runs.

