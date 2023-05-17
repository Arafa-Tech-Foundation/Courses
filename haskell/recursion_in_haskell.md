# Module 3: Higher-Order Functions and Recursion

## Lesson 2: Recursion in Haskell

Welcome to the recursion lesson of the Higher-Order Functions and Recursion module. In this lesson, we will cover the basics of recursion in Haskell.

### What is Recursion?

Recursion is a technique whereby a function calls itself during its execution. Recursive functions typically have two cases: a base case and a recursive case. The base case specifies a simple solution to the problem, while the recursive case handles the more complex aspects of the problem by calling the function again.

### Recursion in Haskell: Example

Let's take a look at an example of recursion in Haskell. Here is a recursive function that calculates the factorial of a number:

```haskell
factorial :: Int -> Int
factorial 0 = 1
factorial n = n * factorial (n -1)
```

In this example, we define the factorial function using the two cases of a recursive function. The base case specifies that the factorial of 0 is 1. The recursive case handles the more complicated aspects of the problem by calling the factorial function with `n -1` as its argument.

### Tail Recursion

In some cases, we can optimize a recursive function by using tail recursion. Tail recursion is a special case of recursion where the call to the recursive function is the last operation in the function. In this case, the compiler can optimize the function so that it uses constant stack space.

Here is an example of a factorial function that is optimized for tail recursion:

```haskell
factorial' :: Int -> Int -> Int
factorial' acc 0 = acc
factorial' acc n = factorial' (acc * n) (n -1)

factorial :: Int -> Int
factorial n = factorial' 1 n
```

In this example, we define a factorial' function that takes two arguments: an accumulator to store the factorial and the number to calculate the factorial for. The base case specifies that the factorial is to `acc`. The recursive case handles the more complex aspects of the problem by calling the `factorial'` function with the `acc * n` and `n -1` as its arguments. The `factorial` function calls the `factorial'` function with an initial value of 1 for accumulator and `n` as the number to calculate the factorial for.

### Conclusion

In this lesson, we learned about recursion in Haskell. We looked at an example of a recursive function and how it can be optimized for tail recursion. Haskell is well-suited to recursion, and we can use this technique to write elegant and effective code.

### Resources

- [Haskell Wiki: Recursion](https://wiki.haskell.org/Recursion)
- [Haskell Programming from First Principles: Recursion](http://haskellbook.com/ch06.html)
- [Tail Recursion vs. Accumulation](https://www.cs.nmsu.edu/~rth/cs/cs471/the-fundamentals-haskell.pdf)
