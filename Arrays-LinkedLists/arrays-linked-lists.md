# Arrays and Linked Lists

## Arrays

An array is a data structure that contains elements of identical data types in contiguous memory locations. The positions at which these elements are stored are called indices. In general, indexing in computer science starts from 0, not 1. For example, if an element in array "arr" is present at position 4, we would denote the element as arr[3].

- Since the indices of the elements can directly be converted into a memory address with arithmetic: `address = start + index * element_size`, the lookup in arrays is O(1). This conversion is only possible because the elements of the array are of identical data types AND stored contiguously.
- Insertion/Deletion in arrays is O(n) because the remaining elements are shifted in memory.

## Linked Lists

A linked list is a data structure where the elements are stored in separate objects called nodes. Each node contains two things: the data, and a pointer/reference to the next node in the sequence. 

- These nodes need not be in contiguous memory locations.
- In a linked list, if you wish to get to an element, you need to start at the first node and traverse the sequence to get to the desired node.
- Due to the need for traversal, the access in linked lists is O(n).
- Insertion/Deletion is O(1) (only if you are at the location of the element) since the elements are stored in non-contiguous locations and no shifting occurs.

## Difference between Arrays and Linked Lists

|                        | Array                          | Linked List                            |
| ---------------------- | ------------------------------ | -------------------------------------- |
| Memory layout          | Contiguous block               | Nodes scattered, connected by pointers |
| Access by index        | O(1) — address arithmetic      | O(n) — traverse from the head          |
| Insertion/Deletion     | O(n) — elements must shift     | O(1) — at a known position             |
| Size                   | Fixed (classic arrays)         | Grows one node at a time               |
| Extra memory per item  | None                           | One pointer per node                   |
| Binary search possible | Yes (if sorted)                | No — can't jump to the middle          |

## How to choose

- If the use case involves lots of inserts/removals/modifications then linked lists are better suited as they allow O(1) operations and O(n) (worst case if traversal is needed), whereas arrays would always operate in O(n).

- If the use case requires random access and reads at high frequency (non-sequential), then arrays are better suited. However, if the reads are sequential then linked lists might be more suitable - provided inserts and deletes are performed at higher frequency as both perform at O(n).
