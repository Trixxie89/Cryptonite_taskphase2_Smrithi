# VAULT DOOR 6
password must be 32 characters long and each of them is xorred 0x55 and check sif they same
password[i]xor0x55=mybytes[i]
so to find it we do mybyte[i]xor0x55
acc to a xor b xor b =a





## code
hence i fould code from net that did this and got it''we can also do it with cyber chef
passBytes = [None] * 32
myBytes = [
            0x3b, 0x65, 0x21, 0xa , 0x38, 0x0 , 0x36, 0x1d,
            0xa , 0x3d, 0x61, 0x27, 0x11, 0x66, 0x27, 0xa ,
            0x21, 0x1d, 0x61, 0x3b, 0xa , 0x2d, 0x65, 0x27,
            0xa , 0x31, 0x30, 0x30, 0x30, 0x64, 0x61, 0x33,
	]

for i in range(32):
	passBytes[i] =  chr(myBytes[i] ^ 0x55)

print("picoCTF{{{}}}".format(''.join(passBytes)))
## what i learnt
xor special principle
## other method
cyberchef or py code
# refernces
https://captainmich.github.io/programming_language/CTF/Challenge/picoCTF2019/reverse_engineering.html#vault-door-4
