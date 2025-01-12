# vault door 3
flag:picoCTF{jU5t_a_sna_3lpm18gb41_u_4_mfr340}
## step 1
we were given a java code..which basically is there..to print flag..out..so i opened the code in java online compiler ..and it was asking enter vault passwoed..i typed the flag..
given in code(last)..it printed me access denied..so ehat i understto d was tthis flag is being edited in loop of java script and..we should be printing the buffer..after all teh loops to see what change happened..
im not well versed in java..so i found to print we use system.out.println(buffer);
did that and got flag
root@kali:/media/sf_CTFs/pico/vault-door-3# node
> password = "jU5t_a_sna_3lpm1dg347_u_4_mfr54b"
'jU5t_a_sna_3lpm1dg347_u_4_mfr54b'
>
> var i;
undefined
> var buffer = Array(32);
undefined
>
> for (i=0; i<8; i++) {
...     buffer[i] = password.charAt(i);
... }
's'
> for (; i<16; i++) {
...     buffer[i] = password.charAt(23-i);
... }
'n'
> for (; i<32; i+=2) {
...     buffer[i] = password.charAt(46-i);
... }
'd'
> for (i=31; i>=17; i-=2) {
...     buffer[i] = password.charAt(i);
... }
'g'
> console.log("picoCTF{" + buffer.join("") + "}");
picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_7f35db}
## step 2:
## code
root@kali:/media/sf_CTFs/pico/vault-door-3# node
> password = "jU5t_a_sna_3lpm1dg347_u_4_mfr54b"
'jU5t_a_sna_3lpm1dg347_u_4_mfr54b'
>
> var i;
undefined
> var buffer = Array(32);
undefined
>
> for (i=0; i<8; i++) {
...     buffer[i] = password.charAt(i);
... }
's'
> for (; i<16; i++) {
...     buffer[i] = password.charAt(23-i);
... }
'n'
> for (; i<32; i+=2) {
...     buffer[i] = password.charAt(46-i);
... }
'd'
> for (i=31; i>=17; i-=2) {
...     buffer[i] = password.charAt(i);
... }
'g'
> console.log("picoCTF{" + buffer.join("") + "}");


picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_7f35db}
![Screenshot 2024-11-07 013621](https://github.com/user-attachments/assets/ef16a9d0-6b06-4a93-a34b-ec743520c084)
## what i learnt:
a new code to print a variable in java:
## other methods:
while entering password i first typed just the string then icoctf for a lot of times
and then realised it wss picoCTF..
## references
https://www.w3schools.com/java/java_variables_print.asp
