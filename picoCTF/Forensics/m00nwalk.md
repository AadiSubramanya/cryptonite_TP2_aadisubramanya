# m00nwalk
**Flag:** `picoCTF{beep_boop_im_in_Space}`

How I approached the challenge:

- step 1

```
After downloading and analyzing the audio file with no leads, I had to resort to the hints.

The first hint read: "How did pictures from the moon landing get sent back to Earth?"

Upon some research I got to know that they did this using slow-scan television (SSTV) technology.
```

- step 2

```
Upon realizing that it was sstv encoded, I tried to seach for an appropriate sstv decoder online and came across this github:
https://github.com/colaclanth/sstv/blob/master/README.md
```
https://github.com/colaclanth/sstv/blob/master/README.md

- etc.

![screenshot](./screenshot.png)

What you learned through solving this challenge:

1. Installing open source github projects
2. Understanding SSTV encoding & decoding.

Other incorrect methods you tried:

- I assumed the audio was a morse code of some form and tried morse decoding XD.

References

- chatGPT for some research
- https://github.com/colaclanth/sstv to install the sstv decoder
