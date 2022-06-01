# Linked Lists
-A sequence of Nodes that are connected/linked to each other.
-A data structure that contains nodes that links/points to the next node in the list. 


1.	A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
2.	A Doubly linked list means that there is a reference to both the Next and Previous node.
3.	 Head - The Head is a reference of type Node to the first node in a linked list.
4.	Current - The Current is a reference of type Node to the node that is currently being looked at.
5.	Circular linked list is a linked list where all nodes are connected to form a circle. There is no NULL at the end. A circular linked list can be a singly circular linked list or doubly circular linked list.


* linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.

* In non-linear data structures, items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.

* Linked lists don’t need to take up a single block of memory; instead, the memory that they use can be scattered throughout.

* The fundamental difference between arrays and linked lists is that arrays are static data structures, while linked lists are dynamic data structures.

* The starting point of the list is a reference to the first node, which is referred to as the head

* The end of the list a node that points to null, or an empty value.

* A single node has two parts: data, or the information that the node contains, and a reference to the next node.

* A node only knows about what data it contains, and who its neighbor is.

## insert an element into a linked list: O(1)
1.	First, we find the head node of the linked list.
2.	Next, we’ll make our new node, and set its pointer to the current first node of the list.
3.	Lastly, we rearrange our head node’s pointer to point at our new node.


## inserting an element at the end of a linked list: O(n)
1.	Find the node we want to change the pointer of (in this case, the last node)
2.	Create the new node we want to insert and set its pointer (in this case, to null)
3.	Direct the preceding node’s pointer to our new node
a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element.


### Arrays : helpful if you know the size of the list, you need random access to elements or want to itrate quickly.

### Linked list: helpful if you don’t know the size of the list, and mostly want to add or remove things quickly, without random access.


## Resources
[codefellows](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

[medium part 1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

[medium part 1](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)
