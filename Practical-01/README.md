# Practical 01: Pattern Printing Using Numbers, Alphabets, and Asterisks

## 1. Problem Statement
Write a C program to display different patterns using numbers, alphabets, and asterisks. The patterns include a right-angle triangle with numbers, a diamond shape with numbers, a pyramid with asterisks, and a pyramid using alphabets.

## 2. Objectives
- To understand the use of nested loops in C programming.
- To apply control structures such as loops and conditional statements.
- To develop logic for generating structured patterns.
- To practice basic programming constructs used in implementing data structures.

## 3. Concepts Used
- `for` loops and nested loops
- Conditional statements (`if-else`)
- Pattern printing
- ASCII values for alphabet patterns
- Basic input and output functions in C

## 4. Algorithm / Approach
1. Start the program.
2. Accept the number of rows from the user.
3. Use nested loops to control the rows, columns, and spaces.
4. Print numbers in an increasing sequence to form a right-angle triangle.
5. Use spaces and number sequences to generate the diamond pattern.
6. Print asterisks in increasing odd-numbered quantities to form a pyramid.
7. Use alphabet characters to generate the alphabet pyramid.
8. Display all patterns and stop the program.

## 5. Test Cases

| Test Case | Input | Expected Result |
|---|---|---|
| 1 | `n = 1` | Each pattern displays its smallest valid form. |
| 2 | `n = 4` | Patterns display four rows in the upper/increasing section. |
| 3 | `n = 5` | Patterns display correctly for five rows. |
| 4 | `n = 0` | The program should handle zero rows appropriately. |
| 5 | Negative value | The program should reject invalid row counts if input validation is implemented. |

## 6. Sample Input and Output

**Sample Input**
```text
Enter number of rows: 4
```

**Expected Pattern Examples**

Right-angle triangle:
```text
1
1 2
1 2 3
1 2 3 4
```

Pyramid using alphabets:
```text
   A
  A B A
 A B C B A
A B C D C B A
```


## 7. Complexity Analysis
- **Time Complexity:** O(n²), assuming nested loops process up to n rows and n columns.
- **Space Complexity:** O(1) auxiliary space if the patterns are printed directly without storing them in additional arrays.

## 8. Conclusion
This practical demonstrates the use of nested loops, conditional statements, and character manipulation in C programming. It helps develop logical thinking and improves understanding of structured output generation.

## 9. Source Code
The C program for this practical is available in practical-01/main.c 
