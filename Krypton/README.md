# Introduction to Krypton

## Cryptography

In any software application, there is often a need for confidentiality. This can be web traffic such as passwords and communication, proprietary software encryption, and key exchange algorithms [^1].

Cryptography wargames will teach you the techniques behind encryption by getting you to decrypt encoded data. 

Some common ciphers and encryption techniques you may come across include: 
+	Substitution ciphers
+	Caesar Ciphers
+	Vigenère Ciphers
+	Block ciphering
+	Stream ciphering
+	MD5 Hash
+	RSA encryption

Source: [^1]

I will explain any encryption types we come across in the walkthrough; however, if you want more information now, use the following links: 
[Link 1](https://ctf101.org/cryptography/overview/), 
[Link 2](https://primer.picoctf.com/#_cryptography)

## Software to get you started
[Cyberchef](https://gchq.github.io/CyberChef/)  
All-purpose web application for analyzing, encoding, and decoding data

[Quipquip](https://quipqiup.com/)  
Web application that attempts to automatically decipher substitution ciphers (including no-key Vigenère deciphering). Not always successful.

Source: [^2], [^3]

## How to connect

Krypton level 0 gives you a string to decrypt, which will be used as the password for the next level. 

Krypton level 1 gives you an SSH address, port, username, and password. SSH into the Krypton server by entering the following command into your terminal: `ssh username@address -p port`

Then enter the password. 
> Note: You won’t be able to see the password once you enter it, and copy-pasting the password might not work, so try typing it manually.

In subsequent levels, use the given username and flag you found from the previous level as the password.
For more information on SSH, see the reference guide.





### References
[^1]: https://ctf101.org/cryptography/overview/
[^2]: https://ctf101.org/faq/recommended-software/
[^3]: https://medium.com/@ohheyymjincyber/ctf-toolkit-guide-9f5bda3931ea
