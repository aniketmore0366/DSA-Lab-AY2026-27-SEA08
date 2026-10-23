# Practical 8: Binary Search Tree Operations for Online Directory Systems

## 1. Problem Statement
To implement a Binary Search Tree (BST) for an online contact directory system. The program stores contact names and phone numbers, performs tree traversals, and searches for a contact by name.

## 2. Objectives
- To understand the structure and properties of a Binary Search Tree.
- To insert contact details into a BST.
- To perform inorder, preorder, and postorder traversals.
- To search for a contact using its name.
- To understand recursive operations on a tree data structure.

## 3. Data Structure and Concepts Used
- **Binary Search Tree (BST):** A binary tree in which smaller names are stored in the left subtree and larger names in the right subtree, based on case-insensitive comparison.
- **Node:** Stores a contact's name, phone number, and pointers to the left and right child nodes.
- **Dynamic Memory Allocation:** `malloc()` allocates memory for each new node.
- **Recursion:** Used for insertion, traversal, and searching.
- **Inorder Traversal:** Visits left subtree, root, then right subtree.
- **Preorder Traversal:** Visits root, left subtree, then right subtree.
- **Postorder Traversal:** Visits left subtree, right subtree, then root.
- **String Comparison:** `strcasecmp()` compares names without distinguishing uppercase and lowercase letters.

## 4. Algorithm

### A. Create / Insert
1. Allocate memory for a new BST node.
2. Accept the contact's name and phone number.
3. Initialize the node's left and right pointers to `NULL`.
4. If the tree is empty, make the new node the root.
5. Otherwise, compare the new contact's name with the current node's name.
6. If the name is smaller, insert it into the left subtree.
7. If the name is larger, insert it into the right subtree.
8. Repeat while the user chooses to add more contacts.

### B. Traverse
1. Check whether the tree is empty.
2. If it is not empty, perform the following traversals:
   - **Inorder:** Left, Root, Right.
   - **Preorder:** Root, Left, Right.
   - **Postorder:** Left, Right, Root.
3. Display the contact names in each traversal order.

### C. Search
1. Accept the contact name to search for.
2. Compare the search key with the current node's name.
3. If both names match, display the contact's name and phone number.
4. If the key is smaller, search the left subtree.
5. If the key is larger, search the right subtree.
6. If the search reaches `NULL`, display “Contact not found.”

## 5. Test Cases

| Test Case | Operation | Expected Result |
|---|---|---|
| 1 | Create a tree with contacts Neel, Abhishek, and Utkarsh | Contacts are inserted according to BST ordering |
| 2 | Perform inorder traversal | Names are displayed in case-insensitive alphabetical order |
| 3 | Perform preorder traversal | Root is displayed before its subtrees |
| 4 | Perform postorder traversal | Root is displayed after its subtrees |
| 5 | Search for an existing contact | Contact name and phone number are displayed |
| 6 | Search for a contact that does not exist | “Contact not found” is displayed |
| 7 | Select Exit | “Exited Successfully” is displayed |

## 6. Sample Input and Output

**Example contacts inserted in this order:**
- Neel — 9876543210
- Abhishek — 9876501234
- Utkarsh — 9876512345

**Sample traversal output:**
```text
Inorder: Abhishek Neel Utkarsh
Preorder: Neel Abhishek Utkarsh
Postorder: Abhishek Utkarsh Neel
```

**Sample search output:**
```text
Enter contact name to search: Utkarsh
Contact found
Name: Utkarsh
Phone: 9876512345
```

*Note: The sample assumes these three contacts are inserted in the order shown. Actual output depends on the contacts entered.*

## 7. Time and Space Complexity

Let `n` be the number of contacts and `h` be the height of the BST.

- **Insertion:** O(h) per contact.
- **Inorder Traversal:** O(n).
- **Preorder Traversal:** O(n).
- **Postorder Traversal:** O(n).
- **Search:** O(h).
- **Average Time for Insertion and Search:** O(log n) for a reasonably balanced tree.
- **Worst-Case Time for Insertion and Search:** O(n) when the tree becomes skewed.
- **Space Complexity:** O(n) for storing the nodes. Recursive operations also use O(h) call-stack space.

## 8. Conclusion
The online directory system was implemented using a Binary Search Tree. The program supports contact insertion, inorder, preorder and postorder traversals, and searching by contact name. It demonstrates dynamic memory allocation, recursion, and efficient searching when the tree is reasonably balanced.

## Source Code
Refer to [`program.c`](program.c) for the complete implementation.
