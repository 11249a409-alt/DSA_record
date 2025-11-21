Aim: To write a C program to reverse a string using a stack.

Algorithm:
1. Start.
2. Read the input string.
3. Iterate through the string from the first to the last character.
4. Push each character onto the stack.
5. Iterate through the string again from the first to the last character.
6. Pop a character from the stack and place it in the current position of the string.
7. Print the modified (reversed) string.
8. Stop.

#include <stdio.h>
#include <string.h>

#define MAX 100

char stack[MAX];
int top = -1;

void push(char c) {
    if (top == MAX - 1) {
        printf("Stack Overflow\n");
    } else {
        top++;
        stack[top] = c;
    }
}

char pop() {
    if (top == -1) {
        printf("Stack Underflow\n");
        return -1;
    } else {
        return stack[top--];
    }
}

int main() {
    char str[MAX];
    int i;

    printf("Enter a string: ");
    scanf("%s", str);

    for (i = 0; i < strlen(str); i++) {
        push(str[i]);
    }

    for (i = 0; i < strlen(str); i++) {
        str[i] = pop();
    }

    printf("Reversed string: %s\n", str);

    return 0;
}

Output:
Enter a string: hello
Reversed string: olleh

Results: The string reversal program using a stack was successfully implemented and executed.
