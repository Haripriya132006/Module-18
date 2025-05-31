## Evaluate the given Postfix Expression
## Aim
Write a C function to evaluate a postfix expression using a stack. The input expression contains only digits, addition (+), and multiplication (*) operators.

Evaluate the postfix expression "231*+9+" and print the output inside the function.

## Algorithm
Initialize an empty stack.

Scan the postfix expression from left to right.

For each character:

If it is a digit, convert it to integer and push it onto the stack.

If it is an operator (+ or *), pop two elements from the stack, apply the operator, and push the result back.

After the expression is fully scanned, the stack contains the final result.

Print the final result.

## Program

```
#include<stdio.h>
#include<ctype.h>
int stack[20];
int top = -1;

void push(int x)
{
    stack[++top] = x;
}

int pop()
{
    return stack[top--];
}

void evalpostfix(char *e)
{
int num1, num2, result;
    
    while (*e)
    {
        if (isdigit(*e)) 
        {
            push(*e - '0'); 
        }
        else 
        {
            num2 = pop();
            num1 = pop();
            
            switch (*e)
            {
                case '+': result = num1 + num2; break;
                case '-': result = num1 - num2; break;
                case '*': result = num1 * num2; break;
                case '/': result = num1 / num2; break;
            }
            push(result);
        }
        e++;
    }
    
    printf("%d\n", pop()); 
}


```

## Output
![alt text](image-3.png)
## Result
The program correctly evaluates the postfix expression "231*+9+" and outputs the result 20.










