# 🧠 Double Linked List – All Basic Operations in C
## 🎯 Aim
To implement all basic operations on a Double Linked List in C:

Insert elements

Display the list

Search for an item

Delete from the beginning of the list

## 📦 What’s a Double Linked List?
A Double Linked List is a chain of elements (nodes), where:

Each node has a number (float)

Each node knows who’s before it and who’s next

You can move forward and backward through the list

```
NULL <- 10.1 <-> 20.2 <-> 30.3 -> NULL
```
## 🔧 Functions
✅ insert(float data)
Adds a number at the end of the list.

✅ display()
Prints all the numbers in the list.

✅ search(float data)
Finds and tells you the position of a number in the list.

✅ delete()
Deletes the first node (from the beginning).
If the list is empty, it says: UNDERFLOW.

## 💻 Full Code
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display()
{
    struct Node *temp=head;
    while(temp!=NULL){
        printf("%.2f ",temp->data);
        temp=temp->next;
    }
    
}

void insert(float data)
{
    struct Node *newnode=(struct Node*)malloc(sizeof(struct Node));
    newnode->data=data;
    newnode->next=NULL;
    
    if(head==NULL){
        head=newnode;
        return;
    }
    struct Node *temp=head;
    while(temp->next!=NULL){
        temp=temp->next;
    }
    temp->next=newnode;
    newnode->prev=temp;
}

void search(float data)
{
    struct Node *temp=head;
    int pos=1;
    while(temp!=NULL){
        if(temp->data==data){
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
        printf("UNDERFLOW\n");
        return;
    }
    struct Node *temp=head;
    head=head->next;
    
    if (head!=NULL){
        head->prev=NULL;

    }
    free(temp);
    printf("Node deleted\n");
}
```

## ✅ Output:
![alt text](image-3.png)
## 📚 Learning Outcome
✅ Understand how a Double Linked List works
✅ Learn to create and manage memory using malloc and free
✅ Practice basic operations: Insert, Search, Display, Delete
✅ Handle special cases like empty list (UNDERFLOW)