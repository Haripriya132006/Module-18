# Priority of Operators in an Expression
## Aim
Write a C program to find and display the priority of the operators in the given postfix expression:

```
"(A*B)^C+(D%H)/F&G"
```
Classify the operators into the following priority categories:

Lowest Priority

Second Lowest Priority

Second Highest Priority

Highest Priority

## Algorithm
Initialize a string containing the postfix expression.

Create a function priority() to return priority values for each operator:

& → Lowest Priority

+ → Second Lowest Priority

*, %, / → Second Highest Priority

^ → Highest Priority

Traverse each character in the expression.

For each operator found, use the priority() function to get its priority.

Print the operator along with its priority category.

Ignore operands and parentheses.

## Program
```
#include <stdio.h>
#include <string.h>

// Function to determine the priority of an operator
int priority(char x) {
    switch (x) {
        case '&': return 1;  // Lowest Priority
        case '+': return 2;  // Second Lowest Priority
        case '*': 
        case '%': 
        case '/': return 3;  // Second Highest Priority
        case '^': return 4;  // Highest Priority
        default: return 0;   // Not an operator
    }
}

int main() {
    char expr[] = "(A*B)^C+(D%H)/F&G";
    int i;
    
    for (i = 0; expr[i] != '\0'; i++) {
        if (priority(expr[i]) > 0) {
            switch (priority(expr[i])) {
                case 1: printf("%c  ----> Lowest Priority\n", expr[i]); break;
                case 2: printf("%c  ----> Second Lowest Priority\n", expr[i]); break;
                case 3: printf("%c  ----> Second Highest Priority\n", expr[i]); break;
                case 4: printf("%c  ----> Highest Priority\n", expr[i]); break;
            }
        }
    }
    
    return 0;
}

```
## Output
![alt text](image.png)
## Result
The program successfully identifies and displays the priority of each operator in the postfix expression as per the classification scheme.