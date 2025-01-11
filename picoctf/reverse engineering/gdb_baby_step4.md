# gdbbabystep4
Step 1: Launch GDB
I started GDB with the target program:

bash
Copy code
gdb debugger0_d
This initialized the debugging session for the executable debugger0_d.

Step 2: List Functions
To get an overview of the program’s functions, I used:

bash
Copy code
info functions
This listed all the functions in the program. The challenge description emphasized that main and func1 were important. Based on the hints, func1 likely contained the multiplication operation.

Step 3: Improve Disassembly Readability
To make the disassembly easier to interpret, I switched the syntax to Intel style with:

bash
Copy code
set disassembly-flavour intel
Intel syntax is more readable for tasks involving assembly code because it explicitly shows the destination operand first and aligns closely with most references.

Step 4: Set Breakpoint
To begin debugging from the start of the program’s execution, I set a breakpoint at main:

bash
Copy code
break main
Step 5: Start the Program
To start the program and pause execution at the main function, I used:

bash
Copy code
run
This command halted execution at the entry point of main.

Step 6: Use the Layout Command
To make the debugging process more visual, I enabled the assembly layout mode with:

bash
Copy code
layout asm
This provided a split-screen view, showing the assembly code as I stepped through the instructions.

Step 7: Step Through the Program
To analyze the execution flow, I used two key commands:

ni (next instruction): Executes the current instruction without stepping into function calls.
si (step into): Steps into the function being called, allowing deeper inspection.
By using si on a call instruction in main, I stepped into func1.

Step 8: Analyze Instructions in func1
Inside func1, I located the following instruction:

asm
Copy code
imul eax, eax, 0x3269
This instruction multiplies the value in the eax register by 0x3269 (hexadecimal) and stores the result back in eax.

Step 9: Convert Hexadecimal to Decimal
The challenge required the constant to be presented in decimal. I used GDB’s print command to convert it:

bash
Copy code
print/d 0x3269
The /d switch converts the hexadecimal value to decimal, revealing the result: 12905.

What I Learned
Stepping Commands in GDB:
ni (step over) and si (step into) allow control over how deeply to debug function calls.
Understanding Assembly Syntax:
Intel syntax is more intuitive for debugging, especially when analyzing operations like imul.
Using GDB Commands:
info functions helps identify relevant functions in a program.
layout asm makes the debugging process more visual and interactive.
Hexadecimal to Decimal Conversion:
GDB’s print command with /d converts values between bases easily.
## refernces
https://www.stackzero.net/gdb-baby-step-4/
