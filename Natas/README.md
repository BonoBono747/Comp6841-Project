# Introduction to Natas

## Server-side web security 
A developer or security professional should be aware that the programming languages used for web applications have specific vulnerabilities. There are fundamental vulnerabilities on the Internet itself as well [^1] [^2].

Web security wargames will teach you these concepts by having you find hidden information or attain higher-level privileges within a web application. 

Some common vulnerabilities you may come across include 
+ SQL injection
+ Command injection
+ Directory Traversal
+	Cross-Site Scripting (XSS)
+	Cross-Site Request Forgery (CSRF)
  
I will explain any vulnerabilities I come across in the walkthrough; however, if you want more information now, use the following links:
[Link 1](https://ctf101.org/web-exploitation/overview/), [Link 2](https://primer.picoctf.com/#_web_exploits)

## Software to get you started
[**Burp Suite**](<https://portswigger.net/burp/documentation/desktop/getting-started>)  
 The go-to set of tools for penetration testing web applications. Allows the interception, analysis, and modification of HTTP traffic for a website. 

[**Sqlmap**](https://sqlmap.org/)  
Penetration testing tool that automates the process of detecting and exploiting SQL injection flaws in vulnerable database servers.

[**WireShark**](https://www.wireshark.org/)    
A packet capture (PCAP) analysis tool that enables network traffic analysis and recording. Works for different network protocols, not just HTTP, but requires an understanding of them.  

[**Nmap**](https://nmap.org/)  
A network scanner that helps determine information about a system, including features like host discovery, port scanning, service, and OS detection. 

Source: [^3], [^4], [^5]

## How to connect
The first level gives you a username, password, and URL. Copy and paste the URL into your browser, then log in with the credentials to get started. 

<img width="750" height="126" alt="image" src="https://github.com/user-attachments/assets/266af7bf-c5ab-4a56-b9bb-670ad1dec09f" />

For subsequent levels, use the provided username and flag from the previous level as the password.

### References
[^1]: <https://ctf101.org/>
[^2]: <https://primer.picoctf.com/#_introduction>
[^3]: <https://ctf101.org/faq/recommended-software/>
[^4]: <https://strobes.co/blog/web-application-penetration-testing-tools/>
[^5]: <https://medium.com/@ohheyymjincyber/ctf-toolkit-guide-9f5bda3931ea>
