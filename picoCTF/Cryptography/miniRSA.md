# miniRSA
**Flag:** `picoCTF{n33d_a_lArg3r_e_d0cd6eae}`
---
How you approached the challenge:

- step 1

![minirsa](https://github.com/user-attachments/assets/06387e86-17bb-4d61-9092-112906790967)
```
Looked through the ciphertext file and noticed a very small value of e (public key), it isnt very mathematically heavy to decypt the message.
```

- step 2

```
Asked chatgpt to provide a code to give cube root of huge numbers with maximum precision (since I had no idea) 
```
```python
def rooter(x,n):
    high = 1
    while high ** n <= x:
        high *= 2
    low = high/2
    while low < high:
        mid = (low + high) // 2
        if low < mid and mid**n < x:
            low = mid
        elif high > mid and mid**n > x:
            high = mid
        else:
            return mid
    return mid + 1

print(rooter(2205316413931134031074603746928247799030155221252519872650080519263755075355825243327515211479747536697517688468095325517209911688684309894900992899707504087647575997847717180766377832435022794675332132906451858990782325436498952049751141,3))
```

```
which gave me: 13016382529449106065894479374027604750406953699090365388203722801043052339225981.
```

- step 3
```
Then got the flag on running this final program that converted the number to string / bytes.
```
![anotherdecoder](https://github.com/user-attachments/assets/33e67b9f-c99e-439c-8fbc-aa3594c9ff58)
![image](https://github.com/user-attachments/assets/eeb44f5e-a978-4046-90e2-b478f87b6965)

---

What you learned through solving this challenge:

1. Learnt how RSA keys are generated and various other terms involved 
2. Security risks involved with rsa encryption with some vulnaribilities like a small value of e

Other incorrect methods you tried:

-
References
- https://www.calculatorsoup.com/calculators/algebra/cuberoots.php
- https://www.javatpoint.com/rsa-encryption-algorithm

