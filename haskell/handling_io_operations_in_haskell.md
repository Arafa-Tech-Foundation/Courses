# Module 4: Monads and IO Operations

## Lesson 2: Handling IO Operations in Haskell

Welcome to the Handling IO Operations in Haskell lesson of the Monads and IO Operations module! In this lesson, we'll learn how to work with IO operations in Haskell.

### Understanding IO Operations in Haskell

IO (Input/Output) operations in Haskell are used to interact with the outside world, such as reading and writing files or getting user input. Haskell uses a pure functional programming paradigm, which means that all functions are side-effect free. This, however, means that we cannot perform IO operations directly as they have side-effects. Because of this, Haskell uses a special IO type to encapsulate these effects.

The IO type allows us to perform IO operations in a controlled and predictable manner. Essentially, an IO operation is a function that takes some input (such as a file handle or user input), performs some IO operation, and then returns a value. The returned value is not the output of the IO operation itself, but rather a description of how to perform the operation.

### Performing IO Operations in Haskell

Let's take a look at an example of reading a file in Haskell:

```haskell
main = do
    contents <- readFile "example.txt"
    putStrLn contents
```

Here, we are reading the `example.txt` file and storing its contents in the `contents` variable. We then use `putStrLn` to output the contents to the console. Note that since `readFile` returns an IO String, we use the `<-` operator to bind its result into `contents`. This is how Haskell allows us to work with side-effecting operations in a controlled manner.

Similarly, let's take a look at an example of getting user input:

```haskell
main = do
    putStrLn "Please enter your name:"
    name <- getLine
    putStrLn ("Hello, " ++ name ++ "!")
```

Here, we are prompting the user to enter their name using `putStrLn`. We then use `getLine` to read the user input and store it in the `name` variable. Lastly, we use `putStrLn` again to output a greeting message that includes the user's name.

### Chaining IO Operations

In Haskell, we can chain IO operations using the `do` notation. This allows us to perform multiple IO operations in a sequence. For example, let's take a look at an example of reading two files and outputting their contents:

```haskell
main = do
    contents1 <- readFile "file1.txt"
    contents2 <- readFile "file2.txt"
    putStrLn (contents1 ++ "\n" ++ contents2)
```

Here, we first read `file1.txt` and store its contents in `contents1`. We then read `file2.txt` and store its contents in `contents2`. Lastly, we output the contents of both files using `putStrLn`.

### Conclusion

In this lesson, we learned how to handle IO operations in Haskell. We covered the IO type, performing IO operations using `do` notation, and chaining IO operations. By understanding how to work with IO operations, we can interact with the outside world in a controlled and predictable manner.

### Additional Resources

- [Haskell IO Documentation](https://www.haskell.org/tutorial/io.html)
- [Real World Haskell: Chapter 7. Input and Output](http://book.realworldhaskell.org/read/io.html)
