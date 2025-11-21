Aim: To write a C program to convert an infix expression to a postfix expression.

Algorithm:
1. Start.
2. Scan the infix expression from left to right.
3. If the scanned character is an operand, output it.
4. If the scanned character is an operator and the stack is empty or contains a '(' at the top, push the operator onto the stack.
5. If the scanned character is an operator, pop all the operators from the stack which are greater than or equal to in precedence than the scanned operator. After doing that, push the scanned operator to the stack.
6. If the scanned character is a '(', push it to the stack.
7. If the scanned character is a ')', pop and output from the stack until a '(' is encountered.
8. Repeat steps 2 to 7 until the infix expression is scanned.
9. Pop and output from the stack until it is empty.
10. Stop.

#include <stdio.h>
#include <ctype.h>
#include <string.h>

#define MAX 100

char stack[MAX];
int top = -1;

void push(char c) {
    stack[++top] = c;
}

char pop() {
    if (top == -1)
        return -1;
    else
        return stack[top--];
}

int priority(char c) {
    if (c == '(')
        return 0;
    if (c == '+' || c == '-')
        return 1;
    if (c == '*' || c == '/')
        return 2;
    return 0;
}

int main() {
    char exp[MAX];
    char *e, x;
    printf("Enter the infix expression: ");
    scanf("%s", exp);
    e = exp;
    printf("Postfix expression: ");
    while (*e != '\0') {
        if (isalnum(*e))
            printf("%c", *e);
        else if (*e == '(')
            push(*e);
        else if (*e == ')') {
            while ((x = pop()) != '(')
                printf("%c", x);
        } else {
            while (priority(stack[top]) >= priority(*e))
                printf("%c", pop());
            push(*e);
        }
        e++;
    }
    while (top != -1) {
        printf("%c", pop());
    }
    printf("\n");
    return 0;
}

Output:
Enter the infix expression: a+b*c
Postfix expression: abc*+

Results: The infix to postfix conversion program was successfully implemented and executed.
