# GDB BABY STEP 1
picoCTF{549698}
## step 1
So here in this challenge I learnt about the gnu debugger it's a power debugging tool and it helps\ Developers to fix bugs in programmes by allowing them to monitor and control programme execution it basically helps them to understand what part of the programme has issue in it and fix the code it also allows them to set break points that is pause the programme in specific places
 that is pause the programme in specific places Helping them to understand how the code works it also helps you to de assemble the code so in order to do this challenge I have to take my Ubuntu Wsl
 so in order to do this challenge I have to take my Ubuntu Wsl And then I understand I downloaded the file given in the question using WGET and then type
 file debugger0_a
 It helps us to understand what type o.... binary file which was sixty four bit
It helps us to understand what type of file it is and I understood that it is an E L F file basically an executable and linkable binary file which was sixty four bit
gdb debugger0_a
This starts the gdb debugger and here our prime target is the main function and there are two types of syntaxes ....el we will be using Intel as its more
 and there are two types of syntaxes that we use for this gdb at and T as well as Intel we will be using Intel as its more Common
 set diassembly -flavour inyel
 diassemble main
 From the de assembling me near the Eax M O V section we find 0X86342 Which is basically the hexadecimal format of the number 549698
 and got flag
 ## what i learnt
 GNU DEBUGGER
 LANGUGES USED IN IT
 HEXADECIMAL FORMAT
 ## other methods 
 NIL
 ## refernces
 https://www.stackzero.net/gdb-baby-step-1/





