---
title: "How Arrays work differently in Java?"
seoTitle: "j"
datePublished: Thu Nov 23 2023 06:31:50 GMT+0000 (Coordinated Universal Time)
cuid: clpatfrq200000akzedxw6ii6
slug: how-arrays-work-in-java
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1700720989794/76e5fa74-a314-4a0c-9e85-ab722feb38c2.png
tags: java, array

---

Arrays lets you store multiple similar values under one name. They're efficient for accessing data, save memory space, and make code cleaner by organising related information into a single structure. Arrays also enable easy iteration and passing collections of data to functions.

### How to declare an array?

```java
dataType[] variableName = new dataType[size];
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700511742486/95f036ef-661c-409a-96fd-3a1bbd9e1557.png align="center")

In Java, arrays are treated as objects, these are special kind of object that doesn't have a specific class . Instead, arrays in Java are instances of dynamically created classes, which are created by the Java Virtual Machine (JVM) at runtime. Let's understand it better,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700510725424/deb14f51-8633-4c4d-8d10-3727196af1ac.png align="center")

We will explore the concepts of stack and heap in Java below to better understand their roles in memory management.

### Stack and heap memory

Stack and heap are two different regions of memory used for different purposes:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700512230872/c2f1018e-f44e-4cb3-885a-e8097f410524.png align="center")

When you create an array or an object using `new` in Java, suppose, `int[] marks = new int[5];`, the memory for that array is allocated in the heap.

However, the reference to that memory location (the object) is stored in the stack if `marks` is a local variable within a method.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700556980514/d03edd12-6c05-4797-8b48-2ce76bc35f44.png align="center")

`Declaration:` happens at compile time (in Stack)  
`Initialisation:` happens at run time. (in heap)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700557638289/b68983ef-878b-4ace-a78e-385182325adf.png align="center")

Based on our understanding:

1. Arrays in Java, being a special type of objects, are facilitated by the JVM. Objects, including arrays, reside in the heap.
    
2. **Java Language Specification (JLS)**, says heap objects aren't necessarily continuous.
    

The heap, responsible for dynamic memory allocation, is where memory for classes and array instances is obtained.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700595071026/47afbfd6-8f61-4b31-918c-b635da52ba62.png align="center")

Hence, array objects in Java might not always be contiguous due to their allocation in the heap. It is actually an array of reference variable that is continuous.

You can explore more on this topic by heading to: [Java: Are 1-D arrays always contiguous in memory?](https://stackoverflow.com/questions/10224888/java-are-1-d-arrays-always-contiguous-in-memory)

### Indices of array:

Indices start at 0 for the first element and increment by 1 for each subsequent element. In our array `marks`, `myArray[0]` refers to the first element, `myArray[1]` refers to the second element, and so on.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700559135977/c9fe8bda-db23-403f-b9aa-beac45ed8269.png align="center")

If an `int[]` is not initialised, its values default to 0, while for a `String[]`, the default values are set to `null`.

### `null:`

Null is a special literal or value that can not be assigned to primitive types **(**`int`, `double`, `etc.`) .

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700561907930/b44992b5-1c87-4d29-acca-89ef03e5c612.png align="center")

`null` is used to indicate that a reference type variable doesn't currently refer to any object, while primitive types like `int` cannot hold `null` as they store values directly.

### User Input to Fill Array & Display Output:

Suppose we have an empty array named '`marks`' our goal is to populate it by obtaining input from the user.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700564262818/0d44406d-c342-41b1-b31d-c5815ebe0711.png align="center")

We can fill it up using a `for loop`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700567356131/67f123de-7331-498f-bcf9-417bb8b01c61.png align="center")

We're increasing `i` to systematically access each subsequent element in the `marks` array, beginning from `marks[0]` and then `marks[1]`, `marks[2]`, and onwards, enabling us to fill these array elements with user-provided input.

Similarly, we can use a `for loop` to show elements

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700567584955/1b448168-e01d-4a7d-850a-9d3a1fbac1dd.png align="center")

### Enhanced for loop (for-each loop):

The `for-each` loop makes it easy to traverse arrays and lists without worrying about index numbers. But, it can not be used for getting user input and storing it.

**Syntax:**

```java
for (dataType refernceVariable : arrayName)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700569882803/5ddffbdc-b6a1-40c5-b6a5-5d5124e93360.png align="center")

### toString() method:

`toString()` method is available in all classes, including arrays, it displays entire array at once, which can be handy for debugging or displaying the entire array's content in one go.

In Java, when using prebuilt methods, there's a convention to follow: `ClassName.methodName(variableName)` (variable as argument is passed to the method).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700573296320/94c2e1b6-2401-4857-a32f-2146a39c6e2a.png align="center")

### How these things behave in function ?

In Java, only call by value is used. The reference variable holds the memory address or reference to the object in the heap. When a reference is passed to a method, it's the value of this reference (memory address) that gets copied, not the entire object itself.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700594946654/f7db20d2-6926-4a1d-add7-c0dba4e07a70.png align="center")

This copied reference still points to the same object in memory.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700595565156/c4efe1ae-674a-44f1-ad80-c324403af5db.png align="center")

so, original will also be changed.

### 2D array:

It is an '**array of arrays',** creating a matrix-like structure where elements are organised in rows and columns.

Row is mandatory

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700596739966/5083063d-8259-4a3a-9291-5cfd672d71c2.png align="center")

`arr` is our 2D array, which contains the following elements:

```java

int [][] arr = {
                {1,2,3},
                {4,5,6},
                {7,8,9}
                };
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700603532069/83f2caa3-8dfb-4f8c-aae1-a3e2b67a0b15.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700603751537/32cd4ca2-8448-4897-8315-6300b701f678.png align="center")

### **Accessing Specific Elements in a 2D Array:**

Accessing elements in a 2D array involves using indices to pinpoint and retrieve values stored in rows and columns.

By specifying the row and column index, you can access particular elements within a 2D array.Let's look at the following example.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700604702473/f33e62eb-e46f-459c-ae7e-f9aff7f987ad.png align="center")

A 2D array is an array of arrays. When we declared and initialised a 2D array like `int[][] arr = new int[3][2];`, we are creating an array that contains three arrays (rows), and each of those arrays contains two elements (columns).

The length of the 2D array (`arr.length`) gives you the number of rows in the array. In this case, `arr.length` would be `3` because you've initialised the array to have three rows.

### User Input to Fill 2D Array & Display Output:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700659912762/1259ab88-5d72-4a50-b074-fa06dd3ba014.png align="center")

The outer loop (`for row`) iterates over the rows ,It starts at `i = 0.` Inside the outer loop, there's another loop (`for col`) that iterates over the columns within each row.

It starts at `col = 0` and continues until `col` reaches the number of columns (`cols`) present in each row.

each row can have a different number of columns. Using `arr[row].length` helps us know how many columns each row has.

```java
int[][] arr = { {1, 2, 3}, // row 0 with 3 columns 

{4, 5}, // row 1 with 2 columns 

{6, 7, 8, 9} // row 2 with 4 columns 

};
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700659803198/fcac1d7a-420a-439a-8131-8f53b5ba8ee7.png align="center")