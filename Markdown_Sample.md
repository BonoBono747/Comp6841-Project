# Markdown Sample

This is a collection of a bunch of markdown features I've come across 

Created: 30/01/2025
S

**Note**: To view this document, I suggest viewing a Markdown preview side my side  
>You can do this by using VSCode, pressing Ctrl+Shift+P then findind Markdown: Open preview to the side

**Note**: There should be an equivalent HTML document somewhere as well.  
>Markdown works the best in conjunction with HTML

## Headings
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
etc etc

## New lines
Two spaces after text to go the next line  
Like so

Or use HTML tag like this <br>
Boom


## Other text features

*Italic*

_Also italic_

**Bold**

~~strikethrough~~

==highlight==

Behold Subscript: H~2~O  
Or try HTML: H<sub>2</sub>O

Behold superscript: X^2^  
Or try HTML: x<sup>2</sup>

Behold emoji :smile:

Note: Some of these features are not supported on all platforms

## Block quotes
>Quote with one indent
>> Quote with two indents  

<br>

## Lists

1. Automatically   
1. Ordered 
1. List

+ Unordered
+ List
    + Complete
    + With 
        + Indentation
        - Can use "*", "+" and "-"
        

- [ ] Here is a checklist
- [x] Here is a check checklist
- [ ] Doesn't seem to be supported here tho but GitHub should work

<br>

## Code 

Note: Add the language after the '''


```python
def hello():
    print("Hello World")

```
Here is an example of `inline code`

<br>

## External and internal hyperlinks

Link: <https://www.google.com/>

Links will also be automatically detected: https://internet-map.net/

Linked text: [Click to find food](https://www.supercook.com/#/desktop)

Link with title: [Titled link](https://www.google.com "Google's Homepage")

Disabled automatic hyperlinks like this `https://www.google.com `

---

### Reference Links

[Referencing-style number links][1]

[Text link][Code]

Here are the reference links that follow later but can't be seen 

[1]: https://www.hanbonforge.com/

[Code]: https://nuclearsecrecy.com/nukemap/

---

### Internal Links

[Relative reference to a repository file (doesnt work yet)](../blob/master/LICENSE)

[Go to the top](#headings)

[The name of heading is seperated by hyphens](#external-and-internal-hyperlinks)

<br>

## Horizontal lines  

This can be done with 
___
underscores
***
or asterisks
******
but use three or more

<br>

## Images

![Not sure what this does](image.png)

<br>

## Table


| Name  | Age |
| ----- | ----|
| Kyle  | 28  |
| Sally | 45  |

| Right | Center | Left |
| ----: | :----: | :--- |
| Kyle  | 28     | Hi   |
| Sally | 45     | Bye  |

<br>

## Dropdown boxes
Note: This isn't markdown it's just HTML
<details>
<summary>Spoiler1</summary>
    Bunch of hidden text inside dropdown box
</details>

<details open>
<summary>Spoiler2</summary>
<br>
    Dropdown box that is always open
</details>

<br>

## Footnotes

Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].  

You can also use words, to fit your writing style more closely[^note].

[^1]: My reference.
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.

Note: This isn't supported always



