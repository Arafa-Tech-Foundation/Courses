# Module 2: Functions and Control Structures in Lua

## Lesson: Loops in Lua

Loops are a fundamental part of programming and allow us to repeat a certain block of code multiple times until a specific condition is met. This lesson will cover the different types of loops available in Lua, how to use them, and their syntax.

### For Loops

For loops in Lua are used to repeat a block of code for a specific number of times. The basic syntax for a for loop is as follow:

```lua
for variable = startValue, endValue, increment do
    -- code to execute
end
```

The `startValue` is the initial value of the variable, `endValue` is the final value of the variable, and `increment` is the amount the variable changes each iteration. Here's a simple example that prints the numbers 1 to 5:

```lua
for i = 1, 5, 1 do
    print(i)
end
```

Output:

```
1
2
3
4
5
```

Note that the `increment` value can be negative, in which case the `endValue` should be less than the `startValue`. Here's an example that counts down from 5 to 1:

```lua
for i = 5, 1, -1 do
    print(i)
end
```

Output:

```
5
4
3
2
1
```

### While Loops

While loops in Lua are used to repeat a block of code as long as a specific condition is true. The basic syntax for a while loop is as follow:

```lua
while condition do
    -- code to execute
end
```

Here's a simple example that prints the numbers 1 to 5 using a while loop:

```lua
local i = 1
while i <= 5 do
    print(i)
    i = i + 1
end
```

Output:

```
1
2
3
4
5
```

### Repeat-Until Loops

Repeat-until loops in Lua are similar to while loops, but the block of code is executed at least once before the condition is checked. The basic syntax for a repeat-until loop is as follow:

```lua
repeat 
    -- code to execute
until condition
```

Here's a simple example that prints the numbers 1 to 5 using a repeat-until loop:

```lua
local i = 1
repeat
    print(i)
    i = i + 1
until i > 5
```

Output:

```
1
2
3
4
5
```

### Breaking Out of Loops

Sometimes, we want to break out of a loop before the condition is met. We can do that using the `break` keyword. Here's an example that uses a for loop to print the numbers 1 to 5, but breaks out of the loop when the number 3 is reached:

```lua
for i = 1, 5, 1 do
    if i == 3 then
        break
    end
    print(i)
end
```

Output:

```
1
2
```

### Skipping Iterations

Sometimes, we want to skip an iteration of a loop without breaking out of the loop. We can do that using the `continue` keyword. Unfortunately, Lua does not have a built-in `continue` keyword, so we can use a `goto` statement to achieve the same effect. Here's an example that uses a for loop to print the even numbers from 1 to 10:

```Lua
for i = 1, 10 do
    if i % 2 ~= 0 then
        goto continue
    end
    print(i)
    ::continue::
end
```

Output:

```
2
4
6
8
10
```

## Conclusion

Loops are a fundamental part of programming and Lua provides several types of loops to fit our needs: for loops, while loops, and repeat-until loops. We can also use the `break` keyword to break out of a loop and the `goto` statement to skip an iteration. By understanding and using loops effectively, we can write more powerful and efficient code.

### External Resources

- [Official Lua documentation on loops](https://www.lua.org/manual/5.1/manual.html#2.4.5)
- [Lua loops tutorial on tutorialspoint](https://www.tutorialspoint.com/lua/lua_loops.htm)
- [Lua loops tutorial on learnlua.com](https://www.learnlua.com/control-structures/)