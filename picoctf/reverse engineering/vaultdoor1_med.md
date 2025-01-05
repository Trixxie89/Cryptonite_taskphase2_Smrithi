# VAULT DOOR 1
## step 1
First I open the Java programme and view it in vs code in that from that I understood that the length of the programme is basically 32 and the programme is telling what word should be in each index so basically I had to make up the flag by looking at the p....at is zero th index is a second index
 make up the flag by looking at the programme that is zero th index is a second index J and so on or we could just run the.... given below which I got from the net
 J and so on or we could just run the programme given below which I got from the net
# other methods
myPass = [None] * 32

myPass[0]  = 'd'
myPass[29] = 'f'
myPass[4]  = 'r'
myPass[2]  = '5'
myPass[23] = 'r'
myPass[3]  = 'c'
myPass[17] = '4'
myPass[1]  = '3'
myPass[7]  = 'b'
myPass[10] = '_'
myPass[5]  = '4'
myPass[9]  = '3'
myPass[11] = 't'
myPass[15] = 'c'
myPass[8]  = 'l'
myPass[12] = 'H'
myPass[20] = 'c'
myPass[14] = '_'
myPass[6]  = 'm'
myPass[24] = '5'
myPass[18] = 'r'
myPass[13] = '3'
myPass[19] = '4'
myPass[21] = 'T'
myPass[16] = 'H'
myPass[27] = '3'
myPass[30] = '3'
myPass[25] = '_'
myPass[22] = '3'
myPass[28] = 'e'
myPass[26] = '6'
myPass[31] = 'a'

print("picoCTF{{{}}}".format(''.join(myPass)))
## refernces
https://captainmich.github.io/programming_language/CTF/Challenge/picoCTF2019/reverse_engineering.html#vault-door-1




