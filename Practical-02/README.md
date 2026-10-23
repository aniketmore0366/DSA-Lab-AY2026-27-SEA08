# Practical 02: Student Result Database Management Using Array of Structures

## 1. Problem Statement

Write a C program to manage student result records using an array of structures. The program stores student details such as name, roll number, program, subject names, subject marks, total marks, and average marks. It allows the user to create student records, display the stored records, and search for a student using their roll number.

## 2. Objectives

- To understand the use of structures and arrays in C programming.
- To store multiple student records using an array of structures.
- To perform basic database operations such as creating, displaying, and searching student records.
- To calculate the total and average marks of each student.
- To understand how linear search is used to find a student record.

## 3. Concepts Used

- Structures using `typedef struct`
- Array of structures
- User-defined functions
- `do-while` loop and `switch` statement
- Input and output functions
- Arithmetic operations
- Linear search using a roll number

## 4. Algorithm / Approach

1. Start the program.
2. Define a structure named `stud` containing the student's name, roll number, program, subject names, subject marks, total, and average.
3. Declare an array of structures to store student records.
4. Display a menu with options to create, display, and search student records.
5. For the Create operation:
   - Accept the number of students.
   - Input each student's details and subject marks.
   - Calculate total marks by adding the two subject marks.
   - Calculate average marks by dividing the total by two.
6. For the Display operation:
   - Traverse the array of student records.
   - Display each student's details, total marks, and average marks.
7. For the Search operation:
   - Accept the roll number to search for.
   - Compare it with the roll numbers stored in the array.
   - Display `STUDENT FOUND` if a match exists.
   - Otherwise, display `STUDENT NOT FOUND`.
8. Repeat the menu while the selected option is less than 3.
9. Stop the program.

## 5. Test Cases

| Test Case | Input / Condition | Expected Result |
|---|---|---|
| 1 | Create two student records | Both student records are accepted and stored. |
| 2 | Tushar: marks 85 and 80 | Total = 165, Average = 82.50 |
| 3 | Ashutosh: marks 35 and 36 | Total = 71, Average = 35.50 |
| 4 | Search for roll number 6 | `STUDENT FOUND` |
| 5 | Search for roll number 19 | `STUDENT NOT FOUND` |
| 6 | Display after creating records | Stored student details and calculated marks are displayed. |

## 6. Sample Input and Output

### Sample Input

```text
Enter no. of students: 2

Student 1:
Name: Tushar
Roll no.: 6
Program: EnTC
Subject 1: EC
Subject 2: DE
Subject 1 marks: 85
Subject 2 marks: 80

Student 2:
Name: Ashutosh
Roll no.: 40
Program: EnTC
Subject 1: EC
Subject 2: DE
Subject 1 marks: 35
Subject 2 marks: 36
```

### Sample Output

```text
Student 1 Data
Name: Tushar
Roll no.: 6
Program: EnTC
Subject 1: EC
Subject 2: DE
Subject 1's marks: 85
Subject 2's marks: 80
Total: 165
Average: 82.50

Student 2 Data
Name: Ashutosh
Roll no.: 40
Program: EnTC
Subject 1: EC
Subject 2: DE
Subject 1's marks: 35
Subject 2's marks: 36
Total: 71
Average: 35.50
```

### Search Operation

**Input:**
```text
Enter student's roll no. to search: 19
```

**Output:**
```text
STUDENT NOT FOUND
```

## 7. Complexity Analysis

Let `n` be the number of student records.

- **Create:** O(n), because details are entered for each student.
- **Display:** O(n), because every stored record is displayed.
- **Search:** O(n) in the worst case, because records are checked sequentially.
- **Space Complexity:** O(n) for storing student records, with a fixed array capacity of 20.

## 8. Conclusion

This practical demonstrates the use of an array of structures to manage student result records in C. The program accepts student details, calculates total and average marks, displays records, and searches for a student using their roll number. It provides practical understanding of structured data storage, user-defined functions, and linear search.

## 9. Source Code

The C source code is available in [`program.c`](program.c).
