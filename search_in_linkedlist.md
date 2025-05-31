# 🔍 Linked List Search Function in C
## 📌 Overview
This project demonstrates how to search for a specific element in a singly linked list using the C programming language. It includes the creation of a basic singly linked list and a function to search for any value provided by the user.

## 📂 File Structure
linked_list_search.c – Contains the definition of the linked list, insertion, and search functions.

README.md – Documentation of the project, usage, and implementation details.

## ✅ Features
Insert new elements into a singly linked list.

Search for a specific element in the list.

Display the position of the element if found.

Inform the user if the element is not found.

## 🧠 Code
```
struct Node{
    int data; 
    struct Node *next;
}*head;

void search(int data)
{
    struct Node *temp = head; 
    int position = 1; 

    while (temp != NULL){
        if (temp->data == data){
            printf("item %d found at location %d\n", data, position);
            return;
        }
        temp = temp->next;
        position++; 
    }
    printf("Item not found\n"); 
}

```
## 🖨️ Output:
![alt text](image.png)

## 🚀 How to Run
### Clone or Download this repository.

### Compile the file using a C compiler:

```
gcc linked_list_search.c -o search
```
### Run the executable:

```
./search
```
## 📚 Learning Outcomes
Understand how linked lists work in C.

Learn how to traverse a linked list.

Learn how to search and locate elements dynamically in memory.