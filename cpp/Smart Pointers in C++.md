# Module 6: Memory Management in C++
## Lesson: Smart Pointers in C++

When dealing with dynamic memory allocation in C++, it is important to make sure that memory is properly allocated and deallocated. One way to do this is through the use of smart pointers.

### What are Smart Pointers?

A smart pointer is a class that provides automatic memory management for objects, specifically those allocated dynamically. Smart pointers ensure that the object they point to is automatically deleted when the smart pointer is no longer in use or when the scope of the smart pointer ends.

Smart pointers provide a safer and more convenient alternative to traditional dynamic memory allocation methods in C++, such as using `new` and `delete` to allocate and deallocate memory.

### Types of Smart Pointers

There are three types of smart pointers in C++: unique_ptr, shared_ptr, and weak_ptr.

#### Unique_ptr

A `unique_ptr` is a smart pointer that owns and manages the object it points to. A `unique_ptr` cannot be copied, but can be moved. When the `unique_ptr` is deleted, the object it points to is also automatically deleted.

```c++
#include <memory>
#include <iostream>

int main()
{
    std::unique_ptr<int> up(new int(5));
    std::cout << *up << std::endl;
    // Output: 5

    // using move to transfer ownership
    std::unique_ptr<int> up2 = std::move(up);
    std::cout << *up2 << std::endl;
    // Output: 5
    // up is now a null pointer

    return 0;
    // up2 is automatically deleted, which also deletes the int it points to
}
```

#### Shared_ptr

A `shared_ptr` is a smart pointer that allows multiple pointers to point to the same object. A reference count is kept to track how many pointers point to the object, and the object is deleted when the reference count reaches zero.

```c++
#include <memory>
#include <iostream>

int main()
{
    std::shared_ptr<int> sp1(new int(5));
    std::shared_ptr<int> sp2 = sp1;

    std::cout << *sp1 << " " << *sp2 << std::endl;
    // Output: 5 5

    sp1.reset();

    std::cout << *sp2 << std::endl;
    // Output: 5
    // sp1 is deleted, but sp2 still points to the same object

    return 0;
    // sp2 is automatically deleted, which also deletes the int it points to
}
```

#### Weak_ptr

A `weak_ptr` is a smart pointer that points to an object that is owned by a `shared_ptr`. A `weak_ptr` does not increment the reference count, so it does not keep the object alive. However, it can be used to check if the object still exists or to retrieve a `shared_ptr` to the object.

```c++
#include <memory>
#include <iostream>

int main()
{
    std::shared_ptr<int> sp(new int(5));
    std::weak_ptr<int> wp = sp;

    std::cout << wp.expired() << std::endl;
    // Output: 0
    // sp still exists, so wp is not expired

    sp.reset();

    std::cout << wp.expired() << std::endl;
    // Output: 1
    // sp no longer exists, so wp is expired

    return 0;
}
```

### Using Smart Pointers

To use a smart pointer, simply create an instance of the desired type of smart pointer and pass in a pointer to the dynamically allocated object.

```c++
#include <memory>
#include <iostream>

int main()
{
    std::unique_ptr<int> up(new int(5));
    std::shared_ptr<int> sp(new int(5));
    std::weak_ptr<int> wp = sp;

    std::cout << *up << " " << *sp << " " << *wp.lock() << std::endl;
    // Output: 5 5 5

    return 0;
}
```

### Advantages of Smart Pointers

Smart pointers provide several advantages over traditional dynamic memory allocation methods. These advantages include:

- Automatic memory management
- No need for manual memory deallocation
- Safer than raw pointers
- More convenient than traditional dynamic memory allocation methods

### Conclusion

Smart pointers provide a safer and more convenient alternative to traditional dynamic memory allocation methods in C++. With the use of smart pointers, you can be sure that memory is properly allocated and deallocated, without the need for manual memory management.