# Practical 5: Circular Queue Implementation Using Array for Parcel Handling System

## 1. Problem Statement
To implement a circular queue using an array for a parcel handling system. The program allows the user to add parcels, dispatch parcels, and display the parcels remaining in the queue. It also checks whether the queue is full or empty.

## 2. Objectives
- To understand the concept of a circular queue.
- To implement queue operations using an array.
- To perform insertion, deletion, and display operations.
- To understand the FIFO (First In, First Out) principle.
- To manage queue positions using circular indexing.

## 3. Data Structure and Concepts Used
- **Circular Queue:** A queue in which the last position connects back to the first position.
- **Array:** Stores parcel numbers.
- **Front:** Points to the parcel that will be dispatched next.
- **Rear:** Points to the last parcel added.
- **FIFO:** The parcel added first is dispatched first.
- **Modulo Operator (`%`):** Helps move the front and rear positions circularly.
- **Overflow and Underflow:** Checks whether the queue is full or empty.

## 4. Algorithm
1. Start the program and initialize `front` and `rear` to `-1`.
2. Display the menu: Add, Dispatch, Display, and Exit.
3. For **Add**:
   - Check whether the queue is full.
   - If full, display a queue-full message.
   - Otherwise, update `rear` circularly and insert the parcel number.
4. For **Dispatch**:
   - Check whether the queue is empty.
   - If empty, display a queue-empty message.
   - Otherwise, display the parcel being dispatched and update `front`.
   - If the last parcel is dispatched, reset both `front` and `rear`.
5. For **Display**:
   - If the queue is empty, display an appropriate message.
   - Otherwise, display all parcels from `front` to `rear` in queue order.
6. Repeat the menu until the user selects Exit.
7. Stop the program.

## 5. Test Cases

| Test Case | Operation | Expected Result |
|---|---|---|
| 1 | Add parcels 1, 2, 3, 4, 5 | All five parcels are added |
| 2 | Add another parcel | Queue-full message is displayed |
| 3 | Dispatch a parcel | Parcel 1 is dispatched |
| 4 | Display the queue | Parcels 2, 3, 4, 5 are displayed |
| 5 | Dispatch all parcels and dispatch again | Queue-empty message is displayed |
| 6 | Select Exit | Exit message is displayed |

## 6. Sample Input and Output

**Sample operations:**
- Add parcels: 1, 2, 3, 4, 5
- Attempt to add another parcel
- Dispatch one parcel
- Display the queue
- Select Exit

**Sample output:**
```text
Parcel queue is Full

Parcel 1 is dispatched

Parcel no. left in queue are: 2 3 4 5

EXITED SUCCESSFULLY
```

## 7. Time and Space Complexity

- **Insertion:** O(1)
- **Dispatch/Deletion:** O(1)
- **Display:** O(n), where n is the number of parcels in the queue.
- **Space Complexity:** O(n), where n is the queue capacity. In this program, the array has a fixed capacity of 5 parcels, so the allocated array space is constant.

## 8. Conclusion
The circular queue was implemented successfully using an array. The program performs parcel insertion, dispatch, and display operations while checking full and empty conditions. Circular indexing allows the queue to reuse array positions after parcels are dispatched and demonstrates the FIFO principle.

## Source Code
Refer to [`program.c`](program.c) for the complete implementation.
