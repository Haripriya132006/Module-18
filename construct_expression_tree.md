# Expression Tree in C — Postfix to Infix Conversion
## Aim:
To implement an Expression Tree algorithm in C that converts a given postfix expression into its corresponding infix expression using tree construction and inorder traversal.

## Problem Description:
Given a postfix expression (also called Reverse Polish Notation), the program builds an expression tree and then prints the equivalent infix expression using inorder traversal.

### How it Works:
Operands (numbers/variables) are directly pushed as tree nodes.

Operators trigger creation of internal tree nodes with the last two operands (from the stack) as children.

An inorder traversal of this tree yields the infix expression.

### Input Format:
A single line containing a valid postfix expression (no spaces between characters).

### Output Format:
The infix expression obtained from inorder traversal of the tree.


## Program Code:
```
void construct_expression_tree(char *suffix) {
  //type your code here
   char s;
   struct n *newNode, *p1, *p2;
   int i = 0;

   while ((s = suffix[i]) != '\0') {
      if (r(s) == 1) {
         // Operand: Create a node and push
         newNode = (struct n *)malloc(sizeof(struct n));
         newNode->d = s;
         newNode->l = NULL;
         newNode->r = NULL;
         push(newNode);
      } else if (r(s) == -1) {
         // Operator: Pop two operands and form subtree
         p1 = pop();  // Right child
         p2 = pop();  // Left child
         newNode = (struct n *)malloc(sizeof(struct n));
         newNode->d = s;
         newNode->l = p2;
         newNode->r = p1;
         push(newNode);
      }
      i++;
   }
}

void inOrder(struct n *tree)//perform inorder traversal 
{
   if(tree != NULL) {
      inOrder(tree->l);
      printf("%c",tree->d);
      inOrder(tree->r);
   }
}

int main() {
   
   scanf("%s",pf);
   construct_expression_tree(pf);
   inOrder(a[0]);
   return 0;
}
```

## Output:
![alt text](image-2.png)

## Conclusion:
This program demonstrates how to convert postfix expressions to infix using an expression tree, showcasing stack usage, recursion, and tree construction. It’s a foundational concept in compilers and expression parsing.