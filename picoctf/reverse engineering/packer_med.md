# PACKER
## step 1
First I understood this is a binary reverse challenge so basically I have to analyse the binary file without looking at the original source code
Binary file is not human readable it can be only read with a programme in python and its basically a file with binary bits of zero and one
 and its basically a file with binary bits of zero and one
## step 2
So first I did file out to understand what type of file it is and if it is executable or not from that I understood that it was an elf file which is basically executable linkab.... format for running programmes in sys
 which is basically executable linkable format it is the standard binary format for running programmes in sys In simple terms it basically means it is an executable binary file
 ## step 3
 Then I did the command strings out which is used to display human readable text strings from the binary file or even a non txt file so here I am ....inary file and if I am able to get it
 or even a non txt file so here I am trying to find whether the flag is in the Binary file and if I am able to get it But in the in the file we do not find in the output we do not file find the flag but we find a text that the output has a upx executable packer so when I checked and researched it I found out that upf is basically a file compressor so if it is compressed we can also make it decompressed
 we can also make it decompressed
## step 4
So I decided to unpack the file using the command upx -d out So from this the file has a been decompressed and also as it decompressed the flag might also have out of the compression mode then I did the command
 then I did the command
## step 5
Edit the command strings out | Grep "flag" Which basically what it does is that it takes the output of the string S which is basically the strings of human readable text strings and we use and grip flag is to find the text string which contains the word ....we get the output a hexadecimal digit
 text string which contains the word flag we could also type pico ctf if it flag is not present from that we get the output a hexadecimal digit
## step 6
From that we copy the X R December series of numbers I put it in magic cyber chef and it converted it into ascii values and I got the flag
# what i learnt
INARY FILE,ELF FILE,UPX FILE,STRINGS COMMAND,HOW TO DECOMPRESS UPX FILE.
# other methods
can use this command in either icoctf prompt or in our wsl ubuntu...just use wget link address
# references
https://dev.to/yowise/picoctf-2024-packer-5h0l







