# vault door 4
## step 1
it is a code where we input and it checks whether input of 1 flag is stored (flag stored in hexa,octa,decimal characters)..we copy each of them put in cyberchef and get code..
causebasically what the code is doing is they check whether the password we typed is same as the one stored in diff frms..we have to convert each of them and get flagg
## what i learnt
using codechef for diff conversions
## other methods
run the code on spyder
passBytes = [None] * 32
myBytes = [
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            '0x55', '0x6e', '0x43', '0x68', '0x5f', '0x30', '0x66', '0x5f',
            '0o142', '0o131', '0o164', '0o63' , '0o163', '0o137', '0o70' , '0o60' ,
            'f' , '8' , 'e' , '1' , 'e' , '0' , '4' , '7' ,
	]

#base10
for i in range(0,8):
	passBytes[i] =  chr(myBytes[i])

#base16
for i in range(8,16):
	#passBytes[i] =  bytearray.fromhex(myBytes[i].replace('0x', '')).decode()
	passBytes[i] =  chr(int(myBytes[i], 16))

#base8
for i in range(16,24):
	passBytes[i] =  chr(int(myBytes[i], 8))

for i in range(24,32):
	passBytes[i] =  myBytes[i]
print("picoCTF{{{}}}".format(''.join(passBytes)))
## refernces
https://captainmich.github.io/programming_language/CTF/Challenge/picoCTF2019/reverse_engineering.html#vault-door-4
print("picoCTF{{{}}}".format(''.join(passBytes))) #
