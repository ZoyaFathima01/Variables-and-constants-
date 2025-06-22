# Assembly Lab - Variables and Constants

This lab demonstrates:

- Assigning values to initialized variables
- Using an uninitialized variable to store results
- Simple addition in x86 NASM Assembly
- Debugging with gdb

## Code Summary

- `var1` = 10
- `var2` = 15
- `result` = var1 + var2 ➜ Stored in memory

## How to Compile and Run

```bash
nasm -f elf32 variables.asm -o variables.o
ld -m elf_i386 variables.o -o variables
./variables
