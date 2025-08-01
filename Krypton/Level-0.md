# Level 0

## Mindset
The hint given to us on the level 0 page tells us that the password for level 1 is the following string encoded in Base64: S1JZUFRPTklTR1JFQVQ

I know that the Cyberchef tool is good for decoding 


## Methodology

Using CyberChef, I set the operation to “From Base64”, entered the encoded string into the Input box, and clicked the "Bake!" Button. This is the flag that I got: 

<img width="1920" height="545" alt="Krypton_0 1" src="https://github.com/user-attachments/assets/397f8c92-6398-45a4-91c1-ff881a90a9bd" />

## Reflection
This level was straightforward, but there is another way of decoding the given string that doesn’t use tools but can be done in the shell. 

```echo S1JZUFRPTklTR1JFQVQ = | base64 -d```

This shell command uses echo (which takes the result of anything after it and displays it as a string in the terminal) with the base64 command. Base64 is a command that can encode and decode base 64 encrypted strings and the -d flag makes it decode. For more information on base 64, see the concepts section.

This method is a bit more technical, but knowing how to use shell commands effectively is essential for CTFs and worth remembering for future Krypton levels and other wargames.

I only saw this method when I read a walkthrough [^1] after completing the level. Reading walkthroughs from other people, even when you have a solution, can teach you new things as well. 

## Concepts
**Base64 encryption**

Base64 is an encoding method that converts binary data into ASCII text. The binary data is broken into 6-bit segments, which are mapped to 64 (2^6) possible characters [^2].

For more information, click the link: 
[Link](https://builtin.com/software-engineering-perspectives/base64-encoding)




### References
[^1]: https://mayadevbe.me/posts/overthewire/krypton/level0/
[^2]: https://builtin.com/software-engineering-perspectives/base64-encoding
