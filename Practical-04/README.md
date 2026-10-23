# Practical 04: Decimal to Binary Conversion Using Stack

## 1. Problem Statement

Write a C program to convert a decimal number into its binary equivalent using a stack data structure. The program repeatedly divides the decimal number by 2, stores the remainders in a stack, and prints them in reverse order to obtain the binary representation.

## 2. Objectives

- To understand the concept of a stack data structure.
- To implement the Last-In-First-Out (LIFO) principle.
- To convert a decimal number into its binary equivalent.
- To use stack operations to reverse the order of binary digits.
- To understand the use of arrays for implementing a stack.

## 3. Concepts Used

- Stack data structure
- LIFO (Last-In-First-Out)
- Array implementation of a stack
- Push operation
- Stack traversal
- Modulus (`%`) and integer division (`/`)
- Loops and input/output functions in C

## 4. Algorithm / Approach

1. Start the program.
2. Accept a decimal integer from the user.
3. Declare an array to represent the stack and initialize `top = -1`.
4. Repeat while the number is not zero:
   - Calculate the remainder using `n % 2`.
   - Divide the number by 2 using integer division.
   - Increment `top` and push the remainder onto the stack.
5. Traverse the stack from `top` down to zero.
6. Print each stored remainder to obtain the binary representation.
7. Stop the program.

## 5. Test Cases

| Test Case | Decimal Input | Expected Binary Output |
|---|---:|---|
| 1 | 11 | `1011` |
| 2 | 10 | `1010` |
| 3 | 8 | `1000` |
| 4 | 1 | `1` |
| 5 | 0 | `0` |

**Note:** The current code does not print `0` when the input is zero because the loop is skipped. The program needs a special case for zero to produce the expected output shown above.

## 6. Sample Input and Output

**Sample Input**
```text
Enter Decimal number: 11
```

**Sample Output**
```text
Binary number for given decimal number is: 1011
```

## 7. Complexity Analysis

Let `n` be the input decimal number, where `n > 0`.

- **Time Complexity:** O(log n), because the number is divided by 2 repeatedly until it becomes zero.
- **Space Complexity:** O(log n), because the stack stores the binary remainders.

## 8. Conclusion

This practical demonstrates decimal-to-binary conversion using a stack implemented with an array. The remainders obtained through repeated division by 2 are stored and then printed in reverse order. This illustrates the LIFO principle and the use of stacks for reversing data.

## 9. Source Code

The C source code for this practical is available in [`program.c`](program.c).
