# Practical 02: Student Result Database Management Using Array of Structures

## 1. Problem Statement

Design and implement a student result management system using an array of structures in C. The system should allow users to add new student records, update existing records, search for specific students, display records, and sort records based on performance metrics such as total marks or average marks. Each student record should contain roll number, name, program, course, subject marks, total marks, and average marks.

## 2. Objectives

- To understand the use of arrays and structures in C programming.
- To implement database operations such as insertion, updating, searching, displaying, and sorting.
- To develop logical thinking for managing structured data.
- To simulate a real-world student result management system.

## 3. Concepts Used

- Structures (`struct`) in C
- Array of structures
- Functions and control structures
- Record insertion and modification
- Linear search
- Bubble sort
- Calculation of total and average marks
- String handling for student names

## 4. Algorithm / Approach

### Step 1: Define the Structure
1. Define a structure named `Student`.
2. Include roll number, name, program, course, subject marks, total marks, and average marks.
3. Declare an array of structures to store student records.
4. Initialize the record count to zero.

### Step 2: Insert Student Records
1. Accept the number of student records to add.
2. Input each student's roll number, name, program, course, and subject marks.
3. Calculate the total marks by adding the subject marks.
4. Calculate the average by dividing the total marks by the number of subjects.
5. Store the record and increment the count.

### Step 3: Display All Records
1. Traverse the array from index zero to the last stored record.
2. Display each student's details, subject marks, total, and average.

### Step 4: Search for a Student
1. Accept a roll number or name to search for.
2. Compare the search value with each stored record.
3. If a match is found, display the student's record.
4. If no match is found, display an appropriate message.

### Step 5: Sort Student Records
1. Use bubble sort to compare adjacent student records.
2. Sort records by total marks or average marks, as required.
3. Swap records when they are in the wrong order.
4. Display the sorted records.

### Step 6: Update a Student Record
1. Accept the roll number of the student to modify.
2. Search for the corresponding record.
3. If found, update the required details or marks.
4. Recalculate total and average marks after modifying the marks.

### Step 7: Append a Record
1. Accept the details of a new student.
2. Calculate total and average marks.
3. Store the new record at the end of the array.
4. Increment the record count.

## 5. Test Cases

| Test Case | Input / Condition | Expected Result |
|---|---|---|
| 1 | Add a student with valid details and marks | Student record is stored with calculated total and average. |
| 2 | Display stored student records | All stored records are displayed correctly. |
| 3 | Search using an existing roll number or name | The matching student record is displayed. |
| 4 | Search using a non-existing roll number or name | A record-not-found message is displayed. |
| 5 | Sort records by total marks | Records are arranged according to total marks. |
| 6 | Update marks for an existing student | Marks, total, and average are updated correctly. |
| 7 | Attempt to add records beyond the array capacity | The program should prevent insertion beyond the supported capacity if validation is implemented. |

## 6. Sample Input and Output

**Illustrative student record:**

```text
Roll Number: 101
Name: Aarav
Program: BTech
Course: DSA
Subject Marks: 80 85 90 75 70
```

**Expected calculated values:**

```text
Total Marks: 400
Average Marks: 80.00
```

The above values illustrate the total and average calculation for five subject marks. The actual prompts and output format depend on the implementation.

## 7. Complexity Analysis

- **Insertion:** O(1) per record when inserting at the next available array position, excluding input processing.
- **Display:** O(n) for n student records.
- **Search:** O(n) using linear search in the worst case.
- **Sorting:** O(n²) using bubble sort in the worst case.
- **Update:** O(n) in the worst case when a record is located using linear search.
- **Space Complexity:** O(n) for storing n student records, with a fixed maximum capacity in an array-based implementation.

## 8. Conclusion

This practical demonstrates how arrays of structures can be used to organize and manage student records in C. It applies insertion, display, searching, updating, and sorting operations while calculating total and average marks. It improves understanding of structured data management and basic database operations.

## 9. Source Code

The C program for this practical is available in [`program.c`](program.c).
