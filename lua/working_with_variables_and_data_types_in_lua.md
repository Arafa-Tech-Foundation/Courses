# Module 1: Introduction to Lua Scripting
## Lesson: Working with Variables and Data Types in Lua

### Introduction
Variables and data types serve as foundational building blocks to any programming language, and Lua is no exception. In this lesson, we'll cover the basics of working with variables and data types in Lua.

### Variables
Variables allow a program to store and manipulate data. In Lua, variables are created by following the variable name with an equals sign (=), and then assigning a value to the variable:

```lua
-- Example of variable initialization
num_apples = 5
```

In the above example, we assign the value of 5 to the variable `num_apples`. It's important to note that Lua is a dynamically-typed language, which means that you do not need to declare the data type of the variable. Instead, Lua can determine the data type of the variable based on its assigned value.

You can also assign the value of a variable to another variable:

```lua
-- Example of variable assignment
num_oranges = num_apples
```

In the above example, we assign the value of `num_apples` to `num_oranges`. It's important to note that this does not create a copy of `num_apples`, but rather makes `num_oranges` refer to the same value as `num_apples`.

### Data Types
Lua has 8 basic data types. Each data type defines what operations can be performed on the data. These data types are:

- `nil`: A non-value value that represents the absence of a value.
- `boolean`: Two values: `true` and `false`.
- `number`: Represents real numbers (also known as floating-point numbers).
- `string`: Represents a sequence of characters.
- `table`: Represents a collection of key-value pairs.
- `function`: Represents a sequence of statements that can be invoked by other parts of the code.
- `userdata`: Represents an arbitrary C data structure.
- `thread`: Represents an independent thread of execution.

Below are some examples of working with different data types in Lua:

```lua
-- Example of working with 'nil'
my_var = nil
if my_var == nil then
  print("my_var is nil!")
end

-- Example of working with 'boolean'
my_bool = true
if my_bool then
  print("my_bool is true!")
end

-- Example of working with 'number'
my_num = 10.5
print("The value of my_num is " .. my_num)

-- Example of working with 'string'
my_str = "hello"
print(my_str .. " world!")

-- Example of working with 'table'
my_table = {name="John", age=30}
print("My name is " .. my_table.name .. ", and I am " .. my_table.age .. " years old.")
```

### Conclusion
In this lesson, we covered the basics of working with variables and data types in Lua. This is just the beginning, and there is much more to learn. Be sure to check out the resources below for additional reading.

### Resources
- [Lua 5.3 Reference Manual](https://www.lua.org/manual/5.3/)
- [Programming in Lua](https://www.lua.org/pil/)