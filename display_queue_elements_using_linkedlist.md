# 📚 Queue Using Linked List in C (for Float Data)
This project demonstrates how to implement a Queue using a singly linked list in the C programming language to store and manage float values.

## ✅ Aim
To develop a function in C to display all the elements in a queue built using a linked list and to understand how FIFO (First In, First Out) operations work with float values.

## 🧠 Data Structure
```
struct Node {
    float data;
    struct Node *next;
} *front = NULL, *rear = NULL;
```
front points to the first element (head) of the queue.

rear points to the last element (tail) of the queue.

Each node holds a float data and a pointer to the next node.

## 🔧 Function: Display
### 🖨️ void display()
This function prints all the elements in the queue from front to rear.


## 💻 Code
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;

void display()
{
    struct Node *temp = front;
    if (front==NULL){
        printf("queue is empty\n");
        return;
    }
    printf("queue elements:\n");
    while (temp != NULL)
    {
        printf("%.2f\n", temp->data);
        temp = temp->next;
    }
}
```

## ✅ Sample Output
![alt text](image-2.png)
## 📌 Notes
A queue works on a First In First Out (FIFO) basis.

The display function shows how elements are retrieved in the order they were added.

Ensure that front and rear are initialized to NULL at the beginning.

