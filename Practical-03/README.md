# Practical 03: Searching Contact Names Using Sequential Search and Binary Search

## 1. Problem Statement

Write a C program to manage contact details and search for a specific contact using Sequential (Linear) Search and Binary Search. Each contact contains a name, phone number, and address. The program displays the contact list, searches for a name using Linear Search, sorts the contact names alphabetically, and then searches using Binary Search. It also counts the comparisons performed by both searching techniques.

## 2. Objectives

- To understand Sequential Search and Binary Search.
- To implement searching techniques using strings in C.
- To store and display contact details using an array of structures.
- To sort contact names alphabetically using Bubble Sort.
- To count and compare the number of comparisons performed by both searching methods.

## 3. Concepts Used

- Structures using `typedef struct`
- Array of structures
- String handling using `string.h`
- String comparison using `strcasecmp()`
- Sequential (Linear) Search
- Bubble Sort
- Binary Search
- Loops and conditional statements
- Comparison counting

## 4. Algorithm / Approach

### A. Input and Display Contact Details

1. Start the program.
2. Accept the number of contacts.
3. Input each contact's name, phone number, and address.
4. Store the details in an array of structures.
5. Display all the stored contact details.

### B. Sequential (Linear) Search

1. Accept the name to search for.
2. Initialize the comparison counter to zero.
3. Traverse the contact array from the first contact.
4. Compare each contact name with the search key using `strcasecmp()`.
5. If a match is found, display the contact's name, phone number, and address.
6. If no match is found, display `CONTACT NOT FOUND`.
7. Display the number of comparisons performed.

### C. Sort Contact Names

1. Use Bubble Sort to compare adjacent contact names.
2. Compare names alphabetically using `strcasecmp()`.
3. Swap adjacent names when they are in the wrong alphabetical order.
4. Repeat the passes until the list is sorted.

### D. Binary Search

1. Initialize `low = 0` and `high = n - 1`.
2. Calculate the middle index using `mid = (low + high) / 2`.
3. Compare the middle contact name with the search key.
4. If the names match, display the contact's position.
5. If the middle name comes alphabetically before the search key, search the right half.
6. Otherwise, search the left half.
7. Repeat until the name is found or the search range becomes empty.
8. Display the number of comparisons performed.

## 5. Test Cases

| Test Case | Input / Condition | Expected Result |
|---|---|---|
| 1 | Search for an existing contact: `Utkarsh` | Contact is found using Linear Search and Binary Search. |
| 2 | Search using lowercase input: `utkarsh` | The name matches `Utkarsh` because `strcasecmp()` ignores letter case. |
| 3 | Search for a name that does not exist | Both searches report that the contact was not found. |
| 4 | Search for the first contact in the input list | Linear Search finds the contact on the first comparison. |
| 5 | Search for the last contact in the input list | Linear Search may require checking all contacts. |
| 6 | Enter contacts in an unsorted order | The program sorts names alphabetically before Binary Search. |

## 6. Sample Input and Output

### Sample Input

```text
Enter number of contacts: 5

Contact 1:
Name: Neel
Contact: 9874125630
Address: Satara

Contact 2:
Name: Abhishek
Contact: 9632014587
Address: Nagpur

Contact 3:
Name: Pushpak
Contact: 9874563210
Address: Pune

Contact 4:
Name: Utkarsh
Contact: 8520147963
Address: Mumbai

Contact 5:
Name: Chaitanya
Contact: 5203698741
Address: Pune

Enter name of contact to search: utkarsh
```

### Sample Output

```text
---//Linear Search//---
CONTACT FOUND
Name: Utkarsh
Contact: 8520147963
Address: Mumbai
Linear comparisons: 4

---//Binary Search//---
Contact found at location 5
Number of binary comparisons: 3
```

The output above follows the supplied program's sample run.

## 7. Complexity Analysis

Let `n` be the number of contacts.

| Operation | Time Complexity |
|---|---|
| Input and Display | O(n) |
| Linear Search | O(n) worst case |
| Bubble Sort | O(n²) worst case |
| Binary Search | O(log n) worst case |

**Space Complexity:** O(n) for storing the contact records in an array. The sorting and searching operations use a constant amount of additional space in this implementation.

**Note:** The current Bubble Sort implementation swaps only contact names, not the corresponding phone numbers and addresses. Therefore, after sorting, the displayed Binary Search position refers to the sorted name array, and the contact details may no longer correspond to that name. Sorting the complete contact structure would preserve the association between each name, phone number, and address.

## 8. Conclusion

This practical demonstrates Sequential Search and Binary Search for locating contact names. It uses an array of structures to store contact information, Bubble Sort to arrange names alphabetically, and comparison counters to observe searching operations. It highlights the importance of sorted data for Binary Search and demonstrates the difference between linear and binary searching techniques.

## 9. Source Code

The C source code for this practical is available in [`program.c`](program.c).
