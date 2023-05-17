# Module 4: Object-Oriented Programming in C++

## Lesson: Inheritance and Polymorphism in C++

Inheritance is an important concept in object-oriented programming. It allows one class to inherit properties and methods from another class. Polymorphism, on the other hand, allows objects of different types to be treated as if they were of the same type.

### Inheritance in C++

Inheritance is the process by which one class can be derived from another class, inheriting properties and behavior from its parent class. The derived class is also known as the child class, while the parent class is also known as the base or superclass.

Inheritance is a powerful mechanism in C++, as it allows you to reuse code that has already been written and tested. This leads to more maintainable and readable code, as well as reduced development time.

To create an inheritance relationship between two classes, use the `class` keyword followed by a colon and the access specifier (`public`, `protected`, or `private`) followed by the name of the parent class:

```c++
class ParentClass {
public:
    void foo() {
        cout << "Hello from ParentClass!" << endl;
    }
};

class ChildClass : public ParentClass {
public:
    void bar() {
        cout << "Hello from ChildClass!" << endl;
    }
};
```

In the example above, `ChildClass` inherits from `ParentClass` using the `public` access specifier. This means that all the members of `ParentClass` that are `public` and `protected` are also accessible from `ChildClass`.

### Polymorphism in C++

Polymorphism is the ability of objects of different types to be treated as if they were of the same type. This makes it possible to write code that works with a wide range of objects, without knowing their exact type at compile time.

In C++, polymorphism is achieved through a combination of inheritance and virtual functions. A virtual function is a member function in a base class that can be overridden by a derived class. When a virtual function is called using a pointer or reference to a base class object, the implementation of the function that is called is determined dynamically at runtime based on the actual type of the object.

To make a function virtual, use the `virtual` keyword in the base class definition:

```c++
class BaseClass {
public:
    virtual void foo() {
        cout << "Hello from BaseClass!" << endl;
    }
};

class DerivedClass : public BaseClass {
public:
    void foo() override {
        cout << "Hello from DerivedClass!" << endl;
    }
};
```

In the example above, `foo()` is a virtual function in `BaseClass` that is overridden in `DerivedClass`. When we call `foo()` on a pointer or reference to a `BaseClass` object, the implementation that is called is determined dynamically based on the runtime type of the object.

### Example Usage

```c++
int main() {
    ParentClass parent;
    ChildClass child;

    parent.foo();   // Output: Hello from ParentClass!
    child.foo();    // Output: Hello from ParentClass!
    child.bar();    // Output: Hello from ChildClass!

    ParentClass* ptr_child = &child;
    ptr_child->foo();   // Output: Hello from DerivedClass!
}
```

In the example above, we create objects of `ParentClass` and `ChildClass`, and call their methods accordingly. We also create a pointer to `ParentClass` that points to the `ChildClass` object, and call the `foo()` method using this pointer. Because `foo()` is a virtual function, the implementation that is called is determined dynamically based on the runtime type of the object pointed to by `ptr_child`.

### External Resources

1. [Inheritance in C++](https://www.geeksforgeeks.org/inheritance-in-c/)
2. [Polymorphism in C++](https://www.geeksforgeeks.org/polymorphism-in-cpp/)