# Level 4

## Mindset
The hint explains how the Vigenère Cipher works.

Since this is a polyalphabetic cipher where a single letter can map to multiple letters, frequency analysis won’t work the same way as level 3. Since the key size is 6, every 6th letter will have the same operation applied to it. Therefore, you can do frequency analysis on every 6th letter, like the 1st, 7t,h and 13th letters. 


## Methodology
I logged into Level 4 and found files similar to Level 3. I didn’t read the HINT file just yet.

The krypton5 file had this encrypted text: HCIKV RJOX

I checked whether CyberChef had the functionality to do frequency analysis for blocks of 6, but I couldn’t find anything. I tried doing the frequency analysis anyway and got this:

<img width="600" height="778" alt="Krypton_4 3" src="https://github.com/user-attachments/assets/0dc12eb7-bb69-4e8d-81e9-1d351fddc3f5" />

I looked for another tool to do frequency analysis, but I couldn’t find any. That left me doing the analysis by writing my own code or solving the challenge differently. 

I did some research and found this website: https://www.dcode.fr/vigenere-cipher.

It attempts to decrypt Vigenère Ciphers using either a key, length, partial key, or known plaintext. Since I had the key length, I input that and text from found1 and got this: 

<img width="984" height="569" alt="Krypton_4 1" src="https://github.com/user-attachments/assets/70a95b4f-75a2-467b-ba81-e0ad0ae01f54" />

This looked like English, even though it was a bit difficult to read in those blocks of 5 letters. It also said that the key was FREKEY (scroll down on the output).

So, I tried this key with the encrypted text from Krypton5 and got this: 

<img width="979" height="420" alt="Krypton_4 2" src="https://github.com/user-attachments/assets/37550fd0-2a29-499e-b815-a890ea0df266" />

Thus, the flag is CLEARTEXT.

## Challenge 
This challenge needed me to use a tool that I hadn’t prepared in advance for this level, and instead had to look up Vigenère decryption tools.


## Concepts

**Vigenere ciphers**  
Check out [Level 1]() 
or the explanation by OverTheWire: [Link](https://overthewire.org/wargames/krypton/krypton4.html)
