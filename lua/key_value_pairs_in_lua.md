# Module 3: Tables and Modules in Lua

## Lesson: Key-Value Pairs in Lua

In Lua, tables are the primary data structure used for grouping related values together. They can be used to represent arrays, dictionaries, objects and other complex data structures. In this lesson, we'll focus on one of the most important features of tables in Lua - the ability to use key-value pairs.

### Key-Value Pairs: Overview

A key-value pair is a set of two connected data items, a key and a value. The key represents what the data is, and the value represents the data that is being stored. In Lua, tables can use key-value pairs to store and retrieve data.

For example, let's say we want to keep track of a set of employees and their salaries. We can use a table to represent this information:

```lua
employee_salaries = {
  ["John"] = 50000,
  ["Jane"] = 60000,
  ["Harry"] = 75000
}
```

In this example, the keys are string values that represent the employees' names, and the values are numeric values that represent their salaries. We can access individual elements of this table using the key:

```lua
print(employee_salaries["John"]) -- Output: 50000
```

### Creating Tables with Key-Value Pairs

Tables in Lua can be created with key-value pairs using the following syntax:

```lua
table_name = {
  [key_1] = value_1,
  [key_2] = value_2,
  ...
  [key_n] = value_n
}
```

Note that the keys can be any type of value in Lua, including numbers, strings, and even other tables.

### Accessing and Modifying Values in Tables

To access the value stored in a table using a key, we simply use the syntax `table_name[key]`. For example:

```lua
print(employee_salaries["Jane"]) -- Output: 60000
```

We can modify the values stored in a table using the same syntax:

```lua
employee_salaries["John"] = 55000
print(employee_salaries["John"]) -- Output: 55000
```

### Iterating Over Key-Value Pairs

We can also iterate over the key-value pairs in a table using a `for` loop. The `pairs` function is used to iterate over the keys and values of a table:

```lua
for key, value in pairs(employee_salaries) do
  print(key .. ": " .. value)
end
```

This will output:

```
John: 55000
Harry: 75000
Jane: 60000
```

### Conclusion

Key-value pairs are a powerful feature of tables in Lua, allowing us to store and retrieve data in a structured and flexible way. By using tables with key-value pairs, we can easily represent complex data structures and iterate over them to perform operations. 

#### External Resources:

- [Lua Tables Tutorial](https://www.lua.org/pil/2.5.html)
- [Lua Tables Tutorial by Dummies.com](https://www.dummies.com/programming/game-development/lua-programming/how-to-use-tables-in-lua-programming/)