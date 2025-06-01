# Delete an Element from an AVL Tree
## 🏁 Aim
Write a C program to delete an element from an AVL Tree.

## 🔍 Algorithm
Read n (number of elements to insert).

Read n elements and insert them into the AVL Tree.

Read the element x to delete.

Perform AVL deletion:

Recursively find and delete the node.

Update the height of the current node.

Calculate the Balance Factor (Bf).

Perform necessary rotations to maintain balance:

LL (Left-Left)

RR (Right-Right)

LR (Left-Right)

RL (Right-Left)

Print the AVL Tree in preorder traversal, showing value(Bf=...) for each node.

## 💻 Program
```
node * Delete(node *T,int x)
{
//type your code here

if (T == NULL) return NULL;

    if (x < T->data)
        T->left = Delete(T->left, x);
    else if (x > T->data)
        T->right = Delete(T->right, x);
    else {
        if (!T->left) return T->right;
        if (!T->right) return T->left;

        node *temp = T->right;
        while (temp->left) temp = temp->left;
        T->data = temp->data;
        T->right = Delete(T->right, temp->data);
    }

    T->ht = height(T);
    int bf = BF(T);

    if (bf > 1) {
        if (BF(T->left) >= 0) return LL(T);
        else return LR(T);
    }
    if (bf < -1) {
        if (BF(T->right) <= 0) return RR(T);
        else return RL(T);
    }

    return T;
}
```
## 📤 Output
![alt text](image.png)
## ✅ Result
The program successfully deletes an element from the AVL Tree while maintaining its balanced property and prints the result in preorder format with balance factors.