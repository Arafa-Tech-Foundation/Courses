# Module 2: Functions and Control Structures in Lua
## Lesson: Working with Strings and Logic in Lua

Lua is a versatile programming language that can be used for a variety of tasks, from game development to web development. One important aspect of Lua programming is using strings and logic effectively. In this lesson, we'll explore how to work with strings and logic in Lua, including how to manipulate strings, use logic to make decisions in your code, and more.

## Strings in Lua

Strings are a fundamental part of any programming language, and Lua is no exception. In Lua, a string is a sequence of characters enclosed in quotation marks. There are two main types of strings in Lua: single-quoted strings and double-quoted strings.

```lua
-- Single-quoted string
my_string = 'Hello, world!'

-- Double-quoted string
my_other_string = "Hello, Lua!"
```

One important thing to note is that Lua treats both single-quoted and double-quoted strings the same way. This means that there's no real difference between the two, other than personal preference.

### String Manipulation

One of the most important things you can do with strings in Lua is manipulate them. Lua provides several built-in functions for working with strings, which we'll explore below.

```lua
-- Concatenation
my_string = "Hello"
my_other_string = "world!"
combined_string = my_string .. " " .. my_other_string -- "Hello world!"

-- Length
length_of_string = string.len(my_string) -- 5

-- Substring
substring = string.sub(my_string, 2, 4) -- "ell"

-- Find
location_of_substring = string.find(my_string, "llo") -- 3

-- Replace
new_string = string.gsub(my_string, "l", "L") -- "HeLLo"
```

### String Formatting

Another important aspect of working with strings is formatting. Lua provides several built-in functions for formatting strings, which we'll explore below.

```lua
-- Basic formatting
my_string = "Hello, %s!"
formatted_string = string.format(my_string, "Lua") -- "Hello, Lua!"

-- Numeric formatting
my_numeric_string = "The value is %d."
formatted_numeric_string = string.format(my_numeric_string, 42) -- "The value is 42."

-- Precision formatting
my_pi_string = "Pi is approximately %0.3f"
formatted_pi_string = string.format(my_pi_string, 3.14159265) -- "Pi is approximately 3.142"
```

## Logic in Lua

Another important aspect of Lua programming is logic. Logic is the process of making decisions in your code based on certain conditions. In Lua, this is done using conditional statements, which we'll explore below.

### If Statements

If statements are used to make decisions in your code based on certain conditions. In Lua, if statements are written using the `if` keyword, followed by the condition you want to test, and then the code you want to execute if the condition is true.

```lua
if x > 10 then
  print("x is greater than 10")
end
```

You can also add an `else` statement to your if statement, which will be executed if the condition is false.

```lua
if x > 10 then
  print("x is greater than 10")
else
  print("x is less than or equal to 10")
end
```

### While Loops

While loops are used to repeat code while a certain condition is true. In Lua, while loops are written using the `while` keyword, followed by the condition you want to test, and then the code you want to execute while the condition is true.

```lua
x = 1
while x <= 10 do
  print(x)
  x = x + 1
end
```

### For Loops

For loops are used to repeat code a specific number of times. In Lua, for loops are written using the `for` keyword, followed by a variable and the range of values you want to loop through, and then the code you want to execute each time through the loop.

```lua
for i = 1, 10 do
  print(i)
end
```

## Conclusion

In this lesson, we explored how to work with strings and logic in Lua. We learned how to manipulate strings using built-in functions, format strings using formatting functions, and make decisions in our code using conditional statements and loops. By mastering these concepts, you can become a more proficient Lua programmer and create more powerful applications.

External resources:
- [Lua 5.4 Reference Manual](https://www.lua.org/manual/5.4/)
- [Programming in Lua, Fourth Edition](https://www.lua.org/pil/contents.html)