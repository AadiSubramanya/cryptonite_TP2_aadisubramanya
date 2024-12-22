# Custom Encryption

**Flag:** `picoCTF{custom_d2cr0pt6d_8b41f976}`

How you approached the challenge:

- step 1

```
Analyzed the code and found that there were few important variables controlling the second half of the encryption, so I made a code to just find the values with the given
```
![WhatsApp Image 2024-12-22 at 21 23 08_06ffd4be](https://github.com/user-attachments/assets/0e289115-b5a4-46b1-85b2-4c1e5d7a35ea)
![WhatsApp Image 2024-12-22 at 21 23 08_c02c9ecf](https://github.com/user-attachments/assets/b086ab9a-6ff2-4432-8ab9-046c14c7d78b)

```python
a = 94
b = 21
p = 97
g = 31

#and thus found that 

u: 43
v: 8

key: 47
b_key = 47

shared_key = 47
```
![WhatsApp Image 2024-12-22 at 21 23 08_45d2c0e2](https://github.com/user-attachments/assets/1ca23d69-4b25-4f1a-9e4d-f650955e4303)

- step 2

```
With the given values such as the text_key, final cipher list and the values from second half of the encryption, I wrote a python program to decrypt the flag (aka the first half of the encryption)
```
![WhatsApp Image 2024-12-22 at 21 24 11_df8bbbdb](https://github.com/user-attachments/assets/82353155-d3cf-4bbe-a828-6f07c1d0f4ec)
![WhatsApp Image 2024-12-22 at 21 24 28_10a7b0f5](https://github.com/user-attachments/assets/82517f15-b8bb-4298-95b8-06b7dd8cd2e4)


What you learned through solving this challenge:

-

Other incorrect methods you tried:

-

References

-
