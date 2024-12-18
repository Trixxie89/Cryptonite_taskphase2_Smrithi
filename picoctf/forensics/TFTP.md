# TFTP
## step 1
codebind@Smrithi:/mnt/c/amma$ steghide --help
steghide version 0.5.1

the first argument must be one of the following:
 embed, --embed          embed data
 extract, --extract      extract data
 info, --info            display information about a cover- or stego-file
   info <filename>       display information about <filename>
 encinfo, --encinfo      display a list of supported encryption algorithms
 version, --version      display version information
 license, --license      display steghide's license
 help, --help            display this usage information

embedding options:
 -ef, --embedfile        select file to be embedded
   -ef <filename>        embed the file <filename>
 -cf, --coverfile        select cover-file
   -cf <filename>        embed into the file <filename>
 -p, --passphrase        specify passphrase
   -p <passphrase>       use <passphrase> to embed data
 -sf, --stegofile        select stego file
   -sf <filename>        write result to <filename> instead of cover-file
 -e, --encryption        select encryption parameters
   -e <a>[<m>]|<m>[<a>]  specify an encryption algorithm and/or mode
   -e none               do not encrypt data before embedding
 -z, --compress          compress data before embedding (default)
   -z <l>                 using level <l> (1 best speed...9 best compression)
 -Z, --dontcompress      do not compress data before embedding
 -K, --nochecksum        do not embed crc32 checksum of embedded data
 -N, --dontembedname     do not embed the name of the original file
 -f, --force             overwrite existing files
 -q, --quiet             suppress information messages
 -v, --verbose           display detailed information

extracting options:
 -sf, --stegofile        select stego file
   -sf <filename>        extract data from <filename>
 -p, --passphrase        specify passphrase
   -p <passphrase>       use <passphrase> to extract data
 -xf, --extractfile      select file name for extracted data
   -xf <filename>        write the extracted data to <filename>
 -f, --force             overwrite existing files
 -q, --quiet             suppress information messages
 -v, --verbose           display detailed information

options for the info command:
 -p, --passphrase        specify passphrase
   -p <passphrase>       use <passphrase> to get info about embedded data

To embed emb.txt in cvr.jpg: steghide embed -cf cvr.jpg -ef emb.txt
To extract embedded data from stg.jpg: steghide extract -sf stg.jpg
codebind@Smrithi:/mnt/c/amma$ steghide extract -sf picture1.bmp -p DUEDILIGENCE
steghide: could not extract any data with that passphrase!
codebind@Smrithi:/mnt/c/amma$ steghide extract -sf picture2.bmp -p DUEDILIGENCE







^[ll


steghide: could not extract any data with that passphrase!
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$ l
picture1.bmp*  picture2.bmp*  picture3.bmp*
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$
codebind@Smrithi:/mnt/c/amma$ steghide extract -sf picture3.bmp -p DUEDILIGE
NCE
wrote extracted data to "flag.txt".
codebind@Smrithi:/mnt/c/amma$ cat flag.txt
picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}
codebind@Smrithi:/mnt/c/amma$ picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}
So first I downloaded Wireshark is a network protocol analyzer it helps to capture and inspect data travelling across the network it also helps us to capture real time network traffic so in this flag with the help of the tutorial I download a bioshock in order to inspect whether hidden data is transferred through the http protocols but we see it's not so basically what have what happened in this challenge is that in the question we had downloaded five files which includes three picture files of the form JPG and we have two types of text files and one dot DEB file so in this what we understand is that our flag has been hidden in one of the 3 pictures and we have to get them so 1st we use the rot 13 translator in order to convert the text in the introduction file as well as the plan file so in the plan file they give us the password to get the flag from the picture so to get the flag I have to open my wsl ubuntu terminal and use steghide
Steakhite is basically a steganography tool to hide data with the help of other images or audios it basically helps us to hide secret files like it can be text or doc or in this case the flag inside a pic or an audio and after hiding the The picture or audio file we have to enter the password in order to get the secret data so in that document of plan we had got that due diligence is the password so we use the command stehide extract -sf picture1.bmo -p DUEDILIGENCE 

We use this command in order to get the flag it's basically the command which helps us to get the secret data if it's there in that picture and get the flag so here 
 In this question the flag is hidden picture three so when we type the command with respect to picture three we get the flag and that's how we solve this problem

![Screenshot 2024-12-17 023140](https://github.com/user-attachments/assets/4961ed63-ef3c-4606-a82b-32017822e1a1)

## what i learnt
wireshark,steghide,rot13(language letters shifted  by 13 sopaces),steghide commands
## other methods
none
## refernces

https://youtu.be/VmSgalNMw_Y?si=ntpD1w1HIbOQ429t

























