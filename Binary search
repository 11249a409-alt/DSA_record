Aim: To write a C program to implement **Binary Search** 
---

# **1. AIM**

To write a C program to search for an element in a sorted array using the **Binary Search** technique using only the variable **found**.

---

# **2. ALGORITHM**

1. Start the program.
2. Declare variables: array, n, key, low, high, mid, found = 0.
3. Read the number of elements (n).
4. Input **n sorted elements** into the array.
5. Read the element to be searched (key).
6. Set `low = 0` and `high = n - 1`.
7. Repeat while `low <= high`:

   * Compute `mid = (low + high) / 2`
   * If `arr[mid] == key`:

     * Set `found = 1`
     * Print position = `mid + 1`
     * Break
   * Else if `key < arr[mid]`:

     * Set `high = mid - 1`
   * Else

     * Set `low = mid + 1`
8. After loop, if `!found` :

   * Print “Element not found”.
9. Stop the program.

---

# **3. PROGRAM 

```c
#include <stdio.h>

int main() {
    int arr[50], n, i, key, low, high, mid, found = 0;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    printf("Enter %d sorted elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter element to search: ");
    scanf("%d", &key);

    low = 0;
    high = n - 1;

    while(low <= high) {
        mid = (low + high) / 2;

        if(arr[mid] == key) {
            found = 1;
            printf("Element %d found at position %d\n", key, mid + 1);
            break;
        }
        else if(key < arr[mid]) {
            high = mid - 1;
        }
        else {
            low = mid + 1;
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
Enter number of elements: 6
Enter 6 sorted elements:
5 10 15 20 25 30
Enter element to search: 20
Element 20 found at position 4
```

**OR**

```
Element 12 not found in the array
```

---

# **5. RESULT**

The Binary Search program  was successfully executed.

---

