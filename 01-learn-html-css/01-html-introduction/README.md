# HTML Introduction 🌐

HTML (**HyperText Markup Language**) is the standard markup language used to structure content on webpages.

This section covers the fundamental concepts behind HTML syntax, elements, tags, attributes, and the basic structure of an HTML document.

---

## 📌 What is HTML?

HTML is used to give a webpage its **structure**.

It tells the browser what different pieces of content are, such as:

* Headings
* Paragraphs
* Links
* Images
* Lists
* Forms
* Tables

HTML is **not a programming language**. It is a **markup language**.

---

## 🧩 HTML Syntax

HTML uses **tags** to describe and structure content.

A common HTML pattern looks like this:

```html
<tag>Content</tag>
```

For example:

```html
<p>Hello World!</p>
```

Here:

* `<p>` is the **opening tag**
* `Hello World!` is the **content**
* `</p>` is the **closing tag**
* The complete structure is an **HTML element**

---

## 🧱 HTML Elements

An HTML element is a complete piece of HTML.

For example:

```html
<h1>Welcome to My Website</h1>
```

This consists of:

```text
Opening tag → <h1>
Content     → Welcome to My Website
Closing tag → </h1>
```

Together, they form an **`h1` element**.

### Some elements don't have closing tags

For example:

```html
<br>
<img src="image.jpg" alt="A photo">
```

These are commonly called **void elements** because they don't contain content between an opening and closing tag.

---

## 🏷️ HTML Tags

A **tag** is the markup used to create or identify an element.

Examples:

```html
<h1>
<p>
<a>
<img>
```

It is useful to remember:

> **Tag = the markup**
> **Element = the complete structure**

For example:

```html
<p>Hello</p>
```

`<p>` and `</p>` are tags, while the entire `<p>Hello</p>` is the element.

---

## ⚙️ HTML Attributes

Attributes provide **additional information** about an element.

They are usually written inside the opening tag:

```html
<tag attribute="value">Content</tag>
```

Example:

```html
<a href="https://example.com">Visit Example</a>
```

Here:

* `<a>` is the element's tag
* `href` is an attribute
* `"https://example.com"` is the attribute value
* `Visit Example` is the content

Another example:

```html
<img src="photo.jpg" alt="My photo">
```

The `src` and `alt` are attributes of the `<img>` element.

---

# 🏗️ Basic HTML Document Structure

A basic HTML document looks like this:

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
</head>

<body>

    <h1>Hello, World! 👋</h1>

    <p>Welcome to my webpage.</p>

</body>

</html>
```

Let's break it down.

---

## `<!DOCTYPE html>`

```html
<!DOCTYPE html>
```

This tells the browser that the document uses **HTML5**.

It is placed at the very beginning of an HTML document.

---

## `<html>`

```html
<html lang="en">
```

The `<html>` element is the **root element** of the webpage.

Everything else belongs inside it.

The `lang="en"` attribute tells browsers and assistive technologies that the main language of the page is English.

---

## `<head>`

```html
<head>
    ...
</head>
```

The `<head>` contains information about the webpage.

Much of this information is not directly displayed as content on the page.

It can contain things such as:

* Page title
* Character encoding
* Viewport settings
* Links to CSS
* Metadata

---

## `<title>`

```html
<title>My Website</title>
```

The `<title>` sets the title shown in the browser tab.

It is different from a visible heading such as `<h1>`.

---

## `<body>`

```html
<body>
    ...
</body>
```

The `<body>` contains the content that appears on the webpage.

For example:

```html
<h1>Hello, World!</h1>
<p>Welcome to my webpage.</p>
```

---

# 💬 HTML Comments

Comments allow you to leave notes inside your HTML code.

They are written like this:

```html
<!-- This is a comment -->
```

Comments are not displayed on the webpage.

They can be useful for:

* Explaining code
* Organizing sections
* Leaving notes for yourself
* Temporarily disabling code

Example:

```html
<!-- Main heading -->
<h1>My Website</h1>
```

---

# 🧪 Example

The `index.html` file in this folder demonstrates the basic concepts covered in this section.

A simplified example:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First HTML Page</title>
</head>

<body>

    <!-- Main heading -->
    <h1>Hello, World! 👋</h1>

    <!-- Paragraph -->
    <p>My name is Michael Kanyugo.</p>

</body>

</html>
```

---

# 🧩 Elements Used

| Element / Syntax  | Purpose                          |
| ----------------- | -------------------------------- |
| `<!DOCTYPE html>` | Declares the document as HTML5   |
| `<html>`          | Root element of the document     |
| `<head>`          | Contains document information    |
| `<meta>`          | Provides metadata                |
| `<title>`         | Sets the browser-tab title       |
| `<body>`          | Contains visible webpage content |
| `<h1>`            | Creates a main heading           |
| `<p>`             | Creates a paragraph              |
| `<!-- -->`        | Creates an HTML comment          |

---

# 📝 Key Concepts

### HTML

The markup language used to structure webpages.

### Tag

The markup used to define an element.

### Element

The complete HTML structure.

### Attribute

Additional information added to an element.

### Content

The information placed inside an element.

### Document Structure

The overall organization of an HTML document.

---

# 💡 Key Takeaways

* HTML provides the **structure** of a webpage.
* HTML uses **tags** to create elements.
* Elements can contain **content**.
* Attributes provide additional information about elements.
* `<!DOCTYPE html>` declares an HTML5 document.
* `<html>` is the root element.
* `<head>` contains document information.
* `<body>` contains the visible webpage content.
* Comments can be used to document HTML code.

---

## 🌱 Practice

The goal of this section is not to memorize every HTML element.

The important thing is to understand how HTML is structured and become familiar with the syntax through practice.

> **Learn → Experiment → Understand → Build 🚀**

---

### 📂 Folder Contents

```text
01-html-introduction/
├── index.html
└── README.md
```

**`index.html`** → Practical HTML example
**`README.md`** → Notes and explanations
