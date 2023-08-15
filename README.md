# ----------------picoCTF--------------------
#
#
`1`
```
Name Chellnge = Reverse                               100 points
Description = 
Try reversing this file? Can ya? I forgot the password to this file. Please find it for me?
Link Chellnge = https://play.picoctf.org/practice/challenge/372?category=3&page=2
```
I downloaded the file and upload in `ida 64-bit` and he asked me to enter the password, but I found the flag :
![](/PNG/1.PNG) 
![](/PNG/2.PNG)
##### picoCTF{3lf_r3v3r5ing_succe55ful_2f0131a4}
##--------------------------------------------------------------

`2`
```
Name Chellnge = Safe Opener                               100 points
Description = 
Can you open this safe? I forgot the key to my safe but this program is supposed to help me with retrieving the lost key. Can you help me unlock my safe? Put the password you recover into the picoCTF flag format like:
picoCTF{password}
Link Chellnge = https://play.picoctf.org/practice/challenge/294?category=3&page=2
```
The file was with the extension `(.java)` I downloaded it and opened it sublime text or notepad
![](/PNG/3.PNG)
In the `openSafe method` it confirms that the value of the password is equal to the value of the variable `encodedkey` and this value is encoded by `base64` and I took it on `cyberchef` and I decoded it and got the flag : 
![](/PNG/4.PNG)
##### picoCTF{pl3as3_l3t_m3_1nt0_th3_saf3} 
##--------------------------------------------------------------

`3`
```
Name Chellnge = timer                               100 points
Description = 
You will find the flag after analysing this apk Download here.
Link Chellnge = https://play.picoctf.org/practice/challenge/381?category=3&page=2
```
I downloaded the file and it was in (.apk) format but I did not understand this format I searched for it :
`A file with the APK file extension is a package file used to distribute apps on Google's Android operating system.
APK files are saved in the ZIP format and are typically downloaded directly to Android devices, usually via Google Play, but can also be found on other websites.`
I understood here that it must be extract file and attached to extract tool online :
![](/PNG/5.PNG)
Link of website : https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjQ3pyYtNWAAxU3hf0HHVvtBJkQFnoECA4QAw&url=https%3A%2F%2Fwww.ezyzip.com%2Fextract-apk-files.html&usg=AOvVaw0tLz9UJeYODmv4Trao-VWB&opi=89978449

I searched for how to open or run these files, but I did not find a solution, then it caught my attention to try to read the strings in the files, then I took the file called `AndroidManifest.xml` to `pestudio` and found the Flag there:
![](/PNG/6.PNG)
##### picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}
##--------------------------------------------------------------

`4`
```
Name Chellnge = Bit-O-Asm-1                               100 points
Description = 
Can you figure out what is in the eax register? Put your answer in the picoCTF flag format: picoCTF{n} where n is the contents of the eax register in the decimal number base. If the answer was 0x11 your flag would be picoCTF{17}. Download the assembly dump here.
Link Chellnge = https://play.picoctf.org/practice/challenge/391?category=3&page=2
```
I downloaded the file and opened it with notepad 
![](/PNG/7.PNG)
`30` in hexadecimal == `48` in decimal
then the flag is :
##### picoCTF{48}
##--------------------------------------------------------------

`5`
```
Name Chellnge = file-run2                               100 points
Description = 
Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"? Download the program here.
Link Chellnge = https://play.picoctf.org/practice/challenge/267?category=3&page=2
```
I downloaded the file and opened it with `ida 64-bit` (or in your own way, try to find the strings, for example, through pestudio and search for "pico" and it will show you the flags ) :
![](/PNG/8.PNG)
![](/PNG/9.PNG)
the flag :
##### picoCTF{F1r57_4rgum3n7_be0714da}
##--------------------------------------------------------------

`6`
```
Name Chellnge = Safe Opener 2                               100 points
Description = 
What can you do with this file? I forgot the key to my safe but this file is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
Link Chellnge = https://play.picoctf.org/practice/challenge/375?category=3&page=2
```
I downloaded the file and opened it with `ida 64-bit` then I went to the function called openSafe and found the flag is here :
![](/PNG//10.PNG)
##### picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_3dae8463}
##--------------------------------------------------------------

`7`
```
Name Chellnge = ASCII FTW                               100 points
Description = 
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program. You can download the file from here.
Link Chellnge = https://play.picoctf.org/practice/challenge/389?category=3&page=2
```
I downloaded the file and opened it with `ida 64-bit` and found the flag :
![](/PNG/11.PNG)
##### picoCTF{ASCII_IS_EASY_8960F0AF}
##--------------------------------------------------------------

`8`
```
Name Chellnge = unpackme.py                               100 points
Description = 
Can you get the flag? Reverse engineer this Python program.
Link Chellnge = https://play.picoctf.org/practice/challenge/314?category=3&page=2
```
I downloaded the file and opened it with `VSCode` and I tried to run it 
(Usually there is a problem in running the file and it is that Python does not respond to the library called cryptograghy
-Go to the folder with the basic Python file inside it 
-and open Windows Power Shell 
-and write this command inside it `pip3 install cryptography`
It will running the file easily)
![](/PNG/12.PNG)
![](/PNG/14.PNG)
then I run the file and asked to enter the password
![](/PNG/13.PNG)
Through my reading of the code, I understood that it executes the code inside the flag, so I changed the `exec` function with `print`
![](/PNG/15.PNG)
And I run the code again and the code appeared to me and I found the flag :
![](/PNG/16.PNG)
##### picoCTF{175_chr157m45_5274ff21}
##--------------------------------------------------------------

`9`
```
Name Chellnge = GDB Test Drive                               100 points
Description = 
Can you get the flag?Download this binary (https://artifacts.picoctf.net/c/85/gdbme).
Here's the test drive instructions:
$ chmod +x gdbme
$ gdb gdbme
(gdb) layout asm
(gdb) break *(main+99)
(gdb) run
(gdb) jump *(main+104)
Link Chellnge = https://play.picoctf.org/practice/challenge/273?category=3&page=2
```
I downloaded the file, but this time I uploaded it to my Kali Linux and to note that it gave me instructions that I will follow.
in the First, I opened the terminal and went to the place where the file is located and executed the first command 
![](/PNG/17.png)
This command gives the permissions to execute this file 
![](/PNG/18.PNG)
gdb is the GNU debugger 
![](/PNG/19.PNG)
I searched for the problem and sorry I did not find a solution, but I understood what this does He displays the assembly inside the file, I don't think that this will be important to me, but in general we will continue to implement the other of the instructions.
![](/PNG/20.PNG)
It puts breakpoint in *(main+99) in order to start executing from there
![](/PNG/21.PNG)
Executes the assembly code from the breakpoint
![](/PNG/22.PNG)
He jumps to the next address * (Main + 104) and finally prints the flag : 
##### picoCTF{d3bugg3r_dr1v3_197c378a}
##--------------------------------------------------------------

`10`
```
Name Chellnge = patchme.py                               100 points
Description = 
Can you get the flag?
Run this Python program in the same directory as this encrypted flag.
Link Chellnge = https://play.picoctf.org/practice/challenge/287?category=3&page=2
```
The file called `flag.txt.enc` is the file in which the flag is located, but it is encrypted.
The file called `patchme.flag.py` is the file with the code that decrypts the flag 
I tried to run the Python file and give it the encrypted file as a parameter 
![](/PNG/23.PNG)
Mmmm, then I opened the Python file to find the password
![](/PNG/24.PNG)
the correct password = `ak98-=90adfjhgj321sleuth9000`
![](/PNG/25.PNG)
##### picoCTF{p47ch1ng_l1f3_h4ck_f01eabfa}
##--------------------------------------------------------------

