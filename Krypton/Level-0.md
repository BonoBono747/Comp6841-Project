# Level 0

## Mindset
The hint given to us on the level 0 page tells us that the password for level 1 is the following string encoded in Base64: S1JZUFRPTklTR1JFQVQ

I know that the Cyberchef tool is good for decoding 


## Methodology

Using CyberChef, I set the operation to “From Base64”, enter the encoded string into Input box and click the Bake! Button. This is the flag that I got: 



## Reflection
This level was straightforward but there is another way of decoding the given string that doesn’t use tools but instead can be done in the shell.    
```echo S1JZUFRPTklTR1JFQVQ = | base64 -d```
This shell command uses echo (which takes the result of anything after and displays it as a string in the terminal) with the base64 command. Base64 is a command that can encode and decode base 64 encrypted strings and the -d flag makes it decode. For more information on base 64, see the concepts section.

This method is a bit more technical but knowing how to use shell commands effectively is essential for CTFs and worth remembering for future Krypton levels and other wargames.

I only saw this method when I read a walkthrough after completing the level. Reading walkthrough from other people even when you have a solution can teach you new things as well. 



## Challenge 

### References
