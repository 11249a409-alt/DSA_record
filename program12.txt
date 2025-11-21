Aim: To write a C program to implement BFS tree traversal (Level Order).

Algorithm:
1. Start.
2. Define a node structure for the binary tree.
3. Create a queue and add the root node to it.
4. While the queue is not empty:
   a. Dequeue a node and print its data.
   b. Enqueue the node's left child, if it exists.
   c. Enqueue the node's right child, if it exists.
5. Main Function:
   a. Create a sample binary tree.
   b. Call the level order traversal function and print the results.
6. Stop.

#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node* left;
    struct node* right;
};

struct node* newNode(int data) {
    struct node* node = (struct node*)malloc(sizeof(struct node));
    node->data = data;
    node->left = NULL;
    node->right = NULL;
    return(node);
}

void printLevelOrder(struct node* root) {
    if (root == NULL) return;
    struct node* queue[100];
    int front = 0, rear = 0;
    queue[rear++] = root;
    while (front < rear) {
        struct node* tempNode = queue[front++];
        printf("%d ", tempNode->data);
        if (tempNode->left != NULL)
            queue[rear++] = tempNode->left;
        if (tempNode->right != NULL)
            queue[rear++] = tempNode->right;
    }
}

int main() {
    struct node *root = newNode(1);
    root->left = newNode(2);
    root->right = newNode(3);
    root->left->left = newNode(4);
    root->left->right = newNode(5);

    printf("Level Order traversal of binary tree is \n");
    printLevelOrder(root);
    printf("\n");

    return 0;
}

Output:
Level Order traversal of binary tree is 
1 2 3 4 5 

Results: The BFS tree traversal program was successfully implemented and executed.
