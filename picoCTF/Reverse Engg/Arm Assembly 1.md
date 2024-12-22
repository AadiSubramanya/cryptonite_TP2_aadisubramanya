# Arm Assembly 1

**Flag:** `flag`

How you approached the challenge:

- step 1

```
Followed the learning video mentioned in the JTP_2 guide book to understand in brief, how assembly language works and made notes accordingly.
```

- step 2

```
Analyzed the code provided to find the required flag
```

```asm
str     w0, [sp, 12]
mov     w0, 85
str     w0, [sp, 16]
mov     w0, 6
str     w0, [sp, 20]
mov     w0, 3
str     w0, [sp, 24]
```
```
This tells us that w0 = 85, w1 = 6 and w2 = 3
```

```asm
ldr     w1, [sp, 16]
lsl     w0, w1, w0
str     w0, [sp, 28]
```
```
Didn't understand this but on looking at the hint provided which said "shifts" I looked this up and found it is left shift.
So it is left shifting w0, w1 times to the left and storing it back in w0

85 = 1010101 (binary)
1010101 << 6 = 1010101000000
which is 5440 in decimal
```

```asm
ldr     w1, [sp, 28]
ldr     w0, [sp, 12]
sub     w0, w1, w0
```
```
This is division, so w0 is divided by w1 and stored back in w0.

5440/6 = 906
```

```asm
ldr	w1, [sp, 28]
ldr	w0, [sp, 12]
sub	w0, w1, w0
```

```
subtraction by original value: 906-85= 821 and then returned by function
```

- step 3

```asm
cmp	w0, 0
bne	.L4
adrp	x0, .LC0
```

```
Here its checked if 0 == returned stuff then it goes to .LC0.
Since we didnt obtain 0 we need to subtract 821 from 0 therefor answer is 821 convert it to hex and then wrap it in picoCTF{}
```

What you learned through solving this challenge:

1. Understanding assembly basics
2. Tracking an assembly code

Other incorrect methods you tried:

- tried output of each step as hex and then wrapped in the flag lol

References

- https://www.youtube.com/watch?v=1d-6Hv1c39c

