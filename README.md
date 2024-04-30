## Title: Post Mortem
## Details:
* difficulty: Easy
* category: Forensics 
* author: Sarmed
* flags: flag{steg is crack}

## Description:
Steganography is the art of hiding text in a picture and has been used in the recent years to pass on or send a secret message to the relevant person(s).  

## Hint:
Observe carefully whatever that you see.

## Intended Learning and outcome:
With this challenge, I was able to learn how stegnography is used to hide a message or a file and never to use the name of a file as its password.

## Solution: 
We are given an image of a bat that appears pretty plain. We can use the exiftool to analyze the image to see that the resolution and dimensions of the file translate to much lesser size than the image actually is. We proceed to run the command to check if there is any hidden data in it using **steghide extract -sf bat.jpg**. A prompt is shown asking for a password, we can try common passwords but they don't work, we try **bat** as password and it extracts a file by the name of flag.txt which contains the flag.
