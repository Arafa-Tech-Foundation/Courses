# Module 6: Memory Management in C++

## Lesson: Dynamic Memory Allocation in C++

### Introduction
Memory management is an essential part of programming languages. In some cases, you may know the exact amount of memory required for your program, but in most cases, it may be difficult to determine the exact size of memory that is required. This is when dynamic memory allocation comes into play. Dynamic memory allocation allows us to allocate memory during runtime, as opposed to allocating memory during compilation. C++ provides several dynamic memory allocation operations that allow creating data structures of varying size dynamically.

### Dynamic Memory Allocation in C++
C++ provides two operators for dynamic memory allocation - `new` and `delete`. 

#### The `new` Operator
The `new` operator allocates memory and returns a pointer to the starting address of the allocated memory. The following syntax is used to allocate memory using the `new` operator:

```
pointer_variable = new data_type;
```

Here, `data_type` refers to the data type of the variable to be allocated, and `pointer_variable` is the pointer that will point to the allocated memory.

Let's consider the following code example:

```
int* ptr = new int;
*ptr = 10;
```

In the above code, we have declared an integer pointer `ptr` and allocated memory for an integer using the `new` operator. We also assigned a value of 10 to the memory allocated using the pointer `ptr`. 

#### The `delete` Operator
The `delete` operator deallocates the memory allocated using the `new` operator, making it available for future use. The following syntax is used to deallocate memory using the `delete` operator:

```
delete pointer_variable;
```

Here, `pointer_variable` refers to the pointer that was allocated memory using the `new` operator. 

It is important to note that if we do not deallocate the memory using the `delete` operator, we can run into memory leaks, which can cause significant problems when working with large programs. 

Let's consider the following code example:

```
int* ptr = new int;
*ptr = 10;
delete ptr;
```

In the above code, we allocated memory for an integer using the `new` operator, assigned a value of 10 to the allocated memory using the pointer `ptr`, and then deallocated the memory using the `delete` operator. 

### Best Practices
When working with dynamic memory allocation, there are a few best practices that should be followed to prevent issues related to memory leaks.

#### Avoid Memory Leaks
Memory leaks occur when we allocate memory using the `new` operator but fail to deallocate the memory using the `delete` operator. To avoid memory leaks, we must make sure to deallocate memory for all of our dynamically allocated memory using the `delete` operator.

#### Use Arrays Properly
Allocating memory for arrays is quite similar to allocating memory for individual variables. However, when we allocate memory for an array, we must deallocate the entire array as opposed to only deallocating a single element of the array. 

#### Use Pointers Carefully
Dynamic memory allocation requires the use of pointers, which can be complicated. It is important to use pointers carefully and correctly to prevent issues with our dynamically allocated memory. 

### Conclusion
Dynamic memory allocation is an essential aspect of programming, especially when working with data structures of varying sizes. C++ provides two operators, `new` and `delete`, that allow us to allocate and deallocate memory during runtime. It is important to follow best practices when working with dynamic memory allocation to prevent memory leaks and other issues. 

### External Resources
- [GeeksforGeeks: Dynamic Memory Allocation in C++](https://www.geeksforgeeks.org/new-and-delete-operators-in-cpp-for-dynamic-memory/)
- [cplusplus.com: Dynamic Memory Management](https://www.cplusplus.com/doc/tutorial/dynamic/)