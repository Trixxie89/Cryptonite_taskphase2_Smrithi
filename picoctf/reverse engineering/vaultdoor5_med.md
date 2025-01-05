# VAULT DOOR 5
## step 1
cyberchef
to get flag->base64->url decode->ascii if needed->flag'
so basically the string in code comes after doing base64 then url encoding to thr=e flag..so we reverse it by
flag->base64->url decode->flag'
## what i learnt
using cyberchef
## other methods
import base64

encoded = 
'JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVmJTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2JTM0JTVmJTYzJTMxJTM0JTYzJTYzJTY1JTMxJTMx'
data = base64.b64decode(encoded).decode('utf-8')
print(data)
data = data.replace('%', ' 0x')
print(data)

ch = data.split(" ")
print(ch)

print('picoCTF{', end = '')
for c in ch:
	if(c != ''):
		print(chr(int(c, 16)), end = '')

print('}\n', end = '')
## references
https://captainmich.github.io/programming_language/CTF/Challenge/picoCTF2019/reverse_engineering.html#vault-door-4
