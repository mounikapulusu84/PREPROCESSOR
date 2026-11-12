# MY PREPROCESSOR

## Objective

To develop a C preprocessor tool named `mypreprocessor` that reads a C source file, performs comment removal, file inclusion, and macro substitution, and generates an expanded `.i` file.

## Features

1. **Comment Removal**

   - Removes single-line comments (`//`).
   - Removes multi-line comments (`/* */`).

2. **File Inclusion**

   - Identifies `#include` directives.
   - Replaces the include line with the contents of the specified file.

3. **Macro Substitution**

   - Supports simple macros.
   - Supports macros with arguments.
   - Replaces macro names with their defined values.

## Technologies Used

- C Programming
- GCC Compiler
- Ubuntu
- Makefile

## Project Files

- `main.c`
- `comment_removal.c`
- `file_inclusion.c`
- `macro_handler.c`
- `Makefile`

## Compilation

make

## Execution

./mypreprocessor sample.c

## Output

After successful execution, an output file with `.i` extension is generated.

Example

inputfile.c  ->  inputfile.i

## Clean

make clean

## Concepts Used

- File Handling
- Pointers
- Command-Line Arguments
- Modular Programming
- Macros
