# TUNNEL VISION
flag:picoCTF{qu1t3_a_v13w_2020}
## step 1:
so this was a quite a bit of work to do ..i first got the file and it was a kind of like a text bm file..but other apps were not allowing to open it..so i understtood there could be an error in the in the file making..but i didntknw how to fixt it..so i asked my friends and they suggested to edit file with hex editor file..
in that i had to learn a little about bmp file..it starts with bm..and there is a certain syntax for it..an dthis file wasnt following it..inorder to edit ti,the best way rather than learning suntax is to compare it with areal working bmp file..when i compared  i saw first line it was DA BD  in stead of 
that had to wrote 36 00 00 28 00typed that in ..saved .found it was a pic..opened it..it was written ..notflag sorry...i wa stuck again..then my friesnt gave hint that.vhange picdimension..then it clicked that
file image size is very abnormal..so i put it to size 350..not coming(height was 306 i think) it was written in 2nd lined of hxd file..so my i was not able to pinpoint the perfect 
height anf my friend suggested 850..i dont know where she got it..but it worked 
and bingo go the flag..
## aaSTEP 2
