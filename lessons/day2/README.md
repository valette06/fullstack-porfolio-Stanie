# Day 2 – HTML Practice

## Overview

Today I continued practicing HTML fundamentals.

My main goal was not just to memorize HTML syntax, but to understand what each HTML element does, why it is needed, and how different elements can work together.

Today I practiced:

- Unordered lists
- Ordered lists
- Nested lists
- List items
- Bold/important text
- Emphasized text
- Line breaks
- Horizontal lines
- Anchor tags
- Images
- HTML attributes

---

# 1. What is an unordered list `<ul>`?

`<ul>` stands for **Unordered List**.

It is used when I want to display a collection of items where the order of the items is not important.

For example, a list of technologies does not necessarily need to be numbered because HTML is not more important than CSS simply because it appears first.

Example:

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

The browser displays this as a bulleted list.

### What I learned

`<ul>` creates the list container, while `<li>` creates each individual item inside the list.

---

# 2. What is an ordered list `<ol>`?

`<ol>` stands for **Ordered List**.

It is used when the order or sequence of the items matters.

Example:

```html
<ol>
    <li>Learn HTML</li>
    <li>Learn CSS</li>
    <li>Learn JavaScript</li>
    <li>Learn React</li>
</ol>
```

The browser automatically numbers the items.

### How I remember the difference

```text
ul = Unordered List = bullets

ol = Ordered List = numbers

li = List Item = each item inside either list
```

---

# 3. What is `<li>`?

`<li>` stands for **List Item**.

It represents an individual item inside an ordered or unordered list.

For example:

```html
<ul>
    <li>GitHub</li>
    <li>Docker</li>
    <li>Kubernetes</li>
</ul>
```

The `<ul>` creates the list.

Each `<li>` represents one item in that list.

---

# 4. What is a nested list?

A nested list is a list placed inside another list item.

This allows me to create a hierarchy between information.

For example:

```html
<ul>
    <li>
        HTML
        <ol>
            <li>HTML Structure</li>
            <li>HTML Elements</li>
            <li>HTML Attributes</li>
        </ol>
    </li>
</ul>
```

The ordered list belongs to the HTML list item.

### Important rule I learned

When nesting lists, the nested `<ul>` or `<ol>` should normally be placed inside an `<li>`.

The structure is:

```text
List
└── List Item
    └── Nested List
        ├── List Item
        ├── List Item
        └── List Item
```

This helped me understand HTML parent-child relationships and nesting.

---

# 5. What does `<strong>` do?

The `<strong>` element represents text that has strong importance.

Browsers normally display `<strong>` text in bold.

Example:

```html
<p>I am learning <strong>HTML</strong>.</p>
```

The word HTML will normally appear bold.

I should not think of `<strong>` as only a visual styling tool. It also gives the text semantic importance.

---

# 6. What does `<em>` do?

`<em>` stands for **emphasis**.

It is used when I want to emphasize part of a sentence.

Example:

```html
<p>I am <em>really</em> enjoying HTML.</p>
```

Browsers normally display emphasized text in italics.

The important concept is that `<em>` gives meaning to the text, not just visual styling.

---

# 7. What does `<br>` do?

`<br>` creates a **line break**.

It tells the browser:

> Continue the following content on a new line.

For example:

```html
<p>
Current Role: DevOps Engineer<br>
Current Focus: Full Stack Development<br>
Goal: Full Stack Developer
</p>
```

The information appears on separate lines.

### Important thing I learned

`<br>` does not require a closing tag.

I do not write:

```html
<br></br>
```

I simply write:

```html
<br>
```

It is useful when I need a line break within the same block of content.

---

# 8. What does `<hr>` do?

`<hr>` creates a thematic break between sections of content.

Browsers normally display it as a horizontal line.

Example:

```html
<p>About Me information...</p>

<hr>

<h2>Technical Skills</h2>
```

It visually and semantically separates one topic from another.

Like `<br>`, `<hr>` does not need a closing tag.

---

# 9. What is an anchor `<a>` tag?

The `<a>` element is called the **anchor element**.

It is used to create hyperlinks.

A hyperlink allows the user to navigate to another destination.

For example:

```html
<a href="https://github.com">Visit GitHub</a>
```

The text:

```text
Visit GitHub
```

becomes clickable.

### How I understand it

I can think of `<a>` as saying:

> I want to create a link.

But the anchor still needs to know where the user should go.

That is where the `href` attribute becomes important.

---

# 10. What is `href`?

`href` is an HTML attribute commonly used with the anchor element.

It provides the destination of the hyperlink.

Example:

```html
<a href="https://github.com">GitHub</a>
```

I can think about it like this:

```text
<a>   = I want to create a link.

href  = Where should the link take the user?

GitHub = The clickable text.
```

An anchor can link to more than just another website. It can also link to another page, a location on the same page, an email address, or another resource.

---

# 11. What does `target="_blank"` do?

The `target` attribute controls where the linked destination opens.

When I use:

```html
<a href="https://github.com" target="_blank">GitHub</a>
```

`target="_blank"` tells the browser to open the destination in a **new browser tab or window**.

Without it, the browser will normally open the destination in the current tab.

### How I remember it

```text
href = WHERE am I going?

target = WHERE should the destination open?

_blank = Open a new browsing context, commonly a new tab.
```

---

# 12. What is the `<img>` tag?

The `<img>` element is used to display an image on a webpage.

Example:

```html
<img src="images.jpeg" alt="Cat sitting on a couch">
```

The `<img>` element tells the browser:

> I want to display an image here.

However, the browser still needs to know where the image is located.

That is the purpose of the `src` attribute.

---

# 13. What does `src` mean?

`src` stands for **source**.

It tells the browser where to find the resource that needs to be displayed.

For an image:

```html
<img src="images.jpeg" alt="Cat">
```

I can think about it like this:

```text
<img> = Display an image.

src = Where can the browser find the image?
```

If the browser cannot find the file specified in `src`, the image will not display correctly.

---

# 14. What does the `alt` attribute do?

`alt` stands for **alternative text**.

It provides a text description of an image.

Example:

```html
<img src="cat.jpeg" alt="Orange cat sitting on a couch">
```

The `alt` description is important for accessibility because screen readers can use it to communicate the meaning of an image to users who cannot see it.

It can also provide useful fallback information when an image cannot be loaded.

### What I learned

`alt` should normally describe the meaningful content or purpose of the image rather than simply saying:

```text
image
```

or:

```text
picture
```

A useful description would be:

```text
Orange cat sitting on a couch
```

---

# 15. Why doesn't `<img>` have a closing `</img>` tag?

`<img>` is a **void element**.

Void elements cannot contain child content, so they do not need a separate closing tag.

For example, a paragraph contains content:

```html
<p>Hello World</p>
```

There is content between:

```html
<p>
```

and:

```html
</p>
```

But an image gets the information it needs from attributes:

```html
<img src="cat.jpeg" alt="Cat">
```

There is no text or child content that needs to go between `<img>` and `</img>`.

Therefore, HTML does not use:

```html
<img>something</img>
```

---

# 16. What is an HTML attribute?

An HTML attribute provides additional information about an HTML element or affects its behavior.

Attributes are written inside the opening tag.

For example:

```html
<a href="https://github.com" target="_blank">GitHub</a>
```

Here:

- `href` is an attribute.
- `"https://github.com"` is its value.
- `target` is another attribute.
- `"_blank"` is its value.

Another example:

```html
<img src="cat.jpeg" alt="Orange cat">
```

Here:

- `src` tells the browser where to find the image.
- `alt` provides alternative text describing the image.

### How I understand attributes

The **element tells the browser what something is**.

The **attribute provides additional information about that element**.

For example:

```text
<a>     → This is a link.
href    → This is its destination.

<img>   → This is an image.
src     → This is where the image is located.
alt     → This describes the image.
```

---

# 17. What did I practice today?

Today I practiced combining multiple HTML elements instead of learning them individually.

I created nested structures containing:

```text
ul
 └── li
      └── ul
           └── li
                └── ol
                     └── li
```

I also practiced:

```text
<a href="...">...</a>

<img src="..." alt="...">

<strong>...</strong>

<em>...</em>

<br>

<hr>
```

This helped me understand that HTML elements work together to create a structured document.

---

# Key Concepts I Want to Remember

## Lists

```text
ul = unordered list
ol = ordered list
li = list item
```

## Links

```text
a = anchor/link
href = destination
target="_blank" = open in a new tab/window
```

## Images

```text
img = display an image
src = image source/location
alt = alternative description
```

## Text

```text
strong = strong importance
em = emphasis
br = line break
hr = thematic break
```

---

# Day 2 Reflection

Today I moved beyond basic HTML document structure and practiced combining HTML elements together.

The most important concept I learned was that HTML has a hierarchy. Elements can contain other elements, and their placement matters.

I also learned that HTML attributes provide additional information to elements. For example, an anchor element needs `href` to know its destination, while an image element needs `src` to know where the image is located.

Instead of only memorizing syntax, I am focusing on understanding what each element tells the browser and why I would use it.

My next goal is to understand **HTML file paths and relative paths**, so I can better understand how HTML finds images, pages, CSS files, and other resources inside a project.