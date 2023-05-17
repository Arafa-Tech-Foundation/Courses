# Module 2: Data Types and Pattern Matching

## Lesson 2: Introduction to Pattern Matching

Welcome to the first lesson of the Data Types and Pattern Matching module! In this lesson, we'll learn about pattern matching in Haskell.

### What is Pattern Matching?

In Haskell, pattern matching is a way to match specific structures within values. It allows us to define functions in terms of patterns, rather than using conditional logic. The most common use of pattern matching in Haskell is with the case expression, which is used to pattern match an expression against a set of alternatives.

### Using Pattern Matching with Lists

One important use of pattern matching is with lists. In Haskell, lists are constructed using two operators, the cons operator (:) and the empty list operator ([]).

Let's take a look at some examples of pattern matching with lists:

```haskell
-- match an empty list
emptyList :: [a] -> String
emptyList [] = "List is empty"

-- match a list with exactly one element
oneElement :: [Int] -> Int
oneElement [x] = x

-- match a list with at least two elements
twoOrMore :: [a] -> [a]
twoOrMore (_:_:xs) = xs
```

Here, we define three functions that pattern match on lists. The first function, `emptyList`, matches an empty list and returns a string. The second function, `oneElement`, matches a list with exactly one element and returns that element. The third function, `twoOrMore`, matches a list with at least two elements and returns the tail of the list.

### Using Pattern Matching with Tuples

Pattern matching can also be used with tuples in Haskell. Tuples are defined using parentheses and commas, for example, `(1, "hello")`.

```haskell
-- match a tuple and return the first element
firstElement :: (a, b) -> a
firstElement (x, _) = x

-- match a tuple and return the second element
secondElement :: (a, b) -> b
secondElement (_, y) = y
```

In this example, we define two functions that pattern match on tuples. The first function, `firstElement`, matches a tuple and returns the first element. The second function, `secondElement`, matches a tuple and returns the second element.

### Pattern Matching with Data Types

One of the most powerful features of pattern matching in Haskell is the ability to pattern match on user-defined data types. We can define pattern matching on data constructors with the `case` expression.

```haskell
data MyType = MyConstructor Int String

myFunc :: MyType -> Int
myFunc x = case x of
             MyConstructor i _ -> i
```

In this example, we define a new data type `MyType` with one data constructor `MyConstructor` that takes an `Int` and a `String`. We then define a function `myFunc` that pattern matches on the data constructor and returns the `Int` field.

### Conclusion

In this lesson, we learned about pattern matching in Haskell. We saw examples of pattern matching with lists, tuples, and user-defined data types using the `case` expression. Pattern matching is a powerful tool for defining functions in terms of patterns, rather than using conditional logic.

### Further Reading

- [Learn You a Haskell - Pattern Matching](http://learnyouahaskell.com/syntax-in-functions#pattern-matching)
- [Haskell Wiki - Pattern Matching](https://wiki.haskell.org/Pattern_matching)
