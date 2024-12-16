# MINIRSA
## step 1
import binascii
c=1220012318588871886132524757898884422174534558055593713309088304910273991073554732659977133980685370899257850121970812405700793710546674062154237544840177616746805668666317481140872605653768484867292138139949076102907399831998827567645230986345455915692863094364797526497302082734955903755050638155202890599808146919581675891411119628108546342758721287307471723093546788074479139848242227243523617899178070097350912870635303707113283010669418774091018728233471491573736725568575532635111164176010070788796616348740261987121152288917179932230769893513971774137615028741237163693178359120276497700812698199245070488892892209716639870702721110338285426338729911942926177029934906215716407021792856449586278849142522957603215285531263079546937443583905937777298337318454706096366106704204777777913076793265584075700215822263709126228246232640662350759018119501368721990988895700497330256765579153834824063344973587990533626156498797388821484630786016515988383280196865544019939739447062641481267899176504155482

n=1615765684321463054078226051959887884233678317734892901740763321135213636796075462401950274602405095138589898087428337758445013281488966866073355710771864671726991918706558071231266976427184673800225254531695928541272546385146495736420261815693810544589811104967829354461491178200126099661909654163542661541699404839644035177445092988952614918424317082380174383819025585076206641993479326576180793544321194357018916215113009742654408597083724508169216182008449693917227497813165444372201517541788989925461711067825681947947471001390843774746442699739386923285801022685451221261010798837646928092277556198145662924691803032880040492762442561497760689933601781401617086600593482127465655390841361154025890679757514060456103104199255917164678161972735858939464790960448345988941481499050248673128656508055285037090026439683847266536283160142071643015434813473463469733112182328678706702116054036618277506997666534567846763938692335069955755244438415377933440029498378955355877502743215305768814857864433151287

#from https://riptutorial.com/python/example/8751/computing-large-integer-roots
def nth_root(x, n):
    # Start with some reasonable bounds around the nth root.
    upper_bound = 1
    while upper_bound ** n <= x:
        upper_bound *= 2
    lower_bound = upper_bound // 2
    # Keep searching for a better result as long as the bounds make sense.
    while lower_bound < upper_bound:
        mid = (lower_bound + upper_bound) // 2
        mid_nth = mid ** n
        if lower_bound < mid and mid_nth < x:
            lower_bound = mid
        elif upper_bound > mid and mid_nth > x:
            upper_bound = mid
        else:
            # Found perfect nth root.
            return mid
    return mid + 1

for i in range(4000):
   st=("{:x}".format(nth_root(c+i*n,3)))
   if "7069636f" in st:  # "pico" in hex
      print(st)
      print(binascii.unhexlify(st))
## step 2
So here in rsa rsa is a type of encryption that relies on number theory so here we jogged between plain text and cypher text by using rules based on these rules we generate two keys 1 is the public key which contains e and N 
And the next is the private key which contains smaller D which is kept as secret while the public key is shared with everyone the formula iss
c=M raisedto e %N 
M is the plaintext C is the ciphertext E is shared to everyone and its the public exponent and N is the public key which is shared to everyone so here 
So here P and Q are two very very lar....sically two thousand forty eight bits
N=P*q
$=p-1*q-1
1<e<$
gcd(e,$)=1
d=(e*d)%$=1
N IS >>>>>>>>>>>>>>
So the problem arises when when M raise to E is slightly less than N then C equal to M raise to E so attacker can easily get M by taking the eth root of C without using the secret key D the second problem arises if M raise to E is slightly greater than N then CM raised to E N so here they can get the answer by taking the 8th root of C
so in Q its teh first case n
So here In the question in the programme we have nth root function which basically finds the nth root of any given large number so in the main programme we have for I in range of 4000 so I will get the values from zero to 3999 and the next proline is
 and the next proline is Is to convert each letter each letter each so the next slide is basically to find the cube root of the cap letter N while making smaller smaller manipulations to the value CCI star and CI * N because the values might slightly change
 might slightly change So here first we find the cube root when E is equal to three and then we find when the C is slightly manipulative when I start to basically we are trying to find the multiples of it and then
 and then And then we get the hexadecimal format of it of the root and we cheque and this 706-9636 F is basically the hexadecimal of Pico and by converting the cube root into pav we are converting the cube root value into hexa and checking if that peco string is there in that hexa hexa route
 hexa route Root if it is there then it means we got a flag and hence we print St as well as South T which is the hexa value as well as print the unthinked which gives us the plain text of a flag 
as hexadecimal is similar to ciphertext..the plaintext might be in hexa decimal,ans we need to reconvert the plaintext to hexadecimal to check if there is pico..and then
unhexify it to get flag..so it basically finds the root and finds the hexadecimal form of it ie
if num=255
it finds hexadecimal value ff and checks if this 706963f is in ff..ie if pico i in this root ka hexadecimal..if ys..prints the flag..as oico in that

der and got flag 
![Screenshot 2024-12-17 012830](https://github.com/user-attachments/assets/75e2b2ef-b148-45a3-9f57-88913ad8f78b)
## what i learnt
what is RSA,PUbluc key,PRIVATE KEY,HEXAFORMATTING,RSA FORMULA,SAW CODE TO FIND ROOT IF LARGER NUMS,HEXA VALUE OF PICO CTF
## other methods
can run this file in terminal
with python filename
## references
https://youtu.be/B2Dz1KMSFho?si=PQ1Bbbx74O5kmEsQ

