# FORMAT STRING 0

**Flag:** `picoCTF{7h3_cu570m3r_15_n3v3r_SEGFAULT_74f6c0e7}`

How I approached the challenge:

- step 1

```
On running the instance I was given three options,
Breakf@st_Burger, Gr%114d_Cheese, Bac0n_D3luxe

Since the challenge hint had to do with format specifiers vulnaribilities, I entered the 2nd option as it has a format vulnaribility
```

- step 2

```
Furthermore I was given 3 more options,
Pe%to_Portobello, $outhwest_Burger, Cla%sic_Che%s%steak

Again, I chose the one with a vulnarable format specifier which was the 3rd one.
I was then provided with the flag.
```


What I learned through solving this challenge:

1. When a large field width is used (like %114d), the program may attempt to print more characters than expected. If there are memory buffers in place and the program doesn’t properly check for overflows, this could potentially lead to a buffer overflow.
   
2. If no valid argument is provided for %s, it can read arbitrary parts of memory potentially leaking sensitive information hence a vulnaribility.


Other incorrect methods you tried:
-


References
- chatGPT to explain how these were vulnaribilities (since i got the answer through trial and error, the first time)

