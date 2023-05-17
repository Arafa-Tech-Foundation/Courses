# Module 5: File I/O and Exception Handling in C++ 
## Lesson: Exception Handling in C++

When working with C++, it is important to consider potential errors that can occur in code execution. Exception handling is a programming construct that enables you to handle error conditions and gracefully recover from errors that occur during program execution. 

C++ provides a mechanism for handling exceptions using three keywords – try, catch, and throw. Exception handling enables the programmer to check for errors that can occur in the code. If there are errors that occur during runtime, the exception mechanism will ensure that the rest of the program is unaffected by the error. 

### Basic Exception Handling 
In C++, the simplest form of exception handling involves using the try-catch block. The try block is used to enclose the code that raises an exception. If that code raises an exception, the corresponding catch block is executed. 

The general syntax for a basic try-catch block is as follows: 

```
try {
    // Block of code to try
}
catch(ExceptionType e) {
    // Handle exception here 
}
```

For example, let’s say we have a function that divides two numbers: 

```
int divide(int numerator, int denominator) {
    if(denominator == 0) {
        throw "Error: cannot divide by zero";    
    }
    return (numerator / denominator);
}
```

In this function, we check if the denominator is zero. If it is, the function raises an exception using the throw statement, which throws an error message. We can handle this exception using a try-catch block: 

```
try {
    int result = divide(10, 0);
    cout << "Result is " << result << endl;
}
catch(const char* message) {
    cerr << message << endl;
}
```

In this example, when we attempt to divide by zero, the divide() function will throw an exception with the error message "Error: cannot divide by zero". Since we are handling the exception using a catch block, the program will catch the exception and display the error message. 

### Multiple Catch Blocks 
There may be situations where you want to handle different types of exceptions differently. This is where multiple catch blocks come in. An exception can take multiple catch blocks, each one of which is specialized in handling a specific type of exception. 

For example: 

```
try {
    // Some code that could throw different types of exceptions
}
catch(Type1 e) {
    // Handle Type1 Exception here
}
catch(Type2 e) {
    // Handle Type2 Exception here
}
catch(...) {
    // Handle all other types of Exception here
}
```

In this example, the first catch block catches exceptions of Type1, the second catch block catches exceptions of Type2 and the third catch block catches all other types of exceptions. 

### Standard Exceptions 
C++ has a set of standard exceptions that represent common error conditions. The following are some examples of standard exceptions in C++: 

- std::exception - This is the base class for all standard exceptions.
- std::logic_error - This exception is thrown when there is a logic error in the program.
- std::runtime_error - This exception is thrown when there is a runtime error in the program.

Let’s modify our divide() function to throw one of the standard exceptions, std::runtime_error: 

```
int divide(int numerator, int denominator) {
    if(denominator == 0) {
        throw std::runtime_error("Error: cannot divide by zero");
    }
    return (numerator / denominator);
}
```

In this example, we are throwing an instance of std::runtime_error with the error message "Error: cannot divide by zero". To catch this exception, we can use a catch block that catches std::runtime_error: 

```
try {
    int result = divide(10, 0);
    cout << "Result is " << result << endl;
}
catch(std::runtime_error& e) {
    std::cerr << "Runtime Error: " << e.what() << std::endl;
}
```

std::runtime_error has a member function what() that returns a const char* containing the description of the error. 

### External Resources 
- [Exception Handling in C++ - GeeksforGeeks](https://www.geeksforgeeks.org/exception-handling-c/)
- [Exception Handling - C++ Documentation](https://en.cppreference.com/w/cpp/language/exceptions) 

### Conclusion 
Exception handling is an important programming construct in C++. It gives developers a way to handle errors in a graceful and controlled way. By using try-catch blocks and throwing exceptions, you can make your programs more robust and reliable.