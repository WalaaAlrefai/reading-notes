## Linked Lists

A linked list is a sequence of nodes that contain some data and a pointer to other nodes. Each node points to the next node in the link.

__Terminology__

*__singly__* --> there is only one reference, and the reference points to the next node in a linked list.

*__doubly__* --> there is a reference to both the next and previous node.

*__node__* --> individual items/links that live in a linked list. each node contains the data for each link.

*__next__* --> property in the node that contains the reference to the next node.

*__head__* --> reference of type node to the first node in a linked list.

*__Current__* --> reference of type node to the node that is currently being looked at. when traversing, you create a new current variable at the head to guarantee you are starting from the beginning of the linked list.