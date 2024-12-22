# Custom Encryption

**Flag:** `picoCTF{custom_d2cr0pt6d_8b41f976}`

---
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
```python
def generator(g, x, p):
    return pow(g, x, p)

a=..
b=..
c=..

u = generator(a, b, c)

print("final:", u)
```
adjusting a,b,c as needed
```
- step 2

```
With the given values such as the text_key, final cipher list and the values from second half of the encryption, I wrote a python program to decrypt the flag (aka the first half of the encryption)
```
```python
pt= ""
text = ""
text_key = "trudeau"
for i in [131553, 993956, 964722, 1359381, 43851, 1169360, 950105, 321574, 1081658, 613914, 0, 1213211, 306957, 73085, 993956, 0, 321574, 1257062, 14617, 906254, 350808, 394659, 87702, 87702, 248489, 87702, 380042, 745467, 467744, 716233, 380042, 102319, 175404, 248489]:
    text += chr(i // (47 * 311))
print(text)
for i, char in enumerate(text):
    key_char = text_key[i%len(text_key)]
    num = chr(ord(char)^ord(key_char))
    pt+=num
    
print(pt[::-1])
```
---

What you learned through solving this challenge:

-not much, it was quite easy

Other incorrect methods you tried:

-

References

-
