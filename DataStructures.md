DataStructures:
==============
<br/>Array:
======
<br/> Most basic DS & linear DS
<br/> Collection of elements are allocated contiguous memory. Due to which any element of an array can be accessed in constant time.
<br/>Functionalites:
<br/>Reversing
<br/>Rotation
<br/>Rearrange
<br/>Range
<br/>Multidimentional

<br/>String:
=======
<br/>String is like an array type. last char will be null to represent the end of string
<br/>
<br/>Functionalities:
<br/>Subsequence or substring
<br/>Reverse & Rotation
<br/>Binary string - string formed using two type of chars.A binary string is a string that only has two characters, usually the numbers 0 and 1, and it represents a series of binary digits.
<br/>Palindrome - Chars are at the same distance from center
<br/>Pattern searching

<br/>LinkedList:
=============

<br/> LL is also a linear DS. unlike array it will be stored in random memory. Each node has data part and address part which holds address to next node.
<br/> LL should be created using custom type class
```
public class Node
{
    //Data part
    public string data;
    //Pointer - address part
    public Node next;
}
```
<br/>Single
<br/>Circular  -Last node points to the Head of LL
<br/>Double  - Each node has two pointers. 1- previous node 2- next node [web browser[next previous], undo & redo]

<br/>Matrix/Grid
================
<br/>A matrix represents a collection of numbers arranged in an order of rows and columns. It is necessary to enclose the elements of a matrix in parentheses or brackets.
<br/>
![image](https://github.com/louisulaganathan/Algorithm/assets/74425320/c9e290b6-71d2-4865-acc8-f69ce2fbb56f)
<br/>M[2][3] = 6.

<br/>Complex DS:
===========
<br/>Stack:
======
<br/>Stack is a linear data structure which follows a particular order in which the operations are performed. The order may be LIFO(Last In First Out) 
<br/>A stack is a linear data structure in which the insertion of a new element and removal of an existing element takes place at the same end represented as the top of the stack.
<br/>![image](https://github.com/louisulaganathan/Algorithm/assets/74425320/5b250652-8ba1-4380-a086-d48b05552b8f)

<br/>Basic Operations on Stack
==============================
<br/>push() to insert an element into the stack
<br/>pop() to remove an element from the stack
<br/>top() Returns the top element of the stack.
<br/>isEmpty() returns true if stack is empty else false.
<br/>size() returns the size of stack.

![image](https://github.com/louisulaganathan/Algorithm/assets/74425320/31e1bcdd-2ccc-41de-ba02-72b2aa845220)
<br/>

Implementation of Stack:
=======================
<br/>A stack can be implemented using an array or a linked list. In an array-based implementation, the push operation is implemented by incrementing the index of the top element and storing the new element at that index. The pop operation is implemented by decrementing the index of the top element and returning the value stored at that index. In a linked list-based implementation, the push operation is implemented by creating a new node with the new element and setting the next pointer of the current top node to the new node. The pop operation is implemented by setting the next pointer of the current top node to the next node and returning the value of the current top node.

<br/>Queue:
=============
<br/>A Queue is a linear structure which follows First In First Out (FIFO) approach in its individual operations.

![image](https://github.com/louisulaganathan/Algorithm/assets/74425320/250861fb-ed72-4e08-8400-1ab21c8e828b)
A queue is a linear data structure that is open at both ends and the operations are performed in First In First Out (FIFO) order.

We define a queue to be a list in which all additions to the list are made at one end, and all deletions from the list are made at the other end. 
Basic Operations for Queue in Data Structure:
Some of the basic operations for Queue in Data Structure are:

Enqueue() – Adds (or stores) an element to the end of the queue..
Dequeue() – Removal of elements from the queue.
Peek() or front()- Acquires the data element available at the front node of the queue without deleting it.
rear() – This operation returns the element at the rear end without removing it.
isFull() – Validates if the queue is full.
isNull() – Checks if the queue is empty.


HEAP:
=====
A Heap is a special Tree-based Data Structure in which the tree is a complete binary tree.
Max-heap
Min-Heap

Max-Heap: 

In this heap, the value of the root node must be the greatest among all its child nodes and the same thing must be done for its left and right sub-tree also.

Min-Heap: 

In this heap, the value of the root node must be the smallest among all its child nodes and the same thing must be done for its left ans right sub-tree also.

![image](https://github.com/louisulaganathan/Algorithm/assets/74425320/58e7df2a-bbea-41a8-80dd-7526d4415892)

Hashing
============
Hashing refers to the process of generating a fixed-size output from an input of variable size using the mathematical formulas known as hash functions. This technique determines an index or location for the storage of an item in a data structure.


Non Linear Data Structures:
============================

Tree 

The root is the first node of the tree and the leaves are the ones at the bottom-most level. The special characteristic of a tree is that there is only one path to go from any of its nodes to any other node.
Graph

**Searching algorithms** are used to find a specific element in an array, string, linked list, or some other data structure. 

**Linear Search** – In this searching algorithm, we check for the element iteratively from one end to the other.
**Binary Search** – In this type of searching algorithm, we break the data structure into two equal parts and try to decide in which half we need to find for the element. 
**Ternary Search ** – In this case, the array is divided into three parts, and based on the values at partitioning positions we decide the segment where we need to find the required element.








