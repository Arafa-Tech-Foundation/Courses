# Module 2: Control Structures in C++
## Lesson: Loops in C++

Loops are an essential programming construct that allow developers to execute a block of code repeatedly based on a set of conditions. In C++, there are three types of loops: `while`, `do-while`, and `for`. In this lesson, we'll explore each of these loops and discuss their use cases, syntax, and best practices.

### The while Loop

The `while` loop is the simplest type of loop in C++. It continues to execute a block of code as long as a specified condition is true. Here's the basic syntax of a `while` loop:

```
while (condition)
{
    // code block to execute while condition is true
}
```

Let's look at an example. Suppose we want to print all even numbers between 0 and 10. We can use a `while` loop to achieve this:

```cpp
int i = 0;
while (i <= 10)
{
    if (i % 2 == 0) // check if i is even
    {
        std::cout << i << std::endl; // print i
    }
    i++; // increment i
}
```

In this code, we initialize `i` to 0 and use a `while` loop to keep printing even numbers until `i` reaches 10. We use the `if` statement to check if `i` is even, and if it is, we print it to the console. We then increment `i` by 1 in each iteration of the loop.

### The do-while Loop

The `do-while` loop is similar to the `while` loop, but with one key difference: the loop executes at least once, even if the condition is false. Here's the basic syntax of a `do-while` loop:

```
do
{
    // code block to execute at least once
}
while (condition);
```

Let's modify our previous example to use a `do-while` loop instead:

```cpp
int i = 0;
do
{
    if (i % 2 == 0) // check if i is even
    {
        std::cout << i << std::endl; // print i
    }
    i++; // increment i
}
while (i <= 10);
```

In this code, we use a `do-while` loop to print even numbers between 0 and 10. Since we increment `i` before checking the condition, the loop always executes at least once, even if `i` is initially greater than 10.

### The for Loop

The `for` loop is a more complex loop construct that combines the initialization, condition, and incrementation of a loop variable into a single line of code. Here's the basic syntax of a `for` loop:

```
for (initialization; condition; increment)
{
    // code block to execute repeatedly
}
```

Let's modify our previous example one more time to use a `for` loop:

```cpp
for (int i = 0; i <= 10; i++)
{
    if (i % 2 == 0) // check if i is even
    {
        std::cout << i << std::endl; // print i
    }
}
```

In this code, we use a `for` loop to print even numbers between 0 and 10. We initialize `i` to 0, specify the condition as `i <= 10`, and increment `i` by 1 in each iteration of the loop. Note that the `for` loop eliminates the need to declare the loop variable outside of the loop, as we did with the `while` and `do-while` loops.

### Best Practices for Loops

- Always specify a clear exit condition for your loops to prevent infinite loops.
- Use the `while` loop for simple looping conditions that are evaluated before the code is executed.
- Use the `do-while` loop when you need to execute a loop at least once, regardless of the condition.
- Use the `for` loop when you need to initialize a loop variable, specify a condition, and increment the variable in a single line of code.
- Avoid modifying loop variables inside the loop block.
- Avoid nesting too many loops, as this can reduce the performance of your application.

### Conclusion

Loops are a fundamental programming construct that allow developers to execute a block of code repeatedly based on a set of conditions. In C++, we have three types of loops: `while`, `do-while`, and `for`. When writing loops, it's important to specify a clear exit condition, choose the right type of loop for the situation, and avoid modifying loop variables inside the loop block. By following these best practices, you can write efficient and reliable loops in your C++ applications.

### External Resources

- [C++ Loops (w3schools.com)](https://www.w3schools.com/cpp/cpp_while_loop.asp)
- [C++ While Loop Tutorial With Examples (programiz.com)](https://www.programiz.com/cpp-programming/while-loop)
- [C++ for Loop Explained (guru99.com)](https://www.guru99.com/cpp-for-loop.html)