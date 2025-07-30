# Level 4

## Mindset
When I accessed the level webpage, it showed me this: 
<img width="940" height="242" alt="image" src="https://github.com/user-attachments/assets/58b1d29e-a3e2-4828-9442-6d37fc166ae9" />

I tried clicking the refresh page link a few times, but it took me to “/index.php” and modified where I was visiting from without showing me any flags. 

I also checked the web developer tools and robots.txt file as I did in the previous levels, but they did not yield any flags either.  

The hint said that it would only allow users to visit from the natas5 page, but I hadn’t gotten the password from that page yet, so I couldn’t access it. This page must be checking something in my HTTP GET request that gets sent when I load the page, and determines that I am unauthorized. To find out more, I used Burp Suite. 

## Methodology
<details>
<summary>Spoilers</summary>

Burp Suite was already used in Level 2 to intercept HTTP requests. This time I tried the same thing and got: 

<img width="2713" height="857" alt="image" src="https://github.com/user-attachments/assets/c8329c88-3c61-460b-beb6-99da9fa0b9e9" />

I didn’t see any flags in the intercepted message, but there is another functionality of Burp Proxy beyond intercepting messages. After intercepting the HTTP request, you can modify it. 

You do this by intercepting a request, changing the data of the request via the Inspector tab, and then forwarding the request to the server. For more information, click the [link]().

This challenge hinted that authorized users only come from the natas5 site, so I just need to modify the request data that tells the server where the request is coming from. 
When I refreshed the page again, I intercepted a request, and before forwarding it, I got this:  

<img width="3018" height="615" alt="image" src="https://github.com/user-attachments/assets/91d7a703-5742-4d18-9b48-35303b2438e9" />

Beneath the Inspector tab, it shows all the request data I can modify. I had a look at this and found: 

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/1b675afb-2598-4983-9c9d-e16417d57469" />

There were two fields that gave the address my request was sent from, Host and Referer. The Host is the domain name of the web server being requested and is required in order to respond with content.

Referer (accidentally misspelt when HTTP/1.0 was written) tells the web server where the user is coming from. Based on the hint, we want the web server to think we are coming from the natas5 webpage. So I modified the value to http://natas5.natas.labs.overthewire.org/ (as specified in the hint) and forwarded the request. This gave me the flag: 

<img width="940" height="244" alt="image" src="https://github.com/user-attachments/assets/f5f84fb0-a261-4f8c-b047-768b13a1bb01" />

</details>

## Concepts

For more information on HTTP, click the [link](https://github.com/BonoBono747/Comp6841-Project/blob/main/Natas/Level-2.md#http).

## Challenge 
This was my first time properly utilizing Burp Suite in a challenge, so I had to look up the documentation for it. It was both interesting and daunting to use this tool since it has a lot of functionality and information, while also having fascinating capabilities. 

I also noticed that when I first analyze a website in Burp proxy, I don’t inspect the intercepted message but instead forward it straightaway until I reach the end website. Therefore, it would be faster to turn off intercept initially and then intercept the messages when I know what part of the HTTP request I should modify. 
