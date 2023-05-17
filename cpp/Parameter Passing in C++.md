# Module 3: Functions and Parameter Passing in C++

## Lesson: Parameter Passing in C++

In C++, when using functions, there are two ways to pass arguments to a function: pass by value and pass by reference. 

### Passing by Value

Passing by value means that a copy of the value is made and passed to the function. This copy resides in a new memory location. Changes made to the value within the function do not affect the original variable that was passed in.

Here is an example of passing by value: 

```c++
#include <iostream>

void increment(int x) {
    x++;
}

int main() {
    int num = 5;
    increment(num);
    std::cout << num << std::endl;  // Output: 5
    return 0;
}
```

In the above example, `num` is passed into `increment` by value. `x` is a copy of `num` with a new memory location. When `x` is incremented, only the copy is affected, not the original `num` variable. 

### Passing by Reference

Passing by reference means that a reference to the original variable is passed to the function. This reference does not create a new copy of the value, and any changes made to the reference within the function will affect the original variable that was passed in. 

Here is an example of passing by reference: 

```c++
#include <iostream>

void increment(int& x) {
    x++;
}

int main() {
    int num = 5;
    increment(num);
    std::cout << num << std::endl;  // Output: 6
    return 0;
}
```

In the above example, `num` is passed into `increment` by reference. `x` is not a copy, but rather a reference to the original `num` variable. When `x` is incremented, the original `num` variable is also affected. 

### Const Parameters

Sometimes it is useful to pass a variable into a function as a constant, which means that the function cannot change the value of the variable. 

Here is an example of using a const parameter: 

```c++
#include <iostream>

void print(const std::string& str) {
    std::cout << str << std::endl;
}

int main() {
    std::string message = "Hello, World!";
    print(message);
    return 0;
}
```

In the above example, `message` is passed into `print` by const reference. This means that the `print` function cannot modify the value of `message` within the function. 

### Default Parameters

In C++, it is possible to give parameters default values. If a default value is given, the argument can be omitted when the function is called, and the default value will be used instead. 

Here is an example of using default parameters: 

```c++
#include <iostream>

void print_profile(std::string name, int age = 30, std::string job = "Teacher") {
    std::cout << "Name: " << name << std::endl;
    std::cout << "Age: " << age << std::endl;
    std::cout << "Job: " << job << std::endl;
}

int main() {
    std::string my_name = "Alice";
    int my_age = 25;
    print_profile(my_name);  // Output: Name: Alice, Age: 30, Job: Teacher
    print_profile(my_name, my_age);  // Output: Name: Alice, Age: 25, Job: Teacher
    print_profile(my_name, my_age, "Engineer");  // Output: Name: Alice, Age: 25, Job: Engineer
    return 0;
}
```

In the above example, `print_profile` takes in three parameters, but the second and third parameters have default values. When `print_profile` is called with only one argument, the default values are used for the second and third parameters. 

### External Resources

- [C++ Functions - GeeksforGeeks](https://www.geeksforgeeks.org/functions-in-cpp/)
- [Function Parameters - cplusplus.com](http://www.cplusplus.com/doc/tutorial/functions2/)