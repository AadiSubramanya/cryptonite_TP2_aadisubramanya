# Trivial Flag Transfer Protocol

**Flag:** `picoCTF{h1dd3n_1n_pLa1n_S1GHT_18375919`

How I approached the challenge:

- step 1

```
After looking at the extension of the file and doing some research into what pcapng files are, I got to know that you can access
it using tools like wireshark
```
![image](https://github.com/user-attachments/assets/dbeb521e-11fa-426d-bcc6-e18a6547dd28)

- step 2

```
Upon opening and extracting as tftp (as the file is named) using wireshark, I got a folder that had multiple files under it
like so:
```
![image](https://github.com/user-attachments/assets/6913f554-de88-48b1-8935-b3fa7a76f6bd)
```
Then I opened the instructions and got encrypted text. It looked like shifted encryption soI just tried rot13 decryption and 
it worked
```
![first](https://github.com/user-attachments/assets/837e8e89-8838-4584-b691-b3cfa3be4098)
```
I just tried rot13 decryption and it worked
```
![second](https://github.com/user-attachments/assets/02f72261-21a7-4ebc-99fb-3eba225d368b)

- step 3

```
The plain text told me to go back to plan, so I then opened plan file through hexa d editor and again got encrypted text 
like so:
```
![third](https://github.com/user-attachments/assets/62cf3b31-86e8-4406-9b08-d1dcb8d87f1b)
```
Again tried rot13 decryption and it worked.
```
![fourth](https://github.com/user-attachments/assets/f527bfa4-3701-4503-9146-db8673b444aa)

- step 4

```
The text told me it hid stuff using the program, I tried running the program using terminal:
Since it didnt work I tried to install it. When I asked chat gpt what the error was when it was installing it told me:
```
![image](https://github.com/user-attachments/assets/78f2a426-0b05-4fb7-8727-675ef2e815e5)

- step 2

```
Finally after installing using the steghide command I was able to reveal the hidden data in one of the images like so:
```

- etc.

![sixth](https://github.com/user-attachments/assets/f851ad05-2000-4215-bc4a-6c404e9d8bcf)

What I learned through solving this challenge:

1. What is a .pcapng file and how to extract it (using applications like wireshark)
2. How to reveal hidden data in images using steghide

Other incorrect methods you tried:

- Trying to run the .deb program directly with pictures as argument.

References

- chatGPT solved most of it 😂
