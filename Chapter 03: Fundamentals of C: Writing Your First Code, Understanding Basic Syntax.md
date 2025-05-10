# Chapter 03: Fundamentals of C: Writing Your First Code, Understanding Basic Syntax

## From Code to Execution
To start programming in C, you first need to create, modify, and save your code. Use a text editor to write your C program. Here’s a simple example that displays your name:

```c
#include <stdio.h> // Include standard input-output library

// Main function - execution starts here
int main() {
    printf("Hello, [Your Name]!\n"); // Print your name to the console
    return 0; // Indicate successful completion
}
```

After writing your code, save the file with a `.c` extension, such as `hello.c`.

## The Build Process
The build process consists of three main steps: compiling, linking, and running your program.

1. **Compiling**: This step translates your C code into machine code. Use a compiler like GCC:

   ```bash
   gcc -c hello.c // Compile hello.c to create an object file
   ```

2. **Linking**: The linker combines your object file with necessary libraries to create an executable. This is often done automatically when you compile:

   ```bash
   gcc -o hello hello.c // Compile and link in one step, creating an executable named hello
   ```

3. **Running**: Execute the compiled program in the terminal:

   ```bash
   ./hello // Run the compiled program
   ```

## Understanding and Resolving Compiler Errors
When compiling your code, you may encounter errors. These can be categorized as:

- **Syntax Errors**: Mistakes in the code structure, such as missing semicolons or mismatched parentheses. The compiler will indicate the line number and type of error.

- **Semantic Errors**: These occur when the syntax is correct, but the code does not make logical sense (e.g., using a variable before it is defined).

### Compiler Warnings
Warnings indicate potential issues in your code that may not prevent compilation but could lead to runtime problems. Always review and address warnings to ensure code quality.

## Linker Errors
Linker errors occur when the compiler cannot find the definition of a function or variable. This often happens if you forget to include a library or if there are typos in function names. To troubleshoot, check your function declarations and ensure all necessary files are included.

## Runtime Errors
Runtime errors happen during program execution, often due to exceptional events like division by zero or accessing invalid memory. To handle these, use error-checking techniques and consider implementing exception handling strategies.

## Identifying and Correcting Logic Errors
Logic errors occur when the program runs without crashing but produces incorrect results. Debugging strategies include:
- **Print Statements**: Use `printf` to display variable values at different points in the program.
- **Step-by-Step Execution**: Use a debugger like GDB to execute your program line by line and inspect variable states.

## Displaying Your Name in C: Practical Example
The earlier example of displaying your name illustrates the fundamental concepts of C programming. Modify the `printf` statement to include your name, and follow the build process to see the output.

## Deep Dive into C Program Structure
Understanding the structure of a C program is crucial:
- **Main Function**: Every C program must have a `main` function, which is the entry point of execution.
- **Blocks**: Code within `{}` braces forms a block, allowing you to group statements.
- **Key Elements**: Essential components include headers (like `#include <stdio.h>`), function definitions, and statements.
