---
title: "Stacks & Queues In Java"
datePublished: Sat Mar 02 2024 08:21:48 GMT+0000 (Coordinated Universal Time)
cuid: clt9tedj1000009kyhn9jbray
slug: stacks-queues-in-java
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1709367628122/12ac57ec-7f50-4f3b-ad10-9344ed657ed8.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1709367667755/da9b773d-8fa6-4d1b-a5b0-28cf59c6591b.png
tags: java, stacks, dsa

---

## **What Is Stack?**

Stack is a linear data structure similar to `arrays` and `linked lists`, restricting the random access of elements.

![A Huge Guide About Stack Data Structure - Techno Gezgin](https://technogezgin.com/en/wp-content/uploads/sites/4/2021/02/Examples-of-Stack-Data-Structure-From-Real-Life.png align="left")

It is like a container of pieces that can only be stacked on top of each other and removed from that same direction. That's why Stack doesn't support traversal or random indexing.

![Stack in Java | Methods, Example Program - Scientech Easy](https://www.scientecheasy.com/wp-content/uploads/2021/01/java-stack.png align="center")

## Where do we use Stacks?

1. **Word Reversal:** You can reverse a word by pushing its letters onto a stack and then popping them back.
    
2. **Undo Functionality:** Text editors use stacks to implement "undo" operations, allowing users to revert text changes.
    
3. **Backtracking:** In situations like mazes, backtracking involves storing possible choices on a stack and popping them to retrace steps.
    
4. **Language Processing:** Stacks are used internally for managing parameters, local variables, and recursion checks in compilers.
    

## How to use Java's Built-In Functions for Stack Manipulation?

We first create a stack using `Stack<Integer> stack = new Stack<>();` to hold integers. We then use the `push` method to add elements to the stack. Each call to `push` adds an element to the top of the stack.

### `push()` :

```java
   public static void main(String[] args){

     Stack<Integer> stack = new Stack <> ();
        stack.push(67);
        stack.push(87);
        stack.push(56);
        stack.push(23);
        stack.push(89);
        stack.push(11);
        stack.push(43);
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693860315730/5d9b2f8b-ebae-46cc-8c55-1bc9a6286cdb.png align="center")

### `pop()` :

`pop()` removes and returns the top element from the stack.

```java
stack.pop();
```

Notice how elements pushed last onto the stack are the first to be popped from it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693860754702/25e40790-b9ce-43a0-9de2-a0c3612335ed.png align="left")

Now that we've removed all the elements, the stack is empty. If you attempt to remove an element from an empty stack, it will result in an underflow error or exception.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693865602103/c41078f5-639b-4e9f-95d3-092ff0174cef.png align="center")

## How Does Internal Implementation of a Stack Work in Java?

Java's `Stack` class utilises inheritance by extending the `Vector` class. A `Stack` essentially inherits the core functionality of a `Vector` with more additional methods and constraints to enforce stack behaviour, such as `push` and `pop` operations.

Internally, the `Stack` class relies on a dynamic array, similar to the structure used by `Vector`, to store its elements.

This dynamic array serves as the actual storage for elements, allowing the stack to automatically adjust its size by growing or shrinking as needed.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693866903318/a4cd20ce-dfb1-446e-b3a5-86e016f562a6.png align="center")

In the `Vector` class, the declaration `protected Object[] elementData;` defines a protected instance variable known as `elementData`. This array serves as the fundamental data storage for the `Vector` class, holding the elements that are added to the vector.

`Vector` is a class that encapsulates this array along with a set of methods and behaviours for dynamic resizing, element access, and manipulation.

In essence, `elementData` is the backbone that enables `Vector` to function as a dynamic array, but `Vector` provides a higher-level interface and additional functionality beyond what a simple array would offer.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693867181563/f07f9431-9c14-4a0e-95fc-f58fb0ce5a82.png align="center")

**Think of it this way:** our stack is built on top of a vector, and a vector is like an array. So, our stack is kind of like an array.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693867809066/3293e506-3555-4d9c-9dae-f80d7845699e.png align="center")

## How to Create Your Custom Stack in Java?

Let's gain a basic understanding of how we can utilise a pointer to create a custom stack in Java. To illustrate this concept, imagine an array with 9 elements, which we'll use to simulate a stack.

In this representation, the value **\-1** is used to indicate the stack pointer's position. Since -1 is not a valid index in the array, it signifies that the stack is **empty**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693845339496/96100fed-6b0d-433f-9dc7-e59830d049f4.png align="center")

If we want to add data, we need to increment the pointer, right?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693845625009/9f550522-35a8-4ad2-9d22-e108d4ec8922.png align="center")

Now, we will increment the pointer again and then fill in the data.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693845756677/ca4c2199-d5e0-479f-8f1f-2ba74241140a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693845790471/b94547be-ac97-40bf-9596-3b5acc76e347.png align="center")

And so on...

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693845862008/a286b44a-c428-4472-be31-c442524a42f6.png align="center")

## How to remove data from the stack?

Suppose this is our stack array, and we want to remove elements from it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693846115006/c427fa01-06b8-411f-8333-9e55b778ecaa.png align="center")

To remove data, we simply decrement the pointer by 1.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693846197924/7640296c-2e6e-4658-94c5-2df792d1088c.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693846299089/50a6f3b6-d907-4d0e-b87c-2a5e7bbf3d6b.png align="center")

Now, what about the values we've just removed?

They technically remain in the stack, but they are no longer relevant. In this data structure, we always know that the pointer points to the number at the top of the stack. Right?

So, Any numbers following this pointer are essentially ignored, as they are not considered part of the active stack. But it is a good practice to display the item that is removed.

### Custom class:

```java
import java.util.Arrays;

public class CustomStack {
    protected int[] data;
    private static final int DEFAULT_SIZE = 10;
    int ptr = -1; //initially stack is empty

    public CustomStack() {
        this(DEFAULT_SIZE);
    }

    public CustomStack(int size) {
        this.data = new int[size];
    }

    public boolean push(int item) {

        if (isFull()){
            System.out.println("Stack is full!");
            return false;
        }

        ptr++;
        data[ptr] = item;
        return true;
    }
    public int pop() throws StackException{
        if (isEmpty()){
            throw new StackException("Can not pop from an empty stack!!");
        }
        int removed = data[ptr];
        ptr--;
        return removed;
    }
    private boolean isFull(){
        return ptr == data.length - 1;//ptr is at last index
    }

    public int peek() throws StackException{
        if (isEmpty()){
            throw new StackException("Can not peek from an empty stack!!");
        }
        return data[ptr];
    }

    private boolean isEmpty(){
        return ptr == -1;
    }
}
```

### Exception class:

Invoke the constructor of the exception(super) class & pass the provided messages as an argument.

Basically, telling the exception class *"Take this message I'm giving you & use it like an exception message"*

```java
public class StackException extends Exception{
    public StackException(String message) {
        super(message);
    }
}
```

### Main class:

```java
import java.util.Stack;
import java.util.Deque;
public class inBuiltExamples {
    public static void main(String[] args) {

  CustomStack stack = new CustomStack(7);
        stack.push(67);
        stack.push(87);
        stack.push(56);
        stack.push(23);
        stack.push(89);
        stack.push(11);
        stack.push(43);

        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
```

### How to Create a Dynamic Custom Stack in Java?

The `DynamicStack` class extends `CustomStack` to inherit its functionality. It introduces two constructors: one for a default-sized stack and another for a stack with a specific initial size.

This allows `DynamicStack` dynamically adapts to the number of elements, automatically resizing itself when necessary, making it a flexible choice for stack management in Java.

```java
public class DynamicStack extends CustomStack {

    public DynamicStack() {
        super(); // Calls the default constructor of CustomStack
    }

    public DynamicStack(int size) {
        super(size); // Calls the constructor of CustomStack with a specified size
    }
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693871350872/85640a82-0490-4c66-9b26-d277c58f9281.png align="center")

These are the various functions that we can perform on our custom stack:

* Pop
    
* Peek (or Top)
    
* isEmpty
    
* isFull
    
* Push
    

Now, let's consider which one of these stack functions might create a problem if we want to **add** more elements to the stack. `push()` right?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693884134431/30a2267f-53cc-483f-8cab-00d18c4567e1.png align="center")

We will create a temporary array with a size that is twice the size of the data array.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693885141635/441a0fa2-dc7e-4aac-aef8-2a98653d594d.png align="center")

Next, we'll copy all the elements from the `data` array to the `temp` array and Update the data array to the new larger array.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693884870526/741c928a-76b0-426e-ae1f-e152293a764c.png align="center")

Now, let's take a closer look at the code.

```java
public class DynamicStack extends CustomStack {

    public DynamicStack() {
        super(); // Calls the default constructor of CustomStack
    }

    public DynamicStack(int size) {
        super(size); // Calls the constructor of CustomStack with a specified size
    }

    @Override
    public boolean push(int item) {
        // Check if the stack is full
        if (this.isFull()) {
            // Double the array size
            int[] temp = new int[data.length * 2];

            // Copy all previous items to the new data array
            for (int i = 0; i < data.length; i++) {
                temp[i] = data[i];
            }
            data = temp; // Update the data array to the new larger array
        }
        // At this point, we know the array is not full, so insert data normally
        // Insert the item using the push method from CustomStack
        return super.push(item);
    }
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693872035919/b1d6c5b3-d950-4f38-8109-af5b8c8d1f95.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693879799477/ae7ef24a-33ac-4ab5-852b-d00d67528728.png align="center")

But when we call the `push` method from `DynamicStack` successfully inserts the element.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693880865943/96268340-e659-4b13-97a4-f206ecbf0d3d.png align="center")

You can use a more general type to refer to a more specific object.

Suppose you have a big container called `CustomStack` that can hold things. Now, you make a smaller container called `DynamicStack` that fits inside the big one. You can still put things in the smaller container and use it inside the big one. But remember, the smaller container can only do what both containers can do For instance, you can create a `DynamicStack` object and assign it to a `CustomStack` variable like this: `CustomStack stack = new DynamicStack(5);`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693881360560/f79fb025-9d4a-4b48-8373-7d0b02580cfa.png align="center")

This works because `DynamicStack` is a kind of `CustomStack`, so you can use it where a `CustomStack` is expected.

However, when you use the `stack` variable, you can only use the features that both `CustomStack` and `DynamicStack` has in common. Are any special features unique to `DynamicStack` won't be available through this variable.

## **What Is Queue?**

A queue is a container of objects (a linear collection) that are inserted and removed according to the **first-in-first-out (FIFO)** principle.

It's like a line of people waiting for a service: the first person to arrive is the first one to be served. In a queue, elements are added at one end (rear) and removed from the other end (front).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693897678063/cb6b5e33-72c2-41ff-85e9-d418b123e075.png align="center")

## Where do we use Queue?

1. **Task Scheduling:** Managing processes and threads in operating systems is a fundamental and pervasive application of queues.
    
2. **Print Queue:** Printers are ubiquitous in homes and offices, making print queues a common and widely recognised use case.
    
3. **Breadth-First Search (BFS):** BFS is a fundamental algorithm used in various domains, including computer graphics, network routing, and more.
    
4. **Message Queues:** With the rise of distributed systems, message queues have gained significant popularity for managing asynchronous communication in web applications, microservices architectures, and cloud computing.
    

## How to use Java's Built-In Functions for Queue Manipulation?

Start by creating a queue using `Queue<Integer> queue = new LinkedList<>();` to store integers. To add elements to the queue, we can either use the `offer` or `add` method. Each call inserts an element at the end of the queue.

### `add()` :

```java
Queue<Integer> queue = new LinkedList<>();
        queue.add(3);
        queue.add(34);
        queue.add(56);
        queue.add(78);
        queue.add(90);
        queue.add(12);
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693908215066/f8f634a3-b853-4192-b958-b271297efaea.png align="center")

### `remove()` :

The `remove()` method removes and returns the head (front) element of a queue. It throws a `NoSuchElementException` if the queue is empty.

```java
System.out.println(queue.remove());
```

Notice how elements pushed first onto the stack are the first to be popped from it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693908597042/8c250f9a-8928-4850-951e-f31fbfd5b505.png align="center")

Now that we've removed all the elements, the stack is empty. If you attempt to remove an element from an empty stack, it will result in an `NoSuchElementException.`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693908783056/692a22b0-53fc-4ea0-9fa7-42e8a826a820.png align="center")

## How Does Internal Implementation of a Queue Work in Java?

The `Queue` interface serves as a foundation for implementing various queue data structures. Much like Java's `Stack` class extends `Vector`, queue implementations utilize underlying data structures and inherit common behaviors from Java's collections framework.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693913569246/61ed87fb-def0-400c-a1f7-e364e94b9e21.png align="center")

The `LinkedList` class can function as a queue by adhering to the `Queue` interface's methods. Internally, it's structured as a doubly linked list, which allows for efficient element addition and removal, aligning with the FIFO principle.

Similarly, the `ArrayDeque` class provides a dynamic array-based implementation for queues, making it suitable for both general queue and double-ended queue (Deque) functionality.

The `PriorityQueue` class offers a priority queue implementation using a binary heap, which sorts elements based on their priorities.

**Think of it this way:** An interface defines what to do, not how to do it.

## How to Create Your Custom Queue in Java?

Let's explore how we can use a pointer to make a custom queue in Java. We'll have just one pointer called `end`, and it will show us where the queue ends.

Initially, when the queue is empty, the single pointer can be set to a specific value, such as 0, to indicate the empty state.

All these empty blocks within the queue represent elements initialized as objects of arrays. Therefore, by default, these elements contain the default value for their data type, which in this case is 0. (I missed this step while creating these images, and it would be a hectic task to recreate them.)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693928622428/6aae7170-e7a0-460a-9996-a581cdd59013.png align="left")

When you `Insert` the first element into the queue, it will be placed at position 0 and pointed by the `end`. Then the pointer is moved forward to the new position.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693929381854/e16ba5e4-200f-4548-b4ac-e7606c61830b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693929478322/cdeacb95-abe2-4547-8be4-3eff68b18bc4.png align="center")

and so on...

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693929642358/dd2a9410-e62a-47b8-b8ad-ae64333311b4.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693929675125/1488e321-8776-4b10-9fae-96dda7f2af7e.png align="center")

## How to remove data from the queue?

Suppose this is our queue array, and we want to remove elements from it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693930490746/3bc3bf45-b5ab-4936-b0f1-b58d0336cd6c.png align="center")

We will take out the first element and move all the others one step ahead by doing `data[i-1] = data[i]` for each element in the queue. This process has a time complexity of O(n).

We're also decreasing the value of 'i' by 1, like `i--`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693930902111/221a1c70-4881-437e-9cbf-63dd8ffd1c2d.png align="center")

### Custom class:

```java
public class CustomQueue {
    protected int[] data;
    private static final int DEFAULT_SIZE = 10;
    int end = 0;

    public CustomQueue() {
        this(DEFAULT_SIZE);
    }

    public CustomQueue(int size) {
        this.data = new int[size];
    }
    public boolean isFull(){
        return end == data.length;//end is at last index
    }
    public boolean isEmpty(){
        return end == 0;
    }

    public boolean insert(int item){
        if(isFull()){
            return false;
        }
        data[end++] = item;
        return true;
    }
    public int remove() throws Exception{
        if(isEmpty()){
            throw new Exception("Queue is Empty");
        }
        int removed  = data[0];
        //shift the elements towards head
        for (int i = 1; i < end; i++){
            data[i-1] = data[i];
        }
        end--;
        return removed;
    }
    public int front() throws Exception{
        if(isEmpty()){
            throw new Exception("Queue is Empty");
        }
        return data[0];
    }

    public void display(){
        for(int i = 0; i < end; i++){
            System.out.print(data[i]+" ");
        }
        System.out.println("End");
    }

}
```

### Main class:

```java
public class QueueMain {
    public static void main(String[] args) {
        CustomQueue queue = new CustomQueue(10);
        queue.insert(3);
        queue.insert(34);
        queue.insert(56);
        queue.insert(78);
        queue.insert(90);
        queue.insert(12);

        queue.display();
        System.out.println(queue.remove());
        queue.display();
    }
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693933439648/b34544bf-4890-47ac-96db-9643f9095d5b.png align="center")

## What is a circular queue?

A circular queue, (circular buffer or a ring buffer), is a fixed-size, continuous collection of elements. It is called "circular" because when elements are dequeued (removed), the space they occupy becomes available for new elements, and the queue's front and rear pointers wrap around to the beginning of the queue if they reach the end.

![Circular Queue in data structure - Shiksha Online](https://www.shiksha.com/online-courses/articles/wp-content/uploads/sites/11/2022/11/image-30.png align="center")

Try to grab this example to understand how elements are inserted into a circular queue.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693980238873/68b62732-926a-478f-986f-b61807410afb.png align="center")

## Why do we use circular queues?

Circular queues are advantageous when you need efficient space usage, continuous data flow, and a way to avoid resizing issues. They are ideal for cyclic and streaming data scenarios.

## How to create your custom circular queue in Java?

Let's gain a basic understanding of how we will utilize two-pointers to create a custom circular queue in Java. To illustrate this concept, imagine an array that we'll use to simulate a circular queue. (Remember that an array is the underlying structure of a circular queue, so don't be confused by the illustrations where both array and circular queues are used interchangeably to represent elements.)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693977624719/b6135e5f-1c9b-4d7a-801e-b18c8a4a797e.png align="center")

We will use two pointers, `front` and `end`, to transform this array into a circular queue.

## How to insert an item in the circular queue?

Both pointers are at index 0 of this circular queue. When we enqueue (insert) 3, the insertion takes place at the end, which in this case is 0, so the element will be placed at position 0.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693980503722/9bff2144-1058-4a90-a52c-cd4060c8cc74.png align="center")

We then increment our `end` pointer. If we have to enqueue again, we will fill it from the `end` in the circular queue.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693981073630/f3b29ea7-7a97-4fb3-b3aa-3bb60b1102d2.png align="center")

Just increase the `end` and enqueue the element, and so on...

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693982536775/d1ebad49-3f2a-4aa3-b116-2c970c389cb8.png align="center")

That brings us to the logic during the insertion phase:

```java
data[end] = item; 
end++;
```

## How to remove an item from a circular queue?

Suppose initially we have a full circular queue, and we want to dequeue (remove) an element. We will simply increase the `front` pointer by 1.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693997703916/4b1590f9-0053-49e3-aa9b-9b1451c7a708.png align="center")

If we have to dequeue more elements, we perform the same process by incrementing the `front` pointer for each dequeue operation.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693997940630/215b104b-00bd-4c99-9d3d-21a71e8872ff.png align="center")

But wait, 3 is not removed, and neither are 34 nor 56. So, why are we saying we have removed them?

We only consider what is between the `front` and `end` pointers. All the elements outside of this range will be overridden when we add new elements to the queue.

**Now, here's the real challenge:** If we have removed some elements and we want to insert new ones after the `end` pointer, how do we traverse back to index 0? If we simply increase the pointer, it will go out of bounds.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693999515075/be999daa-2420-4ecf-b4da-f72cd0360d44.png align="center")

![Archery Funny GIFs | Tenor](https://media.tenor.com/h7VogB-CBXgAAAAM/bow.gif align="center")

So, how do we traverse back to index 0 then?

We use the modulo operation (%), For example, if we have `end` % `size` (5 % 5), it equals 0, and we are back at index 0, (6 % 5) equals 1. This technique allows us to seamlessly move through the circular queue without going out of bounds.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693999609216/809de29e-9900-4e76-b3d4-96d84f377cef.png align="center")

You will always read your array starting from the front, so it would be 78, 90, 12, and then 40.

### Custom CircularQueue:

```java
public class CircularQueue {
        protected int[] data;
        private static final int DEFAULT_SIZE = 10;
        protected int end = 0;
        protected int front = 0;
        private int size = 0;


        public CircularQueue() {
            this(DEFAULT_SIZE);
        }

        public CircularQueue(int size) {
            this.data = new int[size];
        }
        public boolean isFull(){
            return size == data.length;
        }
        public boolean isEmpty(){
            return size == 0;
        }
    public boolean insert(int item){
        if(isFull()){
            return false;
        }
        data[end++] = item;
        end = end % data.length;
        size++;
        return true;
    }
    public int remove() throws Exception{
        if(isEmpty()){
            throw new Exception("Queue is Empty");
        }
        int removed  = data[front++];
        front = front % data.length;
        size--;
        return removed;
    }

    public int front() throws Exception{
        if(isEmpty()){
            throw new Exception("Queue is Empty");
        }
        return data[front];
    }
    public void display(){
            if (isEmpty()){
                System.out.println("Empty");
                return;
            }
            int i = front;
        do{
            System.out.print(data[i] + " -> ") ;
            i++;
            i %= data.length;
        } while(i !=end);
        System.out.println("END");
    }
}
```

**Understanding code:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693992067226/174c09a7-4096-4f79-a95f-d4b597699569.png align="center")

Since when checking `isFull()`, we were using pointers, in the case of a circular queue, we can't write `end == data.length` because its index will be continuously changing. Instead, we use the condition:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693992432171/93f2f4c3-c85f-4606-a6b0-be01909a9614.png align="center")

### CircularQueue Main:

```java
public class QueueMain {
    public static void main(String[] args) throws Exception {
        CircularQueue queue = new CircularQueue(5);
        queue.insert(3);
        queue.insert(34);
        queue.insert(56);
        queue.insert(78);
        queue.insert(90);
        queue.insert(12);

        queue.display();
        System.out.println(queue.remove());
        queue.insert(39);
        queue.display();
    }
}
```