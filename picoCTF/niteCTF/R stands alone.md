# R STANDS ALONE

**Flag:** `nite{7h3_Latt1c3_kn0ws_Ur_Pr1m3s_very_vvery_v3Ry_w3LLL}`

---

### SOLUTION

First,
Observed the code and got to know that this is very very similar to rsa encryption.
I remember searching online on how to solve similar problems and often came across python code that solved this

So I analyzed that code and knew I needed to:
1. Find the modular inverse of the public exponent `e` to get the private key exponent `d`
2. Use this private key to decrypt the given message


Next,
I just followed these steps I learnt earlier from reference code to solve the problem

1. **Modular Inverse:** The key to decrypting the message is finding `d`, which is the modular inverse of `e`. This means `d` satisfies the equation:  
   I used the `mod_inverse` function from `sympy` module (unlike the Crypto.Util.number like mentioned in reference code, because i had used this earlier) to calculate this.

2. **Decrypting the Message:** Once I had `d`, I could use it to decrypt the message using modular exponentiation, which actually reverses the encryption
![image](https://github.com/user-attachments/assets/c0fe44c8-d7b3-4311-a7da-e176b39359c1)

### CODE:
![image](https://github.com/user-attachments/assets/96e57afe-f543-4d6f-9139-4752a1467c35)

```python
#code here
```


Finally, 
```
Just used long_to_bytes() to get the byte expression of that number and there it was!
```
![image](https://github.com/user-attachments/assets/dad4a318-ca34-4239-9b2a-d92338876888)

### CODE:
![image](https://github.com/user-attachments/assets/39dc460e-cd74-4e7c-9c26-2b06a4ffeeaa)


References (half the work 😂)

- https://b0mk35h.medium.com/unlocking-secrets-a-beginners-guide-to-rsa-decryption-in-python-89a71ccda295
