# Natas Level 0

## Mindset
Before going on my deep dive into CTFs, known vulnerabilities, and cybersecurity concepts, I had a look at a walkthrough of Natas[^1]. I didn’t want to spoil too much of the challenge, so I only looked at level 0 and did a quick scroll of some of the levels. I saw that level 0 required using web developer tools and that future levels made use of Burp Suite and Wireshark. This wasn’t much to go on, but it was a good place to start without telling me too much. 

## Method
I know that I need to access Google’s developer tools for this task, but I can’t remember how to do that. So I looked it up, and there are three methods:
1.	Right-click on the webpage and click `View Page Source`.
2.	Press `F12`
3.	Press `Ctrl+Shift+I`

I tried F12 and clicked some of the down arrows to show the hidden information. That’s where I found my first flag.
<img width="1920" height="759" alt="image" src="https://github.com/user-attachments/assets/d9011f71-74b9-4ac9-b1e8-028bd2512b12" />

## Concepts
#### Webpage/Websites
A webpage is a document written in the HTML programming language that can be displayed on a web browser. A group of **webpages** is called a website, and they are hosted on a **web server** [^2].

#### HTML
HyperText Markup Language or HTML is the standard “markup” language that defines the meaning and structure of a webpage. It consists of a series of elements that tell the web browser how to display content.

Elements will label different content on a webpage, such as “heading”, “paragraph”, “image”, etc., using tags.  

Other programming languages are used with HTML, like CSS for appearance/presentation and JavaScript for functionality and behavior [^3] [^4].  

For more information, click the links:
[Link 1](https://developer.mozilla.org/en-US/docs/Web/HTML)
[Link 2](https://www.w3schools.com/html/html_intro.asp)

#### Web browser developer tools
A developer tool that’s built directly into the browser and allows for inspecting elements of the currently loaded HTML, CSS, and JavaScript. There are other functionalities as well, but they aren’t relevant to this level [^5]. For more information, click the link: [Link](https://www.geeksforgeeks.org/javascript/browser-developer-tools/)

# References
[^1]: https://www.hackingarticles.in/overthewire-natas-walkthrough-0-11/
[^2]: https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Environment_setup/Browsing_the_web
[^3]: https://developer.mozilla.org/en-US/docs/Web/HTML
[^4]: https://www.w3schools.com/html/html_intro.asp
[^5]: https://www.geeksforgeeks.org/javascript/browser-developer-tools/
