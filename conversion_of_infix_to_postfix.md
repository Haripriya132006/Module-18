# Converting Infix Expression to Postfix Expression 
## Aim
Write a C program to convert the infix expression "3%2+4*(A&B)" into postfix form using a stack, following operator precedence and associativity rules.

## Algorithm
Initialize an empty stack to store operators.

Traverse the infix expression character by character.

If the character is an operand (alphanumeric), print it directly.

If the character is an opening parenthesis '(', push it onto the stack.

If the character is a closing parenthesis ')', pop and print from the stack until '(' is encountered; remove '('.

If the character is an operator:

While the operator at the top of the stack has higher or equal precedence, pop and print it.

Push the current operator onto the stack.

After processing the expression, pop and print all remaining operators from the stack.

## Program
```
#include<stdio.h>
#include<ctype.h>

char stack[100];
int top = -1;

void push(char x)
{
    stack[++top]=x;
}

char pop()
{
    if (top==-1){
        return -1;
    }
    return stack[top--];
}
int priority(char x)
{
    if (x=='%') return 5;
    if (x=='&') return 4;
    if (x=='*') return 3;
    if (x=='+') return 2;
    return 0;
}
char IntoPost(char *exp)
{
    char *e,x;
    e = exp;
  while(*e != '\0')
    {
        if(isalnum(*e))
            printf("%c ",*e);
            
        else if(*e == '(')
            push(*e);
            
        else if(*e == ')')
        {
            while((x = pop()) != '(')
                printf("%c ", x);
        }
        
        else
        {
            while(priority(stack[top]) >= priority(*e))
                printf("%c ",pop());
            push(*e);
        }
        e++;
    }
    
    while(top != -1)
    {
        printf("%c ",pop());
    } 
    return 1;
}


int main()
{
    char str[]="3%2+4*(A&B)";
    IntoPost(str);
    return 1;
}

```
## Output
![alt text](image-1.png)
## Result
The program correctly converts the infix expression "3%2+4*(A&B)" to its postfix form following operator precedence and associativity rules.