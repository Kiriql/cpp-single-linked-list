# **Singly linked list**
## *Educational project*

A singly linked list is also called a linear unidirectional list. This data structure consists of elements of the same type. They are logically connected by pointers. Each list element points to the next one, and the last one points to nullptr. List elements are usually stored in dynamic memory.

The structure of a singly linked list is such that you can move through its elements only in a forward direction. It is impossible to find out the address of the previous element based only on the contents of the current element.

**A singly linked list allows the following operations:**
- inserting an element at the beginning or end of the list,
- inserting an element after some list element,
- deleting the element following this list element,
- checking the list for emptiness,
- determining the number of elements in the list.

**Advantages of a singly linked list:**

insertion and deletion of an element are performed in constant time, that is, they do not depend on the number of elements and the position of the element being inserted or deleted;
The size of the list is limited only by the amount of available memory.

**The disadvantages of a singly linked list follow from the features of its structure:**

Finding out the address of an element by its serial number is an operation of linear complexity. To determine the address of the Nth element of a list, you need to sequentially iterate through all N-1 elements, starting with the first element.
Memory waste: In addition to data, each list element stores a pointer to the next element. In addition, each time an object is created in dynamic memory, a couple of tens of bytes are spent maintaining the heap structure.
Insertion and removal efficiency is not as high. Every insert and every delete involves a heap operation: new or delete. These operations are considered to run in constant time, but the constant can be quite large. This executes complex synchronization code between threads and may involve low-level memory mechanisms.
Adjacent list elements may not be located sequentially in memory, reducing cache efficiency.


The list class has developed support for iterating through the elements of the SingleLinkedList container using the BasicIterator template class, on the basis of which constant and non-const list iterators are declared.
The list class also implements const and non-const versions of the begin and end methods, which return iterators to the first element of the container and the position after the last element. To make it convenient to obtain constant iterators, the cbegin and cend methods have been implemented.


**The singly linked list class implements the following functionality:**
- Comparison operations ==, !=, <, >, <=, >=;
- Exchange the contents of two lists using the swap method and the swap template function;
- Construction of a singly linked list based on initializer_list. The sequence of elements of the created list and the initializer_list is the same;
- Robust copy constructor and assignment operator. The assignment operator provides a strong exception safety guarantee. If an exception is thrown during the assignment, the contents of the left argument of the assignment operation remain unchanged.
- The PushFront method provides a strong exception safety guarantee: if an exception is thrown while the method is running, the state of the list will remain the same as before the method was called.
- The Clear method clears the list and does not throw exceptions.
- PopFront method. Removes the first element of a non-empty list in O(1) time. Does not throw exceptions.
- InsertAfter method. In O(1) time, it inserts a new value into the list after the element referenced by the iterator passed to InsertAfter. The method provides a strong exception safety guarantee.
- EraseAfter method. In O(1) time, it removes from the list the element following the element referenced by the iterator passed to InsertAfter. Does not throw exceptions.
- Methods before_begin and cbefore_begin. Return iterators that refer to a dummy position before the first element of the list. This iterator is used as a parameter for the InsertAfter and EraseAfter methods when you need to insert or remove an element at the beginning of the list.

## Assembly and installation
Build using any IDE or build from the command line

## System requirements
C++ compiler supporting C++17 standard or later
