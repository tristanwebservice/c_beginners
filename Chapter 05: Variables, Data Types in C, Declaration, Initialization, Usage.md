# Chapter 05: Variables, Data Types in C, Declaration, Initialization, Usage

## Introduction to Variables and Data Types in C
In C programming, **variables** are used to store data that can be changed during program execution. Each variable has a specific **data type** that determines the kind of data it can hold, how much memory it occupies, and the operations that can be performed on it. Understanding variables and data types is crucial for effective memory management and data manipulation in C.

## Fundamental Data Types in C
C provides several fundamental data types:

- **`int`**: Used for storing integers (whole numbers). Example:
  ```c
  int age = 25; // Declare an integer variable 'age' and initialize it to 25
  ```

- **`float`**: Used for storing single-precision floating-point numbers (decimals). Example:
  ```c
  float height = 5.9; // Declare a float variable 'height' and initialize it to 5.9
  ```

- **`double`**: Used for storing double-precision floating-point numbers, which provide more precision than `float`. Example:
  ```c
  double pi = 3.14159; // Declare a double variable 'pi' and initialize it to 3.14159
  ```

- **`bool`**: Represents boolean values (`true` or `false`). In C, you typically use `#include <stdbool.h>` to use `bool`. Example:
  ```c
  #include <stdbool.h>
  bool isActive = true; // Declare a boolean variable 'isActive' and initialize it to true
  ```

## Enumerated Data Types and Character Representation
- **Enumerated Data Types**: These allow you to define a variable that can hold a set of predefined constants. Example:
  ```c
  enum Day { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };
  ```

- **Character Representation**: The `char` data type is used to store single characters. Example:
  ```c
  char initial = 'A'; // Declare a char variable 'initial' and initialize it to 'A'
  ```

## Defining and Utilizing Custom Data Types
You can create custom data types using `struct` and `typedef`. This allows you to group different data types into a single unit. Example:
```c
struct Rectangle {
    float length; // Length of the rectangle
    float width;  // Width of the rectangle
};

typedef struct Rectangle Rect; // Create a new type 'Rect' for the Rectangle struct
```

## Precision Output: Mastering Format Specifiers with `printf`
The `printf` function is used to display variables with specific formatting. Format specifiers control how data is presented. Common specifiers include:
- `%d` for integers
- `%f` for floats
- `%lf` for doubles
- `%c` for characters
- `%s` for strings

Example:
```c
int age = 25;
float height = 5.9;
printf("Age: %d, Height: %.1f\n", age, height); // Display age and height with one decimal place
```

## Rectangle Calculations: Area and Perimeter with Variable Manipulation Example
You can perform calculations using variables. For a rectangle, the area and perimeter can be calculated as follows:
```c
#include <stdio.h>

int main() {
    float length = 10.0; // Length of the rectangle
    float width = 5.0;   // Width of the rectangle
    float area = length * width; // Calculate area
    float perimeter = 2 * (length + width); // Calculate perimeter

    printf("Area: %.2f, Perimeter: %.2f\n", area, perimeter); // Display results
    return 0;
}
```

## Understanding Command Line Arguments: `argc`, `argv`
Command line arguments allow you to pass information to your program when it is executed. The `main` function can accept two parameters: `argc` (argument count) and `argv` (argument vector). Example:
```c
#include <stdio.h>

int main(int argc, char *argv[]) {
    printf("Number of arguments: %d\n", argc); // Display the number of arguments
    for (int i = 0; i < argc; i++) {
        printf("Argument %d: %s\n", i, argv[i]); // Display each argument
    }
    return 0;
}
```
