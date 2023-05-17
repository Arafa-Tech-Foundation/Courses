# Module 2: Functions and Control Structures in Lua

## Lesson: Working with Functions in Lua

### Introduction

In programming, a function is a group of related statements that performs a specific task. Functions help you break down your code into smaller and more manageable sections, making it easier to read and understand. In this lesson, we will explore how to create and use functions in Lua.

### Defining a Function

In Lua, a function is defined using the `function` keyword followed by the function name and a set of parentheses. Any parameters to be passed into the function are listed inside the parentheses, separated by commas. The body of the function is enclosed in a set of `do` and `end` keywords. Here is an example of a simple function:

```lua
function greet(name)
  print("Hello, " .. name .. "!")
end
```

In this example, we define a function called `greet` that takes an argument `name`. The body of the function simply prints out a greeting with the provided name. 

### Calling a Function

Once a function has been defined, we can call it from elsewhere in our code. To call a function, simply provide the function name followed by any necessary arguments in parentheses. Here is an example of calling the `greet` function we defined earlier:

```lua
greet("Bob")
```

When this code is executed, we will see the following output printed to the console:

```
Hello, Bob!
```

### Returning Values

Functions in Lua can also return values, which can be useful in many situations. To return a value from a function, use the `return` keyword followed by the value or values to be returned. Here is an example of a function that calculates the square of a number and returns the result:

```lua
function square(x)
  return x * x
end
```

We can call this function and assign the returned value to a variable like this:

```lua
local result = square(5)
print(result)
```

In this example, we call the `square` function with an argument of `5`. The value returned by the function (which is `25`) is then assigned to a variable called `result`, which is then printed out to the console. 

### Scope

In Lua, variables can have different scopes depending on where they are defined. A variable defined outside of any function or block is said to have a **global scope** and can be accessed from anywhere in the code. 

However, if a variable is defined inside a function or block, it is said to have a **local scope** and can only be accessed from within that function or block. Here is an example of a function that defines a local variable:

```lua
function myFunction()
  local x = 42
end
```

In this example, the variable `x` has a local scope and can only be accessed within the `myFunction` function. If we try to access `x` from outside the function, we will get an error. 

### Control Structures in Functions 

Control structures such as `if` statements and loops can also be used within functions. Here is an example of a function that uses an `if` statement to determine if a number is even or odd:

```lua
function isEven(x)
  if x % 2 == 0 then
    return true
  else
    return false
  end
end
```

In this example, we use the modulo operator (`%`) to determine the remainder when `x` is divided by 2. If the remainder is 0, we return `true`, indicating that the number is even. Otherwise, we return `false`, indicating that the number is odd.

### Conclusion

Functions are an important part of programming in Lua (and in many other languages). They help you organize your code into more manageable chunks and make it easier to read and understand. In this lesson, we explored how to define and call functions, return values, and use control structures within functions. With these tools, you should be well-equipped to start writing your own functions in Lua.

### External Resources

- [Lua Functions Tutorial](https://www.tutorialspoint.com/lua/lua_functions.htm)
- [Lua Control Structures Tutorial](https://www.tutorialspoint.com/lua/lua_control_statements.htm)