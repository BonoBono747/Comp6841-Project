# Level 1

## Mindset

Level 0 mentioned that you need to SSH into krypton.labs.overthewire.org and gave us the password. In addition, it mentioned that the files for other levels can be found in /krypton/. 

/krypton/ looks like a directory I would navigate to within the SSH environment using bash commands, so that seems like a good place to start.

The hint on overthewire.org for level 1 was that the string in the krypton2 file was the password for level 2 and is encrypted with a rotation cipher called ROT13. 

For more information on rotation ciphers, see the concepts section.


## Methodology

I connected to the site with: ```ssh krypton1@krypton.labs.overthewire.org -p 2231```, using the password KRYPTONISGREAT from level 0.

<img width="694" height="650" alt="Krypton_1 1" src="https://github.com/user-attachments/assets/e2f50fc2-824c-4df6-8bd1-830dbd241b79" />

I tried using the ls command, but this didn’t show anything. 

I then used the cd command to connect to /krypton/ and used ls to show what’s in the directories. This showed me:

<img width="554" height="73" alt="Krypton_1 2" src="https://github.com/user-attachments/assets/2ded7bd3-1ed9-40d2-89a9-72331a41c1d3" />

This lists a few directories that were probably for all the Krypton levels. Since we are doing level 1, krypton1 is most likely the relevant file, so I used cd to navigate to the krypton1 directory and saw the files krypton2 and README.

I used cat to view both these files, and this is what I got:

<img width="643" height="468" alt="Krypton_1 3" src="https://github.com/user-attachments/assets/869be4cd-0381-462d-a894-9d2530abe1fe" />

The krypton2 file had the string: YRIRY GJB CNFFJBEQ EBGGRA

The README file told me that the string in the krypton2 file was the password for level 2 and is encrypted with a rotation (or Caesar) cipher called ROT13. This cipher is non-standard, so it likely can’t be found on CyberChef. 

I checked CyberChef anyway and found the cipher, which gave me the flag: 

<img width="1189" height="547" alt="Krypton_1 4" src="https://github.com/user-attachments/assets/4ccb817e-0aa4-4378-b2f4-9dede8b054de" />

## Reflections

The challenge asked me to solve it without using a cryptography tool, but to save time, I used CyberChef. However, for the sake of learning, I looked into how I would solve the ROT13 cipher myself in a walkthrough [^1]. 

## Concepts

**Substitution ciphers**

A type of cipher where a character of plain text is substituted by some other character, all from the same set of characters, and based on some key [^2]. 

There are **monoalphabetic** ciphers where a single character will only map to one other character or **polyalphabetic** ciphers where a single character could map to multiple possible letters [^2]. 

An example of a monoalphabetic cipher is the shift/rotational ciphers like the **Caesar cipher** or **ROT13 cipher**. They shift a letter a certain number of places forward in the alphabet (or set of characters) [^2]. For example, a Caesar cipher with shift 3 used on “EMPTY” would become “HPSWB”.

An example of polyalphabetic is the **Vigenère Cipher**, where the plain text is shifted based on the corresponding letter of a keyword [^2]. For example, the word “EMPTY” with keyword “BAT” would become “FMIUY”.

For more information on substitution ciphers and examples, click the link: 
[Link](https://www.stackzero.net/substitution-ciphers/#History_of_Substitution_Ciphers)

**Bash commands**

+ `Cd`: Used to change the current working directory [^3].  
+ `Ls`: Used to list the contents of the current directory [^3].  
+ `Cat`: Used to show the contents of a file in the terminal [^3].  

For more information on these bash commands, click the link: 
[Link](https://www.w3schools.com/bash/bash_commands.php)


### References
[^1]: https://mayadevbe.me/posts/overthewire/krypton/level1/
[^2]: https://www.stackzero.net/substitution-ciphers/#History_of_Substitution_Ciphers 
[^3]: https://www.w3schools.com/bash/bash_commands.php
