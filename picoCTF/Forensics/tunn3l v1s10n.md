**Flag:** `picoCTF{qu1t3_a_v13w_2020}`

How I approached the challenge:

- step 1

```
I put the given unknown file into a hxd editor and found out that its header contains BM, which means it was a bit map file.
I renamed it to a .bmp file accordingly.
```
![image](https://github.com/user-attachments/assets/e74561bf-6b96-4b65-9c32-6d0e9de45a3e)

- step 2

```
I then looked up for the right format of a bitmap file since I knew some part of this data was corrupted.
Upon inspection I found the place that had some invalid data and corrected it.
```
![initial](https://github.com/user-attachments/assets/da55bafa-284d-45f3-bc42-294ca2b2b981)
![corrected](https://github.com/user-attachments/assets/18333029-977b-484b-b82a-9c9c6af4266d)

- step 3

```
I was then given this image
```
![halfimage](https://github.com/user-attachments/assets/5db47363-460a-4bd3-9c70-89d05ea9f706)
```
The challenge was named 'tunnel vision', so I assumed that the image size is somehow cropped or reduced.
```

- step 4

```
I thought of modifiying the image size in the hex data.
```
![details](https://github.com/user-attachments/assets/02a968c0-22c5-47a1-bafd-bc0aea482161)
```
On searching the data for the hex values of the size I found it in the second line
```
![valuespresent](https://github.com/user-attachments/assets/baa76986-a866-49c7-95c2-32add5fe488c)
```
Finally after modifying the size with trial and error I found the perfect size of the image
```
![code](https://github.com/user-attachments/assets/fd319859-4785-4f8a-83d6-74a64af355b8)
```
Final image that I got was: (It had the flag in it!)
```
![fullimage](https://github.com/user-attachments/assets/9fc7437f-4a71-4248-b2af-de6c56b4d712)

What you learned through solving this challenge:

1. The BMP file format

Other incorrect methods you tried:

- I tried reading the data through terminal and just found rubbish.
References

- Understanding bit map file format: (https://www.ece.ualberta.ca/~elliott/ee552/studentAppNotes/2003_w/misc/bmp_file_format/bmp_file_format.htm)

