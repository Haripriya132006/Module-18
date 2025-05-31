# 📘 Single Linked List in C – All Operations (Create, Display, Delete, Search)
## 📌 Overview
This project demonstrates the core operations on a Singly Linked List using the C programming language. It includes:

Inserting elements at the end of the list

Displaying all elements

Searching for a specific element

Deleting the first node

## 📂 File Structure
linked_list_operations.c – Contains all the required functions: insert, display, delete, and search.

README.md – Documentation of the project.

✅ Features
✅ Create a singly linked list using dynamic memory allocation

✅ Insert floating-point elements

✅ Display the contents of the list

✅ Search for a specific value

✅ Delete a node from the beginning

✅ Handles edge cases (like empty list)

## 🧠 Code
```
struct Node{
    float data; 
    struct Node *next;
}*head;


void display()
{
    struct Node *temp=head;
    while (temp!=NULL){
        printf("%.2f ",temp->data);
        temp=temp->next;
    }
}

void insert(float data)
{
    struct Node *newnode=(struct Node*)malloc(sizeof(struct Node));
    newnode->data=data;
    newnode->next=NULL;
    if (head==NULL){
        head=newnode;
    }
    else{
        struct Node *temp=head;
        if(temp->next!=NULL){
            temp=temp->next;
        }
        temp->next=newnode;
    }
}


void search(float data)
{
    struct Node *temp=head;
    int pos=1;
    while(temp!=NULL){
        if (temp->data==data){
            printf("item %.2f found at location %d\n",data,pos);
            return;
        }
        temp=temp->next;
        pos++;
    }
    printf("Item not found\n");
}
void delete()
{
    if (head==NULL){
        printf("List is empty\n");
    }
    else{
        struct Node *ptr;
        ptr=head;
        head=ptr->next;
        free(ptr);
        printf("Node deleted from the begining\n");
    }

    
}
```

## 🖨️ Output:
![alt text](image-1.png)
## 🚀 How to Run
### Clone or download the repository.

### Compile using a C compiler:

```
gcc linked_list_operations.c -o list
```
### Run the executable:

```
./list
```
## 📚 Learning Outcomes
Understand how linked lists work in C.

Learn memory allocation and pointer manipulation.

Practice handling edge cases and dynamic structures.

