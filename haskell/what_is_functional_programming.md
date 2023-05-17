# Module 1: Introduction to Functional Programming

## Lesson 1: What is Functional Programming?

Welcome to the first lesson of the Introduction to Functional Programming module! In this lesson, we'll learn about the basics of functional programming and why it's becoming more popular in modern programming.

### What is Functional Programming?

Functional programming is a programming paradigm that emphasizes immutability, purity, and higher-order functions. Instead of relying on mutable data structures and side-effects, functional programming focuses on using functions to transform data in a predictable and transparent manner. Programs written in a functional style are often more concise, modular, and easier to reason about than those written in an imperative or object-oriented style.

### Key Concepts in Functional Programming

#### Immutability

In functional programming, immutability means that once a value is created, it cannot be changed. This ensures that there are no side-effects or surprises in the program. Instead of modifying existing values, functions create new values based on the old ones.

#### Purity

A pure function is a function that has no side effects and always returns the same output for a given input. Pure functions are predictable and easy to reason about, since they do not depend on external state and cannot modify it.

#### Higher-Order Functions

A higher-order function is a function that either takes one or more functions as arguments, or returns a function as its result. Higher-order functions are a key feature of functional programming, and they allow us to compose and abstract functionality in powerful ways.

### Functional Programming in Action

Here's a simple example of a function written in a functional style:

```javascript
const double = (x) => x * 2;

const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = numbers.map(double);

console.log(doubledNumbers); // [2, 4, 6, 8, 10]
```

In this example, we define a higher-order function `double` that multiplies a number by 2. We then use the `map` method to create a new array that contains each number in the `numbers` array doubled.

## Conclusion

In this lesson, we learned about functional programming and its key concepts. We discussed immutability, purity, and higher-order functions, and how they can be used to write more concise and modular code. We also saw an example of functional programming in action, and how it can be used to transform data in a predictable and transparent way. If you'd like to learn more about functional programming, check out the resources below!

### Additional Resources

- [Functional Programming Concepts in Depth](https://www.freecodecamp.org/news/functional-programming-concepts-in-depth/) by FreeCodeCamp
- [An Introduction to Functional Programming](https://maryrosecook.com/blog/post/a-practical-introduction-to-functional-programming) by Mary Rose Cook
- [JavaScript Functional Programming: Why You Should Care](https://medium.com/@lazlojuly/javascript-functional-programming-why-you-should-care-7cbbc842f451) by Lazlo Hollyfeld
