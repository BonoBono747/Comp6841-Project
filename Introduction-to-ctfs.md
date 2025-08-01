# Introduction to Capture The Flag Challenges

## What are Catpure The Flag challenges? 

Capture The Flag or CTF challenges are gamified security challenges that involve participants exploiting security vulnerabilities to retrieve a “flag”, which is usually a string of text. These challenges provide an opportunity to grow your computing knowledge with hands-on experience and help keep hard skills up to date [^1] [^2] [^3]. 

There are different types of CTF formats, including Jeopardy-style questions with multiple categories, Attack-Defense style, which involves attacking and defending a network, and King of the Hill, where participants try to control a resource as long as possible [^3].

## Advice 
I summarised some of the best advice for CTF challenges that I found:
+ **Hints**: The short descriptions of challenges are often hints to how to solve them.
+ **Prioritize learning**: Don’t be afraid to read write-ups of challenges. For a beginner, they’re a good place to start, and even experienced challengers can learn new things from them.
+ **Work together**: It can be helpful to have someone to bounce ideas off, and it also makes CTF challenges more fun.
+ **Use existing tools**: There are a variety of tools out there that simplify what you need to solve challenges. Don’t overcomplicate things!
+ **Avoid rabbit holes**: If you get stuck on something, take a break and come back to the problem later.
+ **Write stuff down**: Document your process of solving problems as they improve your overall mindset and may be useful in future challenges.

Source: [^4]

## Types of CTF challenges
There are different types of CTF challenges that you will encounter, and these are based on the different categories of vulnerabilities. Sometimes, a challenge will require you to exploit multiple types of vulnerabilities to solve the challenge. I’ve listed them below with a short description.

|Challenge Type|Description|
|--------------|--------------------------------------|
| Cryptography   |Breaking or analyzing encrypted data|
|Web exploitation|Exploiting vulnerabilities in web applications|
|Reverse Engineering|Analyzing binary code to understand its behavior or extract hidden data|
|Pwn/Binary Exploitation|Exploiting vulnerabilities in compiled programs, often remotely|
|Forensics|Recovering or analyzing data from files, memory, or network traffic|
|Steganography|Finding data hidden in plain sight, usually in multimedia files|
|Open Source Intelligence|Using publicly available information to discover clues or data|

Sources: [^1] [^3]

There are other miscellaneous types of challenges and challenges that combine these types that are called exploitation/realistic/hybrid. 

Resources that document types of CTF challenges and their associated vulnerabilities: 
1. <https://ctf101.org/>  
Handbook to learn the basics of CTFs. Includes vulnerabilities, methodologies, and techniques for Forensics, Cryptography, Web Exploitation, Reverse Engineering, and Binary Exploitation. 
1. <https://primer.picoctf.com/#_introduction>  
Comprehensive primer for CTF challenges, which is attached to its own CTF challenge website – https://play.picoctf.org/login. Introduces a lot of fundamental computer topics before going more in-depth on security vulnerabilities.

## Introducing OverTheWire
OverTheWire is aimed at a less experienced audience compared to other cyber wargame sites. It uses the Jeopardy format of CTFs and requires you to find the flag from whatever resources or information they give you. These flags are used as the password for the next level, so without solving the previous level, you can’t move on.

The games I’m covering in this walkthrough are Natas and Krypton, but I’ll introduce some of the others as well

+ **Natas** covers the basics of web exploitation and gives you access to websites where you need to try to find the flag.   
+ **Krypton** covers basic cryptography and requires you to find the flag in encrypted text.  
+ **Leviathan** covers reverse engineering, Linux, and binary exploitation, where each level has an exploitable file or binary.  
+ **Narnia** covers binary exploitation and other regular vulnerabilities and provides source code in the C language.  
+ **Behemoth** is like Narnia but at the next level of difficulty. It focuses more on debugging techniques and doesn’t provide the source code.

## Software for CTFs
Another necessary aspect of CTFs that I found when I did my background research was the use of software tools. These applications and tools allow further analysis and exploitation of the various vulnerabilities found in the challenges. 

Here are some of the resources I found that recommend tools for CTF challenges:
1. <https://ctf101.org/faq/recommended-software/>  
Recommends some essential software to start with for decompiling, debugging, web exploitation, virtualization, programming, and cryptography.  
    
1. <https://medium.com/@ohheyymjincyber/ctf-toolkit-guide-9f5bda3931ea>  
Introduces and links popular tools used for various categories of CTFs.   
1. <https://medium.com/@ohheyymjincyber/ctf-toolkit-guide-9f5bda3931ea>

In each wargame, I will introduce the relevant software that might be needed for that type of security vulnerability, and when you might need to use it.

**Reflective note:**
> Since CTFs were new to me, I spent a few hours combing through different resources to introduce me to cybersecurity vulnerabilities and CTF tools. While this was very helpful, it would have been better to get started on the challenges sooner and learn while doing them. Even if you don’t know how to solve a challenge, there’s nothing wrong with looking up a walkthrough and learning from that so you can complete a challenge next time. 

## What's Next

At this point, I recommend starting some challenges. 

Have a look at my walkthroughs of [Natas](https://github.com/BonoBono747/Comp6841-Project/tree/main/Natas) and [Krypton](https://github.com/BonoBono747/Comp6841-Project/tree/main/Krypton).
> These walkthroughs assume that you have completed the previous levels in the challenge, so they don't explain concepts that have already been covered in previous levels. 


## References
[^1]: <https://ctf101.org/>
[^2]: <https://ctfs.github.io/resources/>
[^3]: <https://medium.com/@ohheyymjincyber/ctf-toolkit-guide-9f5bda3931ea>
[^4]: <https://www.hackthebox.com/blog/what-is-ctf>



