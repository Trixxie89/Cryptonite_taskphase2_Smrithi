# GDB BABY STEP3


gdb debugger0_c

Set the disassembly syntax to Intel (preferred for readability):

set disassembly-flavour intel

Step 2: Disassembling and Debugging

2.1 Gathering Initial Information

List all functions in the binary:

info functions

Look for the main function, as it often contains the logic for challenges.

Disassemble the main function:

disassemble main

Analyze the assembly code to identify important instructions. Here, note any constants being moved to memory or registers (e.g., instructions involving RBP - 4).

2.2 Setting Breakpoints and Debugging

Set a breakpoint at the start of the main function:

break main

This halts the program at the first instruction in main.

Start running the program:

run

Switch to assembly layout for better visibility of the program's execution:

layout asm

This displays the assembly instructions alongside the current execution pointer.

Identify the instruction where the EAX register is assigned its final value (e.g., at 0x40111f):

break *0x40111f
continue

The continue command resumes execution until the next breakpoint.

2.3 Inspecting Memory and Registers

Check the value in the EAX register at the breakpoint:

info registers eax

While this shows a value, the challenge hints that it’s stored in memory in little-endian format.

Inspect the relevant memory location (e.g., RBP - 4):

x/4xb $rbp-4
examine Four bytes of data as hexadecimal the officer address is subtracted by four bytes and RBP is the value of the base point

0x7ffc1234:  0x6b  0xc9  0x62  0x22

Reverse the bytes (little-endian representation) to get the correct value:

0x2262c96b

2.4 Constructing the Flag

Format the reversed value into the required flag format:

picoCTF{0x6bc96222}

Submit the flag to complete the challenge.

## what i lrant
comments
## other methods
none
## refernces
https://www.stackzero.net/gdb-baby-step-3/
