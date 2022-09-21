# Stack and Queues

1- What's the difference between Stack and Queue?

| Stack                                                                                                | Queue                                                                              |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| The stack is based on LIFO(Last In First Out) principle                                              | The queue is based on FIFO(First In First Out) principle.                          |
| Insertion Operation is called Push Operation                                                         | Insertion Operation is called Enqueue Operation                                    |
| Deletion Operation is called Pop Operation                                                           | Deletion Operation is called Dequeue Operation                                     |
| Push and Pop Operation takes place from one end of the stack                                         | Enqueue and Dequeue Operation takes place from a different end of the queue        |
| Simple Implementation                                                                                | Complex implementation in comparison to stack                                      |
| The most accessible element is called Top and the least accessible is called the Bottom of the stack | The insertion end is called Rear End and the deletion end is called the Front End. |

2- What is Stacks and how to use it?

Stack is a linear data structure that follows the specific order to perform the operations.
Pushing an element into the stack from one end and popping an element out of the same end are two operations we do on the stack.
The term "top of the stack" refers to the point at which all operations are carried out.
Since a stack adheres to the Last In First Out (LIFO) principle, it is crucial to keep in mind that it only holds pieces of the same data type.

Basic operations

Stack supports two basic operations which are;

- push — inserts into the stack.
- pop — deletes from the stack.

Other operations are also available but their functionality is to check the status of the Stack, unlike the insertion and deletion operations. And they are;

- isFull — checks if the stack is full.

- isEmpty — checks if the stack is empty.

- peek — gets the element at the top of the Stack.

### Push

```js
    Step 1:
  if Stack is full
  print 'Stack is full'
  return null
Step 2:
  top = top++
  Stack[top] = data

 end
```

### Pop

```js
Step 1:
  if Stack is empty
  print 'Stack is empty'
  return null
Step 2:
  deleteElement = Stack[top]
  top = top--
  return Stack

end
```

### isFull

```js
Step 1:
  if top = max
    print 'Stack is full'
    return true

  else
    print 'Stack is not full'
    return false
end
```

### isEmpty

```js
Step 1:
  if top = -1
    print 'Stack is empty'
    return true

   else
    print 'Stack is not empty'
    return false
end
```

### peek

```js
Step 1:
  return Stack[top]

end
```

3- What is Queue?

The queue is a linear data structure in which we can insert the element from one side of the list and delete the element from the other side of the list. The end of the list from where the elements are inserted is called the rear end and the end from where the elements are deleted is called the front end. Therefore, the queue data structure follows the FIFO(First In First Out) principle, which means the element inserted first from the rear end will be the first element to be deleted from the front end.
we can only store elements of the same data type in the queue data structure.
