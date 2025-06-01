# Binary Search Tree Deletion Program in C
## Aim:
To implement a program in C to delete a node from a Binary Search Tree (BST) and print the resulting inorder traversal of the tree.

## Description:
This program constructs a Binary Search Tree by inserting multiple values, deletes a specific node based on user input, and then displays the tree using an inorder traversal.

## Key Operations:
Insertion: Builds the BST.

Deletion: Removes a specified node while maintaining BST properties.

Inorder Traversal: Displays the BST in sorted order.

### Input Format:
First line: An integer n — number of nodes.

Next n lines: Space-separated integers — node values.

Last line: An integer — value to be deleted from the BST.

### Output Format:
Inorder traversal of the BST after deleting the specified element.

## Program Code:
```
int main()
{
   int n,data;
   struct btnode *root = NULL;
   scanf("%d",&n);
   for(int i=0;i<n;i++)
   {
       scanf("%d",&data);
       root = insert(root, data);
   }

           delete(root);
           inorder(root);
           return 0;
}void inorder(struct btnode *t)
{
   if (t)
  {
    inorder(t->l);
    printf("%d -> ", t->value);
    inorder(t->r);
}
}
 
/* To check for the deleted node */
void delete(struct btnode *root)
{
    int key;
    scanf("%d", &key); // take the key to delete from input
    if (root == NULL) {
        printf("Tree is empty\n");
        return;
    }

    t1 = root;
    search1(root, key);
///only upto this is eniugh i guess 

    // if (flag == 1) {
    //     printf("Node deleted.\n");
    // } else {
    //     printf("Node not found.\n");
    // }
}
```

## Output:
![alt text](image-1.png)
## Conclusion:
This program successfully demonstrates how to:

Build a Binary Search Tree

Delete a node while preserving BST properties

Display the final structure using inorder traversal

The use of recursion and structured functions makes it efficient and easy to understand.