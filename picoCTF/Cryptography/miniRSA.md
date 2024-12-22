# miniRSA
**Flag:** `picoCTF{n33d_a_lArg3r_e_d0cd6eae}`

How you approached the challenge:

- step 1

![minirsa](https://github.com/user-attachments/assets/06387e86-17bb-4d61-9092-112906790967)
```
Looked through the ciphertext file and noticed a very small value of e (public key), it isnt very mathematically heavy to decypt the message.
```

- step 2

```
Searched online and read about rsa decryption and applied accordingly
```
![anotherdecoder](https://github.com/user-attachments/assets/33e67b9f-c99e-439c-8fbc-aa3594c9ff58)
```
Then got the flag on running
```
![image](https://github.com/user-attachments/assets/eeb44f5e-a978-4046-90e2-b478f87b6965)
What you learned through solving this challenge:

1. Learnt how RSA keys are generated and various other terms involved 
2. Security risks involved with rsa encryption with some vulnaribilities like a small value of e

Other incorrect methods you tried:

-
References

- https://www.javatpoint.com/rsa-encryption-algorithm

