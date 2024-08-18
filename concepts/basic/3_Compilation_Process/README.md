# Compiling a C Program: Behind the Scenes

The compilation process transforms C source code into machine-readable code. Since C is a mid-level language, it requires a compiler to convert it into executable code that can run on a machine.

The C program goes through the following stages during compilation:

1. **Preprocessing**
2. **Compilation**
3. **Assembly**
4. **Linking**

## How to Compile and Run a C Program?

To compile and run a C program, we need a compiler and a code editor. Below is an example on an Ubuntu machine with the GCC compiler.

### Step 1: Creating a C Source File
First, we create a C program using an editor and save the file as `hello_world.c`.

Write a simple "Hello, World!" program and save it.

### Step 2: Compiling Using the GCC Compiler
We use the following command in the terminal to compile our `hello_world.c` source file:

```bash
$ gcc hello_world.c -o hello_world
```

Or use this below command to view the compilation process:

```bash
$ gcc -Wall -save-temps hello_world.c -o hello_world
```


You can pass various options to the GCC compiler to perform different tasks, such as:
- The option **`-Wall`** enables all compiler warning messages. It's recommended to generate more optimized code.
- The option **`-o`** specifies the output file name. Without this option, the compiler will generate an executable named `a.out`.

If there are no errors, the executable for the C program will be created.

### Step 3: Running the Program
Once the compilation is done, an executable file is generated, which can be run using the following command:

```bash
$ ./hello_world
```

This will execute the program, and the output will be displayed in the terminal.

---

## What Happens During the Compilation Process?

A compiler translates a C program into an executable file. This transformation involves four key phases:

### 1. Preprocessing
This is the initial phase, where the source code is preprocessed to:
- Remove comments.
- Expand macros.
- Include header files.
- Handle conditional compilation.

The preprocessed output is saved as `hello_world.i`. You can view it in your file's directory

In this file:
- Macros like `add(a, b)` are expanded.
- Comments are removed.
- The `#include <stdio.h>` statement is replaced with the contents of the `stdio.h` file.


### 2. Compiling
The next step is to compile the preprocessed file (`hello_world.i`), which generates an intermediate output file in assembly language (`hello_world.s`). This file contains assembly-level instructions. You can view it in your file's directory:


### 3. Assembling
The assembler converts the assembly code (`hello_world.s`) into an object file (`hello_world.o`). This object file contains machine-level instructions. At this point, external function calls (e.g., `printf()`) remain unresolved. You can view it in your file's directory


### 4. Linking
In this final phase, the linker resolves all function calls and external references, linking them to their definitions. It also adds some additional code required for the program's startup and shutdown, like handling command-line arguments.

You can verify this by checking the size of the object file and the executable file using the following commands:

You'll notice that the executable file is larger due to the extra code added by the linker.

---

## Viewing Intermediate Files

To generate and view all intermediate files during compilation, use the following command:

```bash
$ gcc -Wall -save-temps hello_world.c -o hello_world
```

This command will create files like `hello_world.i` (preprocessed code), `hello_world.s` (assembly code), and `hello_world.o` (object code) in the current directory, along with the final executable.

---

This step-by-step guide helps you understand the entire process of compiling a C program, from writing the code to generating the final executable.

---