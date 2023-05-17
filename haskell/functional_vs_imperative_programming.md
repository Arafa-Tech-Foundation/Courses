# Module 1: Introduction to Functional Programming

## Lesson 4: Functional vs Imperative Programming

Welcome to the first lesson of the Introduction to Functional Programming module! In this lesson, we'll learn the differences between functional programming and imperative programming.

### Imperative Programming

Imperative programming is a programming paradigm in which we tell the computer how to do things step-by-step. It emphasizes how a program should execute a certain task. In imperative programming, we have variables that can be changed as the program runs. The state of the program is usually closely tied to the order in which statements are executed.

Here's an example of an imperative program that finds the maximum value in an array of integers:

```python
def find_max(arr):
    result = arr[0]
    for i in range(1, len(arr)):
        if arr[i] > result:
            result = arr[i]
    return result
```

This program achieves its goal, but the focus is on how the program accomplishes it. The for loop relies on the mutable variable `result` to keep track of the max value.

### Functional Programming

Functional programming is a programming paradigm where we focus on what we want to accomplish, rather than how to do it. In functional programming, we use immutable data and functions instead of mutable state and imperative control structures. Functions in functional programming don't have any side effects such as changing the state of variables, and they always return a value.

Here's an example of a functional program that finds the maximum value in an array of integers:

```python
def find_max(arr):
    return max(arr)
```

This program simply delegates the task of finding the maximum value to the built-in `max` function. The focus is entirely on what we want to accomplish: finding the max value.

### Advantages of Functional Programming

Functional programming has several advantages over imperative programming:

- Readability: functional programs are often easier to read and understand because they are declarative.
- Maintainability: functions are usually smaller and do one thing well, making it easier to test and maintain the code.
- Parallelism: because functional programming avoids mutable state, it can make parallel programming easier and less error-prone.

## Conclusion

In this lesson, we learned about the differences between functional programming and imperative programming. We saw that functional programming is based on immutable data and functions, whereas imperative programming relies on mutable state and control structures. We also discussed some of the advantages of functional programming, including readability, maintainability, and parallelism.

### Additional Resources

- [Functional Programming Principles in Scala on Coursera](https://www.coursera.org/learn/progfun1)
- [Functional Programming in JavaScript on Udacity](https://www.udacity.com/course/functional-programming-in-javascript--ud1037)
