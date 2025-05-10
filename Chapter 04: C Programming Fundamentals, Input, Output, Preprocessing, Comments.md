# Chapter 04: C Programming Fundamentals, Input, Output, Preprocessing, Comments

## Improving Code Readability
Code readability is essential for maintaining and understanding your programs. In C, you can improve readability by using comments. There are two types of comments:

- **Single-Line Comments**: Use `//` to comment out a single line. For example:

  ```c
  // This is a single-line comment
  printf("Hello, World!\n"); // Print greeting
  ```

- **Multi-Line Comments**: Use `/*` to start and `*/` to end a comment that spans multiple lines. For example:

  ```c
  /* This is a multi-line comment
     that explains the following code */
  printf("Hello, World!\n");
  ```

Using comments effectively helps others (and yourself) understand the purpose of your code.

## Preprocessing in C
Preprocessing is the first step in the compilation process, where the preprocessor handles directives that begin with `#`. These directives instruct the compiler to perform specific actions before actual compilation. Key directives include:

- **`#include`**: This directive is used to include header files, which contain declarations for functions and macros. For example:

  ```c
  #include <stdio.h> // Include standard input-output library
  ```

- **`#define`**: This directive defines constants or macros that can be used throughout your code. For example:

  ```c
  #define PI 3.14 // Define a constant for Pi
  ```

Understanding preprocessing helps you manage code dependencies and reuse code effectively.

## Header Files and Libraries
Header files are files that contain declarations for functions and macros. By using the `#include` directive, you can include standard libraries or your own header files to reuse code. For example:

```c
#include <math.h> // Include the math library for mathematical functions
```

This allows you to access a wide range of functions without rewriting code, promoting code reuse and organization.

## Formatted Output
The `printf` function is used to display formatted output in C. It allows you to control how data is presented. The basic syntax is:

```c
printf("format string", arguments);
```

For example:

```c
int age = 25;
printf("I am %d years old.\n", age); // %d is a placeholder for an integer
```

You can use various format specifiers, such as `%d` for integers, `%f` for floating-point numbers, and `%s` for strings, to format your output as needed.

## User Input in C
To read data from the user, you can use the `scanf` function. The basic syntax is:

```c
scanf("format string", &variable);
```

For example, to read an integer from the user:

```c
int age;
printf("Enter your age: "); // Prompt the user
scanf("%d", &age); // Read an integer and store it in the variable 'age'
```

The `&` operator is used to provide the address of the variable where the input will be stored.
