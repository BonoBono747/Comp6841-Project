# Level 3

## Mindset
This time, I thought I’d be more careful with each step so I wouldn’t miss any information and therefore avoid the mistake I made in Level 2.

There were no hints given on the webpage for this level that I could see. 

## Methodology
<details>
<summary>Spoilers</summary>
  
I tried inspecting the web developer tools and found a hint:

<img width="1615" height="268" alt="image" src="https://github.com/user-attachments/assets/50bd21bd-94a4-4deb-aa9e-a6273f87b58e" />

I wasn’t sure what this meant. I knew that this hint was very important to the problem, but it meant nothing to me. I thought about using Burp Suite again, but after my experience in Level 2, I thought it would be unnecessary. 

I tried adding “../files” to the URL like I did in Level 2, but no webpage existed. So, having reached a dead-end, I decided to check a walkthrough [^1] [^2].

The walkthrough revealed an aspect of websites that I was unaware of: the robots.txt file. For a full explanation of this, see the concept section below.

So, I added “/robots.txt” to the URL and saw this:

<img width="340" height="100" alt="image" src="https://github.com/user-attachments/assets/05ac116c-5e8e-4731-a8e3-4b4a3b2b97cd" />

This tells us that there is something at the URL `http://natas3.natas.labs.overthewire.org/s3cr3t/`

At that URL, I found a user.txt file where I found the flag: 

<img width="470" height="56" alt="image" src="https://github.com/user-attachments/assets/ce21c5ff-1515-41c7-b534-597b913cbe5a" />

</details>

## Concepts:
#### Search Engines
A search engine is a software that searches and retrieves information from the World Wide Web and presents it to a user who requested it from their web browser. It will return a list of suggested hyperlinks (digital reference providing direct access to data [^3]) ranked by how strongly they match your query. 

Search engines have computer programs called search engine crawlers that are responsible for finding information specified by keywords [^4] [^5]. 

For more information, click the links:
[Link 1](https://developer.mozilla.org/en-US/docs/Glossary/Search_engine)
[Link 2](https://www.geeksforgeeks.org/computer-science-fundamentals/what-are-search-engines-and-how-do-they-work/)

#### Search Engine Crawlers and Robot.txt
Search engine crawlers/bots/spiders are programs operated by search engine providers like Google that are used to automatically discover and scan websites to create an index. This improves the efficiency and quality of search results [^6] [^7]. 

A robots.txt file tells search engine crawlers which URLS on their site the crawler or user can and cannot access [^8]. Read more 
[here](https://developers.google.com/search/docs/crawling-indexing/robots/intro)

As such, if a website has a robots.txt file, it can reveal information about unknown files on a website that might not be accessible from your current webpage. These pages can be accessed by adding the URL specified in the file to the end of the current URL.

For more information on Websites, click the link to [Level 2](). 

## Challenge 

The concept behind Google bots/crawlers was nothing that I had heard of before, so checking a walkthrough for hints was the right choice. To fully understand this level, research into a few topics was needed. These topics include robots.txt, search engine crawlers, search engines, and websites.   

### References
[^1]: https://www.hackingarticles.in/overthewire-natas-walkthrough-0-11/
[^2]: https://mayadevbe.me/posts/overthewire/natas/natas3/
[^3]: https://en.wikipedia.org/wiki/Hyperlink
[^4]: https://developer.mozilla.org/en-US/docs/Glossary/Search_engine
[^5]: https://www.geeksforgeeks.org/computer-science-fundamentals/what-are-search-engines-and-how-do-they-work/
[^6]: https://developers.google.com/search/docs/crawling-indexing/overview-google-crawlers
[^7]: https://www.cloudflare.com/learning/bots/what-is-a-web-crawler/
[^8]: https://developers.google.com/search/docs/crawling-indexing/robots/intro

