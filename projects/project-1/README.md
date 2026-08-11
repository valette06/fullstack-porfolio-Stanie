# Day 3 – HTML Resume & File Paths

## Project Overview

Today I practiced the HTML concepts I learned during the previous lessons and combined them with my new topic: **HTML file paths**.

Instead of practicing individual HTML tags separately, I created an **HTML resume webpage** that contains my professional summary, career objective, work experience, education, technical skills, and links to other pages.

The goal of this exercise was to practice choosing the appropriate HTML elements myself and understand how different files and folders are connected using relative paths.

---

## 🎯 What I Practiced

During this project, I practiced:

- HTML document structure
- Headings and heading hierarchy
- Paragraphs
- Line breaks
- Horizontal rules
- Strong/important text
- Unordered lists
- List items
- Anchor tags
- HTML attributes
- Relative file paths
- Connecting multiple HTML pages
- Organizing content into meaningful sections

---

# 📂 Understanding HTML File Paths

One of the main concepts I learned today was how HTML finds files located in different directories.

## Current Directory

```text
./
```

means:

**Start from the current directory.**

Example:

```html
<img src="./profile.png" alt="Profile photo">
```

If `profile.png` is located in the same directory as my HTML file, the browser can find it using this path.

---

## Entering Another Directory

If my project looks like:

```text
project/
│
├── index.html
│
└── images/
    └── profile.png
```

I can access the image using:

```html
<img src="./images/profile.png" alt="Profile photo">
```

I can think about this path as:

```text
Start where index.html is
        ↓
enter images/
        ↓
find profile.png
```

---

## Parent Directory

```text
../
```

means:

**Go up one directory.**

For example:

```text
project/
│
├── images/
│   └── profile.png
│
└── pages/
    └── about.html
```

If I am inside `about.html`, I first need to leave the `pages` directory before I can enter `images`.

```html
<img src="../images/profile.png" alt="Profile photo">
```

I can think about this as:

```text
about.html
    ↓
../
Go up to project/
    ↓
images/
    ↓
profile.png
```

---

## Going Up Multiple Directories

Each additional `../` means going up another directory.

```text
../      = up one directory

../../   = up two directories

../../../ = up three directories
```

This helped me understand a relative path such as:

```text
../../exercises/4.1+Webpages/public/about.html
```

The browser follows the path starting from the location of the HTML file.

---

# 🔗 Anchor Tags

I practiced connecting HTML pages using the anchor element.

```html
<a href="path-to-page">Connect With Me</a>
```

I learned that:

- `<a>` creates the hyperlink.
- `href` specifies the destination.
- The text between `<a>` and `</a>` becomes clickable.

For external websites, I can also use:

```html
target="_blank"
```

to open the destination in a new browser tab.

---

# 🖼️ Images

I practiced displaying images using:

```html
<img src="image-path" alt="Image description">
```

I learned that:

- `<img>` tells the browser to display an image.
- `src` tells the browser where the image is located.
- `alt` provides an alternative description of the image.
- `<img>` is a void element and does not require a closing `</img>` tag.

The `src` attribute also gave me additional practice with relative file paths.

---

# 📝 HTML Resume Project

For my main exercise, I created an HTML resume containing:

### Professional Summary

A summary of my professional background and transition from DevOps and Platform Engineering into Full Stack Development.

### Career Objective

My goal of combining my infrastructure and DevOps experience with software development skills.

### Work Experience

I structured my previous professional experience using headings and paragraphs.

### Education

I practiced using unordered lists to organize my educational background.

### Technical Skills

I organized my technical skills into different categories using lists.

---

# HTML Structure and Nesting

Today I also learned more about properly nesting HTML elements.

One mistake I corrected was placing a `<ul>` inside a `<p>`.

Incorrect:

```html
<p>
    <ul>
        <li>HTML</li>
    </ul>
</p>
```

Better structure:

```html
<ul>
    <li>HTML</li>
</ul>
```

I learned that HTML elements have structural rules and that not every element should be placed inside another element.

---

# Heading Hierarchy

I practiced organizing my resume using heading levels.

I learned to think about headings as a hierarchy:

```text
h1 → Main page title

    h2 → Major section

        h3 → Subsection

            h4 → Smaller subsection
```

For my resume, my name can be the main `<h1>`, while sections such as Work Experience, Education, and Technical Skills can use `<h2>`.

---

# Important Concepts I Want to Remember

### HTML Structure

```text
DOCTYPE → tells the browser this is an HTML5 document

html → root of the HTML document

head → information about the webpage

body → visible webpage content
```

### Lists

```text
ul → unordered/bullet list

ol → ordered/numbered list

li → individual list item
```

### Links

```text
a → creates a hyperlink

href → destination of the hyperlink

target="_blank" → opens the destination in a new tab
```

### Images

```text
img → displays an image

src → location of the image

alt → alternative description
```

### File Paths

```text
./       → current directory

../      → parent directory

../../   → go up two directories

folder/  → enter a directory
```

---

# Mistakes I Corrected

During today's practice, I learned from several mistakes:

- I learned not to place `<ul>` inside `<p>`.
- I improved my heading hierarchy.
- I practiced giving each skill its own `<li>`.
- I learned the difference between `<b>` and semantic `<strong>`.
- I practiced using relative paths to navigate between directories.
- I learned that file paths depend on the location of the HTML file I am currently working from.

---

# ✅ Day 3 Reflection

Today was an important step because I moved from practicing individual HTML tags to using multiple HTML concepts together to build a real webpage.

I am becoming more comfortable looking at content and deciding which HTML element should represent it instead of simply copying HTML syntax.

The biggest concept I learned today was **relative file paths**.

I now understand that when creating a relative path, I should first ask:

> **Where is my current HTML file, and how do I navigate from that location to the file I want?**

This way of thinking makes it easier to understand paths instead of memorizing them.

I also built an HTML resume that allowed me to combine concepts from my previous lessons, including headings, paragraphs, lists, links, attributes, line breaks, horizontal rules, and page structure.

##  Next Step

Continue strengthening my HTML fundamentals through independent practice before moving deeper into CSS and webpage styling.