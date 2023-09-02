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










