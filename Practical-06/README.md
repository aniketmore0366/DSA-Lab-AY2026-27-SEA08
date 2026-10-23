# Practical 6: Train Ticket Booking System Using Queue

## 1. Problem Statement
To implement a train ticket booking system using a queue. The program allows users to book tickets, cancel confirmed tickets, display confirmed bookings, and maintain a waiting list when all confirmed ticket slots are occupied. When a confirmed ticket is cancelled, the first ticket in the waiting list is confirmed.

## 2. Objectives
- To understand the queue data structure and FIFO principle.
- To implement ticket booking and cancellation operations.
- To manage confirmed tickets using a circular queue.
- To maintain a waiting list when the confirmed queue is full.
- To automatically confirm a waiting-list ticket when a confirmed ticket is cancelled.

## 3. Data Structure and Concepts Used
- **Circular Queue:** Stores up to five confirmed tickets.
- **Array:** Stores confirmed tickets and waiting-list tickets.
- **Front:** Points to the first confirmed ticket.
- **Rear:** Points to the last confirmed ticket.
- **FIFO (First In, First Out):** The earliest waiting-list ticket is confirmed first.
- **Waiting List:** Stores tickets when the confirmed queue is full.
- **Modulo Operator (`%`):** Supports circular movement of queue positions.

## 4. Algorithm
1. Initialize the confirmed queue with `front = -1` and `rear = -1`. Initialize the waiting-list count to zero.
2. Display the menu: Book Ticket, Cancel Ticket, Display Bookings, and Exit.
3. For **Book Ticket**:
   - Accept the ticket number.
   - If the confirmed queue is full, add the ticket to the waiting list if space is available.
   - If the waiting list is also full, display a waiting-list-full message.
   - Otherwise, insert the ticket into the confirmed circular queue.
4. For **Cancel Ticket**:
   - Accept the ticket number to cancel.
   - Search for the ticket among confirmed tickets.
   - If the ticket is not found, display an appropriate message.
   - Otherwise, remove the ticket and adjust the queue.
   - If a waiting-list ticket exists, confirm the first waiting ticket and shift the remaining waiting-list entries.
5. For **Display Bookings**:
   - Display all confirmed tickets.
   - Display all waiting-list tickets.
6. Repeat the menu until the user selects Exit.
7. Stop the program.

## 5. Test Cases

| Test Case | Operation | Expected Result |
|---|---|---|
| 1 | Book tickets 101, 103, 102, 104, 105 | All five tickets are confirmed |
| 2 | Book ticket 106 when confirmed queue is full | Ticket is added to the waiting list |
| 3 | Book ticket 107 | Ticket is added to the waiting list |
| 4 | Display bookings | Confirmed and waiting-list tickets are displayed |
| 5 | Cancel confirmed ticket 102 | Ticket is cancelled and ticket 106 is confirmed |
| 6 | Display bookings again | Confirmed tickets are 101, 103, 104, 105, 106; waiting list contains 107 |
| 7 | Cancel a ticket that does not exist | “Ticket not found” is displayed |
| 8 | Select Exit | Exit message is displayed |

## 6. Sample Input and Output

**Sample operations:**
- Book tickets: 101, 103, 102, 104, 105
- Book tickets: 106 and 107 after the confirmed queue becomes full
- Cancel ticket: 102
- Display bookings
- Select Exit

**Sample output:**
```text
Confirmed Tickets: 101 103 102 104 105
Waiting List: 106 107

Ticket cancelled
Waiting ticket 106 confirmed

Confirmed Tickets: 101 103 104 105 106
Waiting List: 107

EXITED SUCCESSFULLY
```

## 7. Time and Space Complexity

Let `n` be the number of confirmed tickets and `w` be the number of waiting-list tickets.

- **Book Ticket:** O(1)
- **Search for Ticket during Cancellation:** O(n)
- **Remove Ticket and Shift Queue Entries:** O(n)
- **Confirm Waiting Ticket and Shift Waiting List:** O(w)
- **Display Bookings:** O(n + w)
- **Space Complexity:** O(1) for this implementation because both arrays have a fixed capacity of five elements.

## 8. Conclusion
The train ticket booking system was implemented using a circular queue and arrays. The program supports booking, cancellation, displaying confirmed tickets, and maintaining a waiting list. When a confirmed ticket is cancelled, the first waiting-list ticket is confirmed, demonstrating the FIFO principle.

## Source Code
Refer to [`program.c`](program.c) for the complete implementation.
