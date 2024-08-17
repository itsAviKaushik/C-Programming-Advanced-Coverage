Printing a `Hello World` on screen is one of the best program to get started with any programming language. It is a first step towards learning any programming language. There are multiple way to print the Hello World or any string in C. You can skip some of them to avoid confusion, in case you are a beginner.

You can print the Hello World in C with the following ways:

### 1. Standard `printf()` Method:
```c
#include <stdio.h>  // Required for printf function

int main() {
    // Prints "Hello, World!" and a new line to the console
    printf("Hello, World!\n");
    return 0;  // Program executed successfully
}
```

### 2. Using `puts()`:
```c
#include <stdio.h>  // Required for puts function

int main() {
    // puts automatically adds a new line after the string
    puts("Hello, World!");
    return 0;  // Program executed successfully
}
```

### 3. Using `putchar()`:
```c
#include <stdio.h>  // Required for putchar function

int main() {
    const char *str = "Hello, World!\n";  // String to be printed
    // Loop through each character in the string and print it
    while (*str) {
        putchar(*str++);  // Print the current character and move to the next
    }
    return 0;  // Program executed successfully
}
```

### 4. Without Standard Library (using `write()` system call):
```c
#include <unistd.h>  // Required for the write system call

int main() {
    // write takes three arguments: file descriptor, string to write, and length of string
    // 1 is the file descriptor for stdout
    write(1, "Hello, World!\n", 14);
    return 0;  // Program executed successfully
}
```

### 5. Using `fprintf()` with `stdout`:
```c
#include <stdio.h>  // Required for fprintf function

int main() {
    // fprintf allows more control over the output stream, here we use stdout
    fprintf(stdout, "Hello, World!\n");
    return 0;  // Program executed successfully
}
```

### 6. Using `fputs()`:
```c
#include <stdio.h>  // Required for fputs function

int main() {
    // fputs prints the string but does not add a new line automatically
    fputs("Hello, World!\n", stdout);  // stdout is the standard output stream
    return 0;  // Program executed successfully
}
```

### 7. Printing ASCII values with `printf()`:
```c
#include <stdio.h>  // Required for printf function

int main() {
    // Print "Hello, World!" by using the ASCII values of each character
    printf("%c%c%c%c%c%c%c%c%c%c%c%c%c\n", 
           72, 101, 108, 108, 111, 44, 32, 87, 111, 114, 108, 100, 33);
    return 0;  // Program executed successfully
}
```

### 8. Using recursion:
```c
#include <stdio.h>  // Required for putchar function

// Recursive function to print the string character by character
void print_hello(int index) {
    char str[] = "Hello, World!\n";  // String to be printed
    if (str[index] != '\0') {  // Base case: stop when the null terminator is reached
        putchar(str[index]);  // Print the current character
        print_hello(index + 1);  // Recursive call to print the next character
    }
}

int main() {
    print_hello(0);  // Start printing from index 0
    return 0;  // Program executed successfully
}
```

### 9. Using macros:
```c
#include <stdio.h>  // Required for printf function

#define HELLO_WORLD "Hello, World!\n"  // Define a macro for the string

int main() {
    // Use the macro to print "Hello, World!"
    printf(HELLO_WORLD);
    return 0;  // Program executed successfully
}
```
