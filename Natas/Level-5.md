# Level 5

## Mindset

This level gave the hint “Access disallowed. You are not logged in” with no refresh button.

I checked developer tools and robots.txt, but this didn’t show me any flags, so I tried using Burp Proxy again. 

## Methodology
<details>
<summary>Spoilers</summary>

I logged into the page on the Burp Suite browser without intercepting any requests and observed this:  

<img width="3010" height="231" alt="image" src="https://github.com/user-attachments/assets/7e00fc0b-91f1-4a2e-a7ee-70cb46765486" />

“Loggedin=0” seemed relevant, considering that the hint for this level was that the user was not logged in. So I turned on intercept and modified the logged-in field under the cookie tab.

<img width="350" height="469" alt="image" src="https://github.com/user-attachments/assets/d5c08a75-9b04-430b-84f0-13a622ef7d4e" />

I forwarded the request, which gave me:

<img width="940" height="219" alt="image" src="https://github.com/user-attachments/assets/b9a110db-99c4-4d37-b565-38da5f514ef9" />

</details>

## Cookies

A small piece of information is left on a user’s web browser when they access a website. Designed to retain information about the user’s activity on the website to personalize their web experience. For example, cookies might store login credentials, user behavior (such as preferences), or user session content (such as shopping cart, sign-in status, or game scores) [^1]. 

For more information, click the link: [Link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Cookies)



### References
[^1]: https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Cookies
