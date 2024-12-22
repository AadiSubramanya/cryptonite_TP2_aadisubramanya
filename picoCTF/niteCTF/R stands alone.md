# R STANDS ALONE

**Flag:** `nite{7h3_Latt1c3_kn0ws_Ur_Pr1m3s_very_vvery_v3Ry_w3LLL}`

---

### How I Solved the Challenge

#### Step 1: Understanding the Problem
When I first saw the challenge, it looked very similar to RSA encryption. I remembered from my previous studies that RSA works by using a pair of keys – a public key to encrypt and a private key to decrypt. 

To solve this, I needed to:
1. Find the modular inverse of the public exponent `e` (which is usually 65537) to get the private key exponent `d`.
2. Use this private key to decrypt the given message.

#### Step 2: Breaking It Down
I quickly found that the process was simple if I followed these steps:
1. **Modular Inverse:** The key to decrypting the message is finding `d`, which is the modular inverse of `e`. This means `d` satisfies the equation:  
   \[
   e \cdot d \equiv 1 \ (\text{mod} \ (N-1))
   \]
   I used the `inverse` function from Python's `Crypto.Util.number` to calculate this.

2. **Decrypting the Message:** Once I had `d`, I could use it to decrypt the message using modular exponentiation, which essentially reverses the encryption.

Here’s the Python code I used to decrypt the message:

```python
from Crypto.Util.number import inverse, long_to_bytes

# Given values
right_side = 583923134770560329725969597854974954817875793223201855918544947864454662723867635785399659016709076642873878052382188776671557362982072671970362761186980877612369359390225243415378728776179883524295537607691571827283702387054497203051018081864728864347679606523298343320899830775463739426749812898275755128789910670953110189932506526059469355433776101712047677552
N = 17089720847522532186100904495372954796086523439343401190123572243129905753474678094845069878902485935983903151003792259885100719816542256646921114782358850654669422154056281086124314106159053995410679203972646861293990837092569959353563829625357193304859110289832087486433404114502776367901058316568043039359702726129176232071380909102959487599545443427656477659826199871583221432635475944633756787715120625352578949312795012083097635951710463898749012187679742033
e = 65537

# Step 1: Find the modular inverse of e mod (N-1)
phi_N = N - 1
e_inv = inverse(e, phi_N)

# Step 2: Decrypt the message using modular exponentiation
x = pow(right_side, e_inv, N)
print(f"x = {x}")

# Convert the result to bytes and print the flag
flag = long_to_bytes(x)
print(f"Flag: {flag.decode()}")















# R STANDS ALONE

**Flag:** `nite{7h3_Latt1c3_kn0ws_Ur_Pr1m3s_very_vvery_v3Ry_w3LLL}`

How you approached the challenge:

- step 1

```
Observed the code and got to know that this is very very similar to rsa encryption...
I remember searching online on how to solve similar problems and often came across python code that solved this

So I used that code (which uses inverse function and logic i dont understand __filL logic in simple words__), replacing the values in the different places and modifying/adjusting the code as needed to get my desired number sequuence of number which was 1224543274432953164098494823673082544474888158727042278518055942472603042171050926269717319080882631327061394998314354487201417153661
```
![image](https://github.com/user-attachments/assets/c0fe44c8-d7b3-4311-a7da-e176b39359c1)

### CODE:
![image](https://github.com/user-attachments/assets/96e57afe-f543-4d6f-9139-4752a1467c35)





- step 2

```
Just used long_to_bytes() to get the byte expression of that number and there it was!
```
![image](https://github.com/user-attachments/assets/dad4a318-ca34-4239-9b2a-d92338876888)

### CODE:
![image](https://github.com/user-attachments/assets/39dc460e-cd74-4e7c-9c26-2b06a4ffeeaa)





References (half the work 😂)

- https://b0mk35h.medium.com/unlocking-secrets-a-beginners-guide-to-rsa-decryption-in-python-89a71ccda295
