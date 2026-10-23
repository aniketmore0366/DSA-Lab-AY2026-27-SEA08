# Practical 7: Dynamic Text Editor Using Singly Linked List

## 1. Problem Statement
To implement a dynamic text editor using a singly linked list. The program allows the user to create a list of text elements, insert a new element at a specified location, display the list, delete an element, and reverse the linked list.

## 2. Objectives
- To understand the concept of a singly linked list.
- To perform insertion and deletion at specified positions.
- To display the elements stored in the linked list.
- To reverse the linked list using pointers.
- To understand dynamic memory allocation using `malloc()` and memory deallocation using `free()`.

## 3. Data Structure and Concepts Used
- **Singly Linked List:** A collection of nodes connected through pointers.
- **Node:** Contains a data field and a pointer to the next node.
- **Head Pointer:** Points to the first node in the list.
- **Dynamic Memory Allocation:** `malloc()` allocates memory for new nodes.
- **Memory Deallocation:** `free()` releases memory when a node is deleted.
- **Pointers:** Used to connect, traverse, insert, delete, and reverse nodes.
- **Reversal:** Changes the direction of links between nodes.

## 4. Algorithm

### A. Create
1. Allocate memory for a new node using `malloc()`.
2. Accept data for the node.
3. Set its `next` pointer to `NULL`.
4. If the list is empty, make the new node the head.
5. Otherwise, attach the new node at the end.
6. Repeat while the user chooses to continue.

### B. Insert
1. Accept the location and data for the new node.
2. Allocate memory for the node.
3. If the location is 1, link the new node before the current head and update the head.
4. Otherwise, traverse to the node immediately before the specified location.
5. Adjust the pointers to insert the new node.

### C. Display
1. Start from the head node.
2. Print the data of each node followed by an arrow.
3. Continue until the pointer becomes `NULL`.
4. Print `NULL` at the end.

### D. Delete
1. Accept the location of the node to delete.
2. If the location is 1, update the head to the next node.
3. Otherwise, traverse to the node before the target node.
4. Update the links to bypass the target node.
5. Release the deleted node's memory using `free()`.

### E. Reverse
1. Initialize three pointers: `p = NULL`, `q = head`, and `r = NULL`.
2. Store the next node in `r`.
3. Reverse the current node's link so it points to `p`.
4. Move `p` and `q` one node forward.
5. Repeat until `q` becomes `NULL`.
6. Update the head to `p` and display the reversed list.

## 5. Test Cases

| Test Case | Operation | Expected Result |
|---|---|---|
| 1 | Create nodes containing A, B, C | `A->B->C->NULL` |
| 2 | Insert X at location 2 | `A->X->B->C->NULL` |
| 3 | Display the list | All nodes are displayed in order |
| 4 | Delete the node at location 2 | `A->B->C->NULL` |
| 5 | Reverse the list | `C->B->A->NULL` |
| 6 | Select Exit | Exit message is displayed |

*Note: These test cases describe the intended operations. Verify the output with the corrected program before submitting.*

## 6. Sample Input and Output

**Example list before reversal:**
```text
A->B->C->NULL
```

**Output after reversal:**
```text
C->B->A->NULL
```

## 7. Time and Space Complexity

Let `n` be the number of nodes in the linked list.

- **Create:** O(n) for creating n nodes.
- **Insert:** O(n) in the worst case because traversal may be required.
- **Display:** O(n).
- **Delete:** O(n) in the worst case because traversal may be required.
- **Reverse:** O(n).
- **Space Complexity:** O(n) for storing n nodes. The reversal operation itself uses O(1) auxiliary space.

## 8. Conclusion
The dynamic text editor was implemented using a singly linked list. The program demonstrates node creation, insertion, display, deletion, and reversal using pointers and dynamic memory allocation. These operations illustrate how linked lists can manage dynamically changing data.

## Source Code
Refer to [`program.c`](program.c) for the complete implementation.
