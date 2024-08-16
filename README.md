# What is C?

C is a general-purpose, procedural, low-level programming language used in the development of computer software and applications, system programming, games, and more.

- C language was developed by Dennis M. Ritchie at the Bell Telephone Laboratories in 1972.
- It is a powerful and flexible language that was first developed for the programming of the UNIX operating system.
- C is one of the most widely used programming languages.

C programming language is known for its simplicity and efficiency. It is the best choice to start with programming as it gives you a foundational understanding of programming.

## Why is C Considered a Low-Level Language?

C is considered a low-level language, but it's often described as a "mid-level" language because it has features of both high-level and low-level programming languages.

### Why C is Considered Low-Level:

1. **Memory Management**: C allows direct manipulation of memory through pointers, which is a characteristic of low-level languages. You have to manually allocate and free memory, and you can directly access and manipulate memory addresses.
2. **System Programming**: C is close to the hardware, making it suitable for system programming, such as writing operating systems, drivers, and embedded systems. It provides the ability to perform low-level tasks like bit manipulation, port I/O, and interacting with the CPU.
3. **Minimal Abstraction**: C provides minimal abstraction over the hardware. There are no built-in features for complex data types (like objects in high-level languages) or automatic memory management (like garbage collection).

### Why C is Also Considered Mid-Level:

1. **High-Level Constructs**: C has features of high-level languages, such as functions, loops, conditionals, and basic data structures (arrays, structs). These features make it easier to write complex programs compared to assembly language, which is purely low-level.
2. **Portability**: While C allows low-level access, it is still portable across different platforms, as long as you avoid platform-specific code. This makes C more versatile than languages that are strictly low-level.

## Comparison with Other Languages

- **Low-Level Languages**: Assembly language is an example of a pure low-level language, where you work directly with CPU instructions and have fine-grained control over the hardware.
- **High-Level Languages**: Languages like Python, Java, and JavaScript are considered high-level because they provide extensive abstraction from the hardware. They manage memory automatically, have complex built-in data types, and offer extensive libraries and frameworks.

In summary, C is considered low-level because it provides direct access to memory and hardware, but it also has features of high-level languages, making it versatile for both system programming and application development.

## Difference Between C and C++

C++ was created to add the OOPs concept into C language, so they both have very similar syntax but differ in various ways. Below are some of the main differences between C and C++:

- **Paradigm**: C is procedural, focusing on functions, while C++ supports both procedural and object-oriented programming.
- **OOP Support**: C++ includes classes and objects, enabling features like inheritance and polymorphism, which C lacks.
- **Memory Management**: C uses `malloc()` and `free()`, whereas C++ uses `new` and `delete` for dynamic memory management.
- **Libraries**: C++ has a richer standard library, including the Standard Template Library (STL), while C has a smaller set of libraries.
- **Function Overloading**: C++ supports function overloading (same function name with different parameters), which C does not.

## Writing the First Program in C

The following code is one of the simplest C programs that will help us understand the basic syntax structure of a C program.

```c
#include <stdio.h>

int main() {
  int a = 10;
  printf("%d", a);
  
  return 0;  
}
```

## Applications of C

C is a powerful low-level programming language widely used in various domains. Here are some key applications of C:

1. **Operating Systems Development**: Many operating systems, including Linux, Windows, and macOS, have components written in C due to its efficiency and direct access to hardware.
2. **Embedded Systems**: C is commonly used in embedded systems (e.g., IoT devices, microcontrollers) because of its ability to interact with hardware at a low level.
3. **System-Level Programming**: Drivers, compilers, and interpreters are often written in C due to its performance and closeness to the machine level.
4. **Database Systems**: Databases like MySQL and SQLite are written in C because of its speed and reliability for handling large-scale data operations.
5. **Game Development**: Some game engines use C to achieve high performance, particularly in areas where low-level memory and hardware management is needed.
