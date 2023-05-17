# Module 2: Data Types and Pattern Matching

## Lesson 1: Data Types in Haskell

Welcome to the Data Types lesson of Module 2! In this lesson, we'll learn about the different data types in Haskell and how to work with them.

### Basic Data Types

Haskell has several basic data types:

- Bool: represents a Boolean value, which can be either True or False. Example: `True`
- Char: represents a single character. Example: `'a'`
- Int: represents an integer value. Example: `42`
- Float: represents a floating-point value. Example: `3.14`

### Defining Data Types

We can also define our own data types in Haskell using the `data` keyword. For example, we can define a data type `Person` with two fields - `name` (a string) and `age` (an integer) - like this:

```haskell
data Person = Person {name :: String, age :: Int}
```

We can then create instances of the `Person` data type like this:

```haskell
person1 = Person {name = "John", age = 30}
person2 = Person {name = "Jane", age = 25}
```

### Pattern Matching

Pattern matching is a powerful feature in Haskell that allows us to match values against specific patterns and define behavior based on those patterns. We can use pattern matching to work with data types (both built-in and custom) in Haskell.

For example, let's say we have a data type `Color` that represents a color as a combination of red, green, and blue values. We can define the data type like this:

```haskell
data Color = RGB Int Int Int
```

We can then define a function `brightness` that takes a `Color` value and returns its brightness, which is defined as the sum of its red, green, and blue values:

```haskell
brightness :: Color -> Int
brightness (RGB r g b) = r + g + b
```

Here, the `brightness` function uses pattern matching to extract the red, green, and blue values from the `Color` value and add them together.

### Type Signatures

Haskell is a strongly typed language, which means that every expression has a specific type. We can use type signatures to explicitly specify the type of a function or expression. Type signatures are written using the `::` symbol, like this:

```haskell
exampleFunction :: Int -> String -> [Float]
```

Here, `exampleFunction` is a function that takes an integer and a string as arguments and returns a list of floating-point values.

### Conclusion

In this lesson, we learned about the basic data types in Haskell, how to define our own data types, how to use pattern matching to work with data types, and how to specify the type of a function or expression using type signatures. With these tools, we can start to build more complex programs in Haskell.

### Further Resources

- [Haskell Data Types](https://www.tutorialspoint.com/haskell/haskell_data_types.htm)
- [Haskell Pattern Matching](https://wiki.haskell.org/Pattern_matching)
- [Haskell Type Signatures](https://en.wikibooks.org/wiki/Haskell/Type_signatures)
