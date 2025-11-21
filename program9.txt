Aim: To write a C program to implement a stack using a linked list.

Algorithm:
1. Start.
2. Define a node structure with 'data' and a 'next' pointer.
3. Push Operation:
   a. Create a new node.
   b. Set the new node's 'next' to the current 'top'.
   c. Make the new node the new 'top'.
4. Pop Operation:
   a. Check for stack underflow.
   b. If not empty, make the second node the new 'top' and free the original 'top'.
5. Display Operation:
   a. Check if the stack is empty.
   b. If not empty, traverse from 'top' and print the data of each node.
6. Main Function:
   a. Provide a menu for Push, Pop, Display, and Exit.
   b. Perform the chosen operation.
7. Stop.

#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node *next;
};

struct node *top = NULL;

void push(int val) {
    struct node *new_node = (struct node *)malloc(sizeof(struct node));
    new_node->data = val;
    new_node->next = top;
    top = new_node;
}

void pop() {
    if (top == NULL) {
        printf("Stack Underflow\n");
    } else {
        printf("Popped element: %d\n", top->data);
        struct node *temp = top;
        top = top->next;
        free(temp);
    }
}

void display() {
    if (top == NULL) {
        printf("Stack is empty\n");
    } else {
        struct node *temp = top;
        printf("Stack elements: ");
        while (temp != NULL) {
            printf("%d ", temp->data);
            temp = temp->next;
        }
        printf("\n");
    }
}

int main() {
    int choice, val;
    do {
        printf("\n1. Push\n2. Pop\n3. Display\n4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch (choice) {
            case 1:
                printf("Enter the value to push: ");
                scanf("%d", &val);
                push(val);
                break;
            case 2:
                pop();
                break;
            case 3:
                display();
                break;
            case 4:
                break;
            default:
                printf("Invalid choice\n");
        }
    } while (choice != 4);
    return 0;
}

Output:

1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 1
Enter the value to push: 10

1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 1
Enter the value to push: 20

1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 3
Stack elements: 20 10 

1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 2
Popped element: 20

1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 3
Stack elements: 10 

1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 4

Results: The stack using a linked list program was successfully implemented and executed.
