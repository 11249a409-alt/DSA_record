---

# **1. AIM**

To write a C program to search for an element in an array using Linear Search using only the variable **found**.

---

# **2. ALGORITHM**

1. Start the program.
2. Declare variables: array, n, key, found = 0.
3. Read the number of elements (n).
4. Input all array elements.
5. Read the element to be searched (key).
6. For each element from index 0 to n–1:

   * If `arr[i] == key`:

     * Set `found = 1`
     * Print position = `i + 1`
     * Break
7. After loop, if `!found` (found == 0):

   * Print “Element not found”.
8. Stop the program.

---

# **3. PROGRAM 
#include <stdio.h>

int main() {
    int arr[50], n, i, key, found = 0;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter element to search: ");
    scanf("%d", &key);

    for(i = 0; i < n; i++) {
        if(arr[i] == key) {
            found = 1;
            printf("Element %d found at position %d\n", key, i + 1);
            break;
        }
    }

    if(!found) {
        printf("Element %d not found in the array\n", key);
    }

    return 0;
}
```

---

# **4. OUTPUT**

```
Enter number of elements: 5
Enter 5 elements:
10 20 30 40 50
Enter element to search: 50
Element 50 found at position 5
```

**OR, if element not found:**

```
Element 25 not found in the array
```

---

# **5. RESULT**

The program for Linear Search using **found** (without index variable) was successfully executed.

---

