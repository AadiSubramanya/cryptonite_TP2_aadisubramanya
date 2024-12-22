# flag leak

**Flag:** `picoCTF{L34k1ng_Fl4g_0ff_St4ck_999e2824}`

How you approached the challenge:

- step 1

```
Went through the code and immidiately found a format specifier vulnaribility.
```
![image](https://github.com/user-attachments/assets/9647bcf2-ef6b-4b51-9dbc-5e88f921ef24)

- step 2

```
Tried the repeated version of vulnaribilty but then realized it probably might not work since its somewhere later in the buffer.
```
![image](https://github.com/user-attachments/assets/55681903-9f60-4bf1-a5be-1e46d79de354)

- step 2

```
Did some research on for loops in terminal and looked through man page of printf() command
Finally used my knowledge to run a for loop of strings at different buffer locations inputed into the link provided
```
![image](https://github.com/user-attachments/assets/af7ac63b-c27f-4bda-aecd-c90862f37106)


What you learned through solving this challenge:

1. printf() working
2. for loops in terminal
3. more about format specifier vulnaribilities and its dangers

Other incorrect methods you tried:

- trying a large sequence of %s%s... (wrong way as if one %s is not read properly/identified as a string it will end the entire command)
- putting a gap in between %s %s (gets() might truncate this)

References

- https://stackoverflow.com/questions/7165774/terminal-commands-for-loop-with-echo
- https://ss64.com/bash/printf.html
