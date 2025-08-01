# Level 5

## Mindset
The hint for this level was that this is a polyalphabetic cipher from American English again, but this time we didn’t know the key length.

I wasn’t too sure how to go about this since the method we used in level 4 relied on using the key length on the dcode.fr website. 

One idea that I had was brute forcing different key lengths. Which meant trying key lengths 1, 2, 3,... on the decryption website and seeing if those yielded results. However, this could take a long time as well.

## Methodology

<details>
<summary>Spoilers</summary>

I logged into level 5 and looked at the file they had in the directory. This time there was no hint, but otherwise it was similar to the previous two levels. 

The ciphered text in krypton6 was: “BELOS Z”.

I copied the text from found1 and input it into https://www.dcode.fr/vigenere-cipher.

I started with a key length of 1 and started brute forcing. While I was brute forcing, I noticed a feature I hadn’t used before: 

<img width="372" height="28" alt="Krypton_5 1" src="https://github.com/user-attachments/assets/20691e10-1318-465e-a50e-585529e64785" />

I wasn’t sure what this was, so I looked it up.

Kasiski’s Test essentially uses an algorithm to determine likely key sizes for a sample of Vigenère ciphered text. For more information, see this 
[link](https://crypto.interactive-maths.com/kasiski-analysis-breaking-the-code.html).

So, I ran this algorithm on the ciphered text from found1 and got this: 

<img width="227" height="278" alt="Krypton_5 3" src="https://github.com/user-attachments/assets/14971ed8-2642-4788-a556-0e78f2891622" />

This tells me that the key length is likely to be 6, 3, 9, 5, or 4. So I tried these key lengths and got the answer at key length 9.

<img width="403" height="785" alt="Krypton_5 2" src="https://github.com/user-attachments/assets/b855b8e8-f553-4711-9f16-18af3a410af9" />

So, the key was KEYLENGTH, and I applied it to the ciphered text in krypton6 and got this:

<img width="227" height="278" alt="Krypton_5 3" src="https://github.com/user-attachments/assets/8d9f5ab9-39f4-4f86-adc3-e1ab7824f01b" />

Therefore, the flag is RANDOM

</details>
