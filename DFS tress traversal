Aim: To write a C program to implement DFS tree traversals (Inorder, Preorder, Postorder).

Algorithm:
1. Start.
2. Define a node structure for the binary tree.
3. Preorder Traversal:
   a. Visit the root.
   b. Traverse the left subtree.
   c. Traverse the right subtree.
4. Inorder Traversal:
   a. Traverse the left subtree.
   b. Visit the root.
   c. Traverse the right subtree.
5. Postorder Traversal:
   a. Traverse the left subtree.
   b. Traverse the right subtree.
   c. Visit the root.
6. Main Function:
   a. Create a sample binary tree.
   b. Call the traversal functions and print the results.
7. Stop.

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

void printPostorder(struct node* node) {
    if (node == NULL)
        return;
    printPostorder(node->left);
    printPostorder(node->right);
    printf("%d ", node->data);
}

void printInorder(struct node* node) {
    if (node == NULL)
        return;
    printInorder(node->left);
    printf("%d ", node->data);
    printInorder(node->right);
}

void printPreorder(struct node* node) {
    if (node == NULL)
        return;
    printf("%d ", node->data);
    printPreorder(node->left);
    printPreorder(node->right);
}

int main() {
    struct node *root = newNode(1);
    root->left = newNode(2);
    root->right = newNode(3);
    root->left->left = newNode(4);
    root->left->right = newNode(5);

    printf("Preorder traversal of binary tree is \n");
    printPreorder(root);

    printf("\nInorder traversal of binary tree is \n");
    printInorder(root);

    printf("\nPostorder traversal of binary tree is \n");
    printPostorder(root);

    printf("\n");

    return 0;
}

Output:
Preorder traversal of binary tree is 
1 2 4 5 3 
Inorder traversal of binary tree is 
4 2 5 1 3 
Postorder traversal of binary tree is 
4 5 2 3 1 

Results: The DFS tree traversals program was successfully implemented and executed.
