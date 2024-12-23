# buffer_overflow_0

**Flag:** `picoCTF{ov3rfl0ws_ar3nt_that_bad_ef01832d}`

How you approached the challenge:

- step 1

```
Observerd the code and saw that the buffer size was 16.
```
![image](https://github.com/user-attachments/assets/2f3108ac-0d09-41f0-9341-a280cc4c9d54)
- step 2

```
Since buffer was limited to 16 characters of input and also becuase I knew these kind of questions from previous ctfs, I inputted a huge input which gave me the flag
```

![image](https://github.com/user-attachments/assets/d98a4db8-b7bb-41b4-a75a-5215ebfe65e2)

What you learned through solving this challenge:

1. tracing a program properly and finding vulnaribilities

Other incorrect methods you tried:

- I think I tried to run the program vuln.c which wasn't even running properly

References

- 
