---
tags:
  - Navigator
  - Knowledge
Purpose:
  - Knowledge
  - Navigator
parent: "[[🧭Navigator]]"
---
---
## Here in Obsidian We Write Everything in MarkDown Language 

# Now What is Markdown?

[Original-ReadMe](https://github.com/im-luka/markdown-cheatsheet/blob/main/README.md#what-is-markdown)

Markdown is a lightweight markup language that you can use to format plain text documents.  

Let's dive into it. ⤵️

# Table of Contents

1. [[Paragraph]]
2. [[Headings]]
3. [[Emphasis]]
4. [[Blockquote]]
5. [[Images]]
6. [[Links]]
7. [[Code]]
8. [[Lists]]
	- [[Ordered List]]
    - [[Unordered List]]
    - [[Mixed List]]
10. [[Table]]
11. [[Task List]]
12. [[Footnote]]
13. [[Jump to section]]
14. [[Horizontal Line]]
15. [[HTML]]

---
# Paragraph

By writing regular text you are basically writing a paragraph.

```
This is a paragraph.
```

This is a paragraph.

---

# Heading

There are 6 heading variants. The number of "#" symbols, followed by text, indicates the importance of the heading.

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

---

## Emphasis

Modifying text is so neat and easy. You can make your text bold, italic and strikethrough.

```
Using two asterisks **this text is bold**.  
Two underscores __work as well__.  
Let's make it *italic now*.  
You guessed it, _one underscore is also enough_.  
Can we combine **_both of that_?** Absolutely.
What if I want to ~~strikethrough~~?
Wanna ==Highlight==?
```

Using two asterisks **this text is bold**.  
Two underscores **work as well**.  
Let's make it _italic now_.  
You guessed it, _one underscore is also enough_.  
Can we combine **_both of that_?** Absolutely.  
What if I want to ~~strikethrough~~?
Wanna ==Highlight==?

---

## Blockquote

Want to emphasise importance of the text? Say no more.

```
> This is a blockquote.
> Want to write on a new line with space between?
>
> > And nested? No problem at all.
> >
> > > PS. you can **style** your text _as you want_.
```

> This is a blockquote. Want to write on a new line with space between?
> 
> > And nested? No problem at all.
> > 
> > > PS. you can **style** your text _as you want_. :

---

## Images

The best way is to simply drag & drop image from your computer directly. You can also create reference to image and assign it that way.  
Here is the syntax.

```
![text if the image fails to load](auto-generated-path-to-file-when-you-upload-image "Text displayed on hover")

[logo]: auto-generated-path-to-file-when-you-upload-image "Hover me"
![error text][logo]
```

![text if the image fails to load](https://user-images.githubusercontent.com/46372998/212541682-9907aaea-5198-45a9-8961-2acc8a98a0db.png "Text displayed on hover")

![error text](https://user-images.githubusercontent.com/46372998/212541682-9907aaea-5198-45a9-8961-2acc8a98a0db.png "Hover me")

---

## Links

Similar to images, links can also be inserted directly or by creating a reference. You can create both inline and block links.

```
[markdown-cheatsheet]: https://github.com/im-luka/markdown-cheatsheet
[docs]: https://github.com/adam-p/markdown-here

[Like it so far? Follow me on GitHub](https://github.com/im-luka)
[My Markdown Cheatsheet - star it if you like it][markdown-cheatsheet]
Find some great docs [here][docs]
```

[Like it so far? Follow me on GitHub](https://github.com/im-luka)  
[My Markdown Cheatsheet - star it if you like it](https://github.com/im-luka/markdown-cheatsheet)  
Find some great docs [here](https://github.com/adam-p/markdown-here)

---

## Code

You can cerate both inline and full block code snippets. You can also define programming language you were using in your snippet. All by using backticks.

```
    I created `.env` file at the root.
    Backticks inside backticks? `` `No problem.` ``

    ```
    {
      learning: "Markdown",
      showing: "block code snippet"
    }
    ```

    ```js
    const x = "Block code snippet in JS";
    console.log(x);
    ```
```

I created `.env` file at the root. Backticks inside backticks? `` `No problem.` ``

```
{
  learning: "Markdown",
  showing: "block code snippet"
}
```

```js
const x = "Block code snippet in JS";
console.log(x);
```

---

## Lists

As you can do in HTML, Markdown allows creating of both ordered and unordered lists.

### Ordered List


```
1. HTML
2. CSS
3. Javascript
4. React
7. I'm Frontend Dev now 👨🏼‍🎨
```

1. HTML
2. CSS
3. Javascript
4. React
5. I'm Frontend Dev now 👨🏼‍🎨

### Unordered List

```
- Node.js
+ Express
* Nest.js
- Learning Backend ⌛️
```

- Node.js

- Express

- Nest.js

- Learning Backend ⌛️

### Mixed List

You can also mix both of the lists and create sublists.  
**PS.** Try not to create lists deeper than two levels. It is the best practice.

```
1. Learn Basics
   1. HTML
   2. CSS
   7. Javascript
2. Learn One Framework
   - React 
     - Router
     - Redux
   * Vue
   + Svelte
```

1. Learn Basics
    1. HTML
    2. CSS
    3. Javascript
2. Learn One Framework
    
    - React
        - Router
        - Redux
    
    - Vue
    
    - Svelte

---

## Table

Great way to display well-arranged data. Use "|" symbol to separate columns and ":" symbol to align row content.

```
| Left Align (default) | Center Align | Right Align |
| :------------------- | :----------: | ----------: |
| React.js             | Node.js      | MySQL       |
| Next.js              | Express      | MongoDB     |
| Vue.js               | Nest.js      | Redis       |
```

| Left Align (default) | Center Align | Right Align |
| :------------------- | :----------: | ----------: |
| React.js             |   Node.js    |       MySQL |
| Next.js              |   Express    |     MongoDB |
| Vue.js               |   Nest.js    |       Redis |

---

## Task List

Keeping track of the tasks that are done, and those that need to be done.

```
- [x] Learn Markdown
- [ ] Learn Frontend Development
- [ ] Learn Full Stack Development
```

- [x]  Learn Markdown
- [ ]  Learn Frontend Development
- [ ]  Learn Full Stack Development

---

## Footnote


Want to describe something at the end of the file? Use footnote!

```
#### I am working on a new project. [^1]
[^1]: Stack is: React, Typescript, Tailwind CSS  

Project is about music & movies.

##### Hope you will like it. [^see]
[^see]: Loading... ⌛️
```

#### I am working on a new project. 

Project is about music & movies.

##### Hope you will like it.


---

# Jump to section


You can give ID to a section so that you can jump straight to that part of the file from wherever you are.

```
[[Headings]]
```

[[Headings]]

---

# Horizontal Line

You can use asterisks, hyphens or underlines (*, -, _) to create horizontal line.  
The only rule is that you must include at least three chars of the symbol.

```
First Horizontal Line

***

Second One

-----

Third

_________
```

First Horizontal Line

***

Second One

---

Third

-------

# List of More Things-
```dataview 
table Product from "Use"
```


