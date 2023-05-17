# Module 1: Introduction to Functional Programming

## Lesson 3: First Program in Haskell

Welcome to the first lesson of the Introduction to Functional Programming module! In this lesson, we will learn how to write our first program in Haskell.

### What is Haskell?

Haskell is a purely functional programming language, which means that it uses expressions and functions to compute values instead of statements and side effects. It is a lazy, strongly typed and statically typed language. One of the great advantages of Haskell is its strong type system and advanced type inference features, which help to reduce errors in code.

### Hello World in Haskell

To write our first program in Haskell, let's start with a classic "Hello World" example:

```haskell
main :: IO ()
main = putStrLn "Hello, World!"
```

Here, we define a main function that performs the action of printing the string "Hello, World!" to the console using the putStrLn function. The `:: IO ()` in the first line is a type signature for the main function that indicates it is an IO action with no return value.

### Exploring the Syntax

Now a little bit about syntax:

- Every function in Haskell is defined by an equation.
- Each equation has a left-hand side and a right-hand side, separated by an equals sign.
- Haskell is a statically typed language which means every type must be known at compile-time.
- The type of a function determines how it can be used in other expressions.

### Writing a Simple Program

Now let's write a simple program to calculate the sum of squares of the first ten positive integers using the `sum` and `map` functions:

```haskell
main :: IO ()
main = do
    let squared = map (\x -> x * x) [1..10]
        result = sum squared
    print result
```

Here, we create a variable "squared" using the map function to square the numbers from 1 to 10, and then sum these squared values to produce the final result.

### Conclusion

In this lesson, we learned how to write our first program in Haskell, explored some of the syntax and type system, and wrote a simple program to calculate the sum of squares of the first ten positive integers. Haskell is a powerful language that offers many advanced features that make it great for developing high-quality software and solving complex problems.

### External Resources

- [Haskell Programming from First Principles](http://haskellbook.com/)
- [Learn You a Haskell for Great Good!](http://learnyouahaskell.com/)
- [Haskell WikiBook](https://en.wikibooks.org/wiki/Haskell)
