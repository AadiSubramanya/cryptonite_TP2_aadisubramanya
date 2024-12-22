# findandopen
**Flag:** `picoCTF{R34DING_LOKd_fil56_succ3ss_494c4f32}`

How you approached the challenge:

- step 1

```
On downloading the tracefile, I could open it with wire shark as it was a network packet file.
Upon glancing through different lines many of which seemed to be bunched, I found an odd one which was not bunched.
```
![image](https://github.com/user-attachments/assets/072d70fc-bed6-4dc9-9c46-76267b8759d7)

- step 2

```
I put this into decoder and tried various combinations to try and get the ascii value out of this. Which seemed to be part of the flag.
```
![image](https://github.com/user-attachments/assets/00385d65-5679-4297-b828-3a026e84cc0c)

- step 3

```
One of the clues said the to try viewing the other file, so I just put the decoded text as the password to open the locked file which gave me the full flag
```

![image](https://github.com/user-attachments/assets/569ec2b7-10ca-4171-bf41-bc71588cfd42)

![image](https://github.com/user-attachments/assets/c5a54405-6e2c-48de-9803-310ed751cb5f)

What you learned through solving this challenge:

1. using cyber chef is so much nicer to bruteforce

Other incorrect methods you tried:

- trying to decode all packet values (including repeated ones with all possible hex+base64 combinations)

References

- https://gchq.github.io/CyberChef/
