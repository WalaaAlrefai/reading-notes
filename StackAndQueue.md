# Stacks and Queues

## Stacks 

- A stack is a data structure that consists of Nodes
- Terms for stack:
  - Push - Nodes or items that are put into the stack are pushed
  - Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
  - Top - This is the top of the stack.
  - Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
  - IsEmpty - returns true when stack is empty otherwise returns false.

- Stacks follow these concepts:
  - FILO: First In Last Out
  - LIFO: Last In First Out
- pseudocode to push a value onto a stack:

<code>

    ALOGORITHM push(value)
    // INPUT <-- value to add, wrapped in Node internally
    // OUTPUT <-- none
    node = new Node(value)
    node.next <-- Top
    top <-- Node
</code>

- Popping a Node off a stack is the action of removing a Node from the top.
- pseudocode for a peek

<code>

    ALGORITHM peek()
    // INPUT <-- none
    // OUTPUT <-- value of top Node in stack
    // EXCEPTION if stack is empty

    return top.value

</code>

- pseudocode for isEmpty

<code>

    ALGORITHM isEmpty()
    // INPUT <-- none
    // OUTPUT <-- boolean

    return top = NULL
</code>

## Queue


- Terminology for a queue is
  - Enqueue - Nodes or items that are added to the queue.

  - Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
  - Front - This is the front/first Node of the queue.
  - Rear - This is the rear/last Node of the queue.
  - Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
  - IsEmpty - returns true when queue is empty otherwise returns false.
- Queues follow these concepts:
FIFO: First in First Out
LILO: Last in Last Out
- pseudocode for the enqueue method:

<code>

    ALGORITHM enqueue(value)
    // INPUT <-- value to add to queue (will be wrapped in Node internally)
    // OUTPUT <-- none
    node = new Node(value)
    rear.next <-- node
    rear <-- node

</code>

- pseudocode for the dequeue method:

<code>

    ALGORITHM dequeue()
    // INPUT <-- none
    // OUTPUT <-- value of the removed Node
    // EXCEPTION if queue is empty

    Node temp <-- front
    front <-- front.next
    temp.next <-- null

    return temp.value

- pseudocode for a peek:

<code>

    ALGORITHM peek()
    // INPUT <-- none
    // OUTPUT <-- value of the front Node in Queue
    // EXCEPTION if Queue is empty

    return front.value
