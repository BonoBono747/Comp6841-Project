# Level 2

## Mindset
The hint they gave was “There is nothing on this page”. I checked the developer tools and found nothing. At this point, I thought I’d try using Burp Suite. 

## Methodology
<details>
<summary>Spoilers</summary>
  
One basic function of Burp Suite is intercepting HTTP traffic. It involves loading a website and using the Burp Proxy to intercept the HTTP request before it reaches the web server. This allows you to inspect the request and possibly see any hidden information. 

For more information on intercepting HTTP traffic on Burp Suite, use this [link](https://portswigger.net/burp/documentation/desktop/getting-started/intercepting-http-traffic?utm_source=burp_suite_community&utm_medium=learn_tab&utm_campaign=onboarding)

<img width="1395" height="1159" alt="image" src="https://github.com/user-attachments/assets/b9b5eb81-6a52-4791-a8de-48b63a7b8a61" />

I reviewed all the requests I intercepted and searched for “natas3” and “pass” to find the flag, but didn’t find anything.  

I had run into my second dead-end. I thought about trying another function of Burp Proxy, which is to modify requests. However, I realized that I’m not making requests to the site, so there are no requests to modify.

So, I went back to developer tools to see if I had missed anything, and I saw this: 

<img width="1833" height="834" alt="image" src="https://github.com/user-attachments/assets/8fed0078-e22e-419e-a8da-3cf79cc52e35" /><br>

This wasn’t there for the previous levels, so I thought it was worth investigating. I right-clicked on the link and hit “open link in new tab”. This opened an image with a single pixel, which didn’t give me the flag. But since this image was inside another folder called files, I thought I’d check that as well by modifying the URL from “../files/image.png” to “../files”. That gave me this page:  

<img width="1039" height="424" alt="image" src="https://github.com/user-attachments/assets/f4e397f1-b512-4660-ba2b-a98926f55603" />

<br>
I clicked on user.txt and found the flag:
<img width="910" height="324" alt="image" src="https://github.com/user-attachments/assets/39566eff-2bbb-4bdd-a4ad-0a9fbf57f780" />


</details>

## Concepts

#### HTTP
The Hyper Text Transfer Protocol or HTTP is an underlying application layer network protocol that defines and enables the transfer of published resources on the Web, between a web server and web browser [^1].

Each HTTP request packet contains a series of encoded data that carries different types of information [^2]. This typically includes:
+ HTTP Version
+	URL
+	HTTP method 
+	HTTP request headers
+	Optional HTTP body  

For more information, click the links: 
[Link 1](https://developer.mozilla.org/en-US/docs/Glossary/HTTP)
[Link 2](https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/)
#### URL
Uniform Resource Locator or URL is the address behind a unique resource on the Internet and is the main way browsers retrieve published resources like websites or images. 

A URL is composed of different parts shown below: 
<img width="1674" height="164" alt="image" src="https://github.com/user-attachments/assets/949917fb-ecf5-4531-af88-c754f5397432" />

Source: [^3]

In this level, we modified the path to the file to access different information. 

For more information, click the link: 
[Link](https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_URL)


## Challenge 
This level had me stumped at first after trying to inspect web developer tools and intercept HTTP requests with Burp Suite. However, going back and checking the previous step for things I’d missed helped solve the level. 

### References
[^1]: https://developer.mozilla.org/en-US/docs/Glossary/HTTP
[^2]: https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/
[^3]: https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_URL
