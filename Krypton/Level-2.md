# Level 2

## Mindset
The hint on overthewire.org for level 2 explained Caesar ciphers and gave the following hint: 

<img width="1491" height="708" alt="Krypton_2 1" src="https://github.com/user-attachments/assets/1759bf02-bbb7-4c11-836e-900df396bf1e" />

The first part tells me that the password for the level is found in Krypton3 and that’s encrypted using a Caesar cipher with a 5-letter group. They also gave us the key, which we can’t see, and an encryption program that will encrypt any .txt file we give it.

The additional information also explains how to create a temporary directory with the keyfile. For an explanation of the bash commands used, see the concepts section. 

From the first hint, we know that we need to find a way to decrypt the string given to us in Krypton3. However, we only have an encrypt function. 

If we recall how substitution ciphers work (see the concepts section), once we figure out how much a single letter is shifted, it will tell us how to decrypt every letter of the alphabet. For example, if we encrypt the letter A and it returns the letter C, we know that the shift we need to do for decryption is 2 letters.

The point of the additional information provided seemed unclear to me, but I kept it in mind in case it was useful later. 


## Methodology

I followed the same method I used in level one to connect to and view the challenge, except the username was changed to krypton2, and the password was from level 1. 
> Note that if you try and access the level 2 information with a level 1 login, you won’t have permission to view the level 2 files.

From there, I had a look at the files in the krypton2 directory, which included README, encrypt, keyfile.dat, and krypton3. I then checked the contents of each file using the cat command.

The README was the same as the hint on overthewire.org, and the keyfile.dat could not be accessed. The krypton3 file had the string “OMQEMDUEQMEK” and the encrypted file showed this: 

<img width="1603" height="263" alt="Krypton_2 2" src="https://github.com/user-attachments/assets/0164c70d-f4ea-4fab-b923-4d850cca6443" />

This didn't seem to have anything useful, so I moved on.

I wanted to try to encrypt a file using the encrypt program they gave us. To do this, I tried creating a file with an echo command that piped some letters into a file. However, I got a denied error. This meant that users couldn’t create files in this directory, which is when I remembered the additional information they gave us on how to create a temporary directory. So I used the following commands:

<img width="591" height="148" alt="Krypton_2 3" src="https://github.com/user-attachments/assets/76951dc5-81eb-4c2a-9699-5448fc220b6e" />

Using this temporary directory, I created the file test.txt with some letters that I could encrypt and used the encrypt program supplied to encrypt the test.txt file. 

<img width="750" height="296" alt="image" src="https://github.com/user-attachments/assets/2ba13c7b-6e8b-4bcb-bc6e-e36bbb5c22d5" />

I tried using the encrypt program directly from the temporary directory, but that didn’t work. So, I looked back at the hint and used the code from there. Note that the encrypt function only works if the key file is in the same directory as the text to be encrypted. 

After using the cat ciphertext to view what was in the file, I saw that it printed MMM.

This means the Caesar cipher we were looking at shifted AAA to MMM, which is a shift of 12 positions to encode. Therefore, to decode, you can either shift back 12 characters or shift forward 26 – 12 = 14. 

To solve this for the string we got from krypton3, you can do this manually or use CyberChef.

> Note that CyberChef does not have a dedicated operation for the Caesar cipher, so use ROT13 and set the amount, which is 14 in this case.

<img width="786" height="567" alt="image" src="https://github.com/user-attachments/assets/45f00865-3c48-4ff1-b1ba-768e9518af4a" />

So, our flag is CAESARISEASY. 

## Reflection

I didn’t understand all the information they gave at the start of the level since it was only useful later in the level. It’s important to at least keep in mind all the information they give, even if you don’t understand it or use it straight away. 

I also didn’t fully understand all the bash commands they used in the additional information section, which I ended up using to solve the challenge. It may not have been essential to completely understand, but I looked it up anyway for the sake of learning.

## Concepts

**Caesar ciphers**

Check out [Level 1](https://github.com/BonoBono747/Comp6841-Project/blob/main/Krypton/Level-1.md#concepts) 
or the explanation by OverTheWire: 
[Link](https://overthewire.org/wargames/krypton/krypton2.html)

**Bash commands**  
+ `Mktemp`: Used to create a temporary file or directory [^1].  
+ `Ln`: Creates a link between two files. The -s flag specifies a symbolic link [^2]. It was used in this level to store the path of the target file, linking it to the current directory.  
+ `Chmod`: Used to modify the file permissions in a Unix-like system [^3]. 777 gives read, write, and execute permissions [^4].   
+ `Echo`: Used to show a line of text or a variable’s value in the terminal [^5]. In this case, the text was “piped” using “>” into a file.   


### References
[^1]: https://man7.org/linux/man-pages/man1/mktemp.1.html
[^2]: https://man7.org/linux/man-pages/man1/ln.1.html
[^3]: https://www.w3schools.com/bash/bash_chmod.php
[^4]: https://linuxize.com/post/what-does-chmod-777-mean/
[^5]: https://www.w3schools.com/bash/bash_echo.php
