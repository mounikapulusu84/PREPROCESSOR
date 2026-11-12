# C Preprocessor

## Project Overview

The C Preprocessor is a modular application developed using the C programming language. It processes C source files and generates a corresponding `.i` output file before compilation.

The project implements essential preprocessing operations, including comment removal, header file inclusion, and macro substitution.

The main objective is to understand how preprocessing works and implement its basic functionality through modular programming and file handling.

## Features

- **Command-Line Input:** Accepts a C source filename as a command-line argument.
- **Comment Removal:** Removes single-line (`//`) and multi-line (`/* */`) comments while preserving code structure.
- **File Inclusion:** Processes local header files and incorporates their contents into the output.
- **Object-Like Macros:** Supports macro definitions such as `#define PI 3.14`.
- **Function-Like Macros:** Supports parameterized macros such as `#define SQUARE(x) ((x)*(x))`.
- **Nested Macro Expansion:** Supports nested function-like macro expansion.
- **Macro Undefinition:** Supports the `#undef` directive.
- **Output Generation:** Generates a corresponding `.i` file containing the processed source code.
- **Error Handling:** Handles invalid arguments, missing input files, and invalid directives.

## Project Structure

```text
C-Preprocessor/
│
├── main.c
├── preprocessor.c
├── preprocessor.h
├── comment_removal.c
├── file_inclusion.c
├── macro_handle.c
├── makefile
│
├── header.h
├── inputfile.c
└── README.md
```

## Module Description

| File | Description |
|---|---|
| `main.c` | Handles command-line arguments and output file generation. |
| `preprocessor.c` | Controls the overall preprocessing operations. |
| `preprocessor.h` | Contains header declarations, macros, and structure definitions. |
| `comment_removal.c` | Removes comments from the input source file. |
| `file_inclusion.c` | Handles local header file inclusion. |
| `macro_handle.c` | Defines, expands, and removes macros. |
| `makefile` | Automates compilation and project cleanup. |

## Technologies Used

- Programming Language: C
- Compiler: GCC / CC
- Development Environment: Linux
- Build Tool: Makefile
- Concepts: File Handling, String Handling, Pointers, Dynamic Memory Allocation, Modular Programming, and Preprocessing Directives.

## Compilation

Clone or download the project and navigate to its directory.

Build the project using:

```bash
make
```

This generates the executable:

```text
mypreprocessor
```

## Execution

Run the program by providing a C source file as a command-line argument:

```bash
./mypreprocessor inputfile.c
```

The program generates:

```text
inputfile.i
```

## Example

Input file (`inputfile.c`):

```c
#include <stdio.h>
#include "header.h"

#define NUMBER 10

// Display the message
int main()
{
    printf("%s\n", PROJECT_NAME);
    printf("Number = %d\n", NUMBER);

    return 0;
}
```

Generated output (`inputfile.i`):

```c
#include <stdio.h>

int main()
{
    printf("%s\n", "C PREPROCESSOR PROJECT");
    printf("Number = %d\n", 10);

    return 0;
}
```

## Cleaning Generated Files

To remove object files, the executable, and generated `.i` files, run:

```bash
make clear
```

## Learning Outcomes

Through this project, I gained practical experience in:

- Understanding the basic working of a C preprocessor.
- Working with file operations and command-line arguments.
- Implementing comment removal and macro substitution.
- Managing multiple source files using modular programming.
- Using Makefiles to automate compilation.
- Handling errors and testing program functionality.

