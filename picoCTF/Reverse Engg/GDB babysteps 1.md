# Challenge name

**Flag:** `picoCTF{549698}`

How you approached the challenge:

- step 1

```
So after catting the file and finding absolutely nothing, I tried to look at the first hint which was to use the gdb debugger. So I did that and installed gdb and ran

'gdb debugger0_a'
which gave me:
```
```
aadi@Aadi:/mnt/c/Users/aadis/Downloads$ gdb debugger0_a
GNU gdb (Ubuntu 12.1-0ubuntu1~22.04.2) 12.1
Copyright (C) 2022 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from debugger0_a...
(No debugging symbols found in debugger0_a)
```

- step 2

```
Very little knowledge of GDB and this question seemed very hard after some analyzing so I asked gemini to help me out here and along with the provided hint about main i figured out about the disassemble main command which gave me the following output:
```


```
(gdb) disassemble main
Dump of assembler code for function main:
   0x0000000000001129 <+0>:     endbr64
   0x000000000000112d <+4>:     push   %rbp
   0x000000000000112e <+5>:     mov    %rsp,%rbp
   0x0000000000001131 <+8>:     mov    %edi,-0x4(%rbp)
   0x0000000000001134 <+11>:    mov    %rsi,-0x10(%rbp)
   0x0000000000001138 <+15>:    mov    $0x86342,%eax
   0x000000000000113d <+20>:    pop    %rbp
   0x000000000000113e <+21>:    ret
End of assembler dump.
```

```
Since the question involved figuring out what is in the eax register, I saw the hex value near %eax and converted it to decimal as mentioned in the question giving me the required flag which I wrapped in picoCTF{}
```
![image](https://github.com/user-attachments/assets/ddaafc83-a250-48d5-8442-3d2a14a46f8d)


What you learned through solving this challenge:

1. A little bit of how gdb debugger/gnu compiler works


Other incorrect methods you tried:

- trying to comprehend nothing from catting the file

References
-
