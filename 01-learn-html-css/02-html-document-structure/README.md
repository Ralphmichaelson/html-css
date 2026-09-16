# HTML Document Structure 🏗️

This folder focuses on the basic structure of an HTML document and how the different parts of a webpage are organized.

The `index.html` file demonstrates the main sections of an HTML document, including the `<head>`, `<body>`, `<header>`, `<main>`, `<section>`, and `<footer>`.

---

## 📌 What is HTML Document Structure?

An HTML document follows a specific structure that helps browsers understand and display a webpage correctly.

A basic HTML document looks like this:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <!-- Information about the webpage -->
</head>

<body>
    <!-- Content displayed on the webpage -->
</body>

</html>
```

Each part has a different purpose.

---

## 1. `<!DOCTYPE html>`

```html
<!DOCTYPE html>
```

The `DOCTYPE` declaration tells the browser that the document is written using **HTML5**.

It should normally be the first line of an HTML document.

It is not an HTML element. It is a declaration that tells the browser which HTML standard to use.

---

## 2. The `<html>` Element

```html
<html lang="en">
```

The `<html>` element is the **root element** of the document.

All other HTML elements are placed inside it.

### `lang` Attribute

```html
lang="en"
```

The `lang` attribute tells browsers and assistive technologies what language the page is written in.

For example:

```html
<html lang="en">
```

means the document is written in English.

---

## 3. The `<head>` Element

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>HTML Document Structure</title>
</head>
```

The `<head>` contains information **about the webpage**.

Most of the information inside the `<head>` is not displayed directly as page content.

The `head` can contain things such as:

* Page title
* Character encoding
* Viewport settings
* CSS links
* Metadata
* External resources

---

## 4. Character Encoding

```html
<meta charset="UTF-8">
```

This tells the browser which character encoding should be used.

`UTF-8` supports a very large range of characters, symbols, and languages.

For example:

```text
Hello 👋
Kenya 🇰🇪
HTML 🌐
```

Using UTF-8 helps ensure these characters are displayed correctly.

---

## 5. The Viewport Meta Tag

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This helps webpages display properly on different screen sizes, especially mobile devices.

### `width=device-width`

Tells the browser to make the webpage width match the device's screen width.

### `initial-scale=1.0`

Sets the initial zoom level to 100%.

This is an important part of making webpages responsive.

---

## 6. The `<title>` Element

```html
<title>HTML Document Structure</title>
```

The `<title>` specifies the title of the webpage.

It is usually displayed:

* In the browser tab
* In bookmarks
* In browser history

It is different from an `<h1>` because `<title>` belongs to the document's metadata, while `<h1>` is visible page content.

---

# 7. The `<body>` Element

```html
<body>

</body>
```

The `<body>` contains the main content that users see on the webpage.

This can include:

* Headings
* Paragraphs
* Images
* Links
* Lists
* Forms
* Tables
* Videos
* Sections
* Navigation
* Other HTML elements

In this project, the body contains the actual webpage content.

---

# 8. The `<header>` Element

```html
<header>
    <h1>Understanding HTML Document Structure</h1>
    <p>
        This page demonstrates how a basic HTML document is organized.
    </p>
</header>
```

The `<header>` represents introductory content for a page or section.

It commonly contains things such as:

* Headings
* Introduction text
* Logos
* Navigation
* Other introductory content

A `<header>` does **not** have to appear only once on a webpage.

---

# 9. The `<main>` Element

```html
<main>

</main>
```

The `<main>` element contains the **main content** of the webpage.

It should contain content that is directly related to the primary purpose of the page.

For example:

```html
<main>
    <section>
        <h2>The Head Section</h2>
    </section>

    <section>
        <h2>The Body Section</h2>
    </section>
</main>
```

Using `<main>` makes the structure of the webpage clearer and improves accessibility.

---

# 10. The `<section>` Element

```html
<section>
    <h2>The Head Section</h2>
    <p>
        The head contains information about the webpage.
    </p>
</section>
```

A `<section>` represents a distinct section of related content.

A page can contain multiple sections.

For example:

```html
<section>
    <h2>About</h2>
</section>

<section>
    <h2>Projects</h2>
</section>

<section>
    <h2>Contact</h2>
</section>
```

Each section should generally have a meaningful heading.

---

# 11. The `<footer>` Element

```html
<footer>
    <p>Created as part of my HTML learning journey.</p>
</footer>
```

The `<footer>` represents the footer of a page or section.

It can contain information such as:

* Copyright information
* Contact information
* Author information
* Related links
* Additional information

A webpage can have a footer for the entire page, while individual sections can also have their own footer.

---

# 12. Parent and Child Elements

HTML elements can be placed inside other elements.

For example:

```html
<main>
    <section>
        <h2>HTML Structure</h2>
        <p>HTML elements can be nested inside one another.</p>
    </section>
</main>
```

Here:

* `<main>` is the parent of `<section>`
* `<section>` is a child of `<main>`
* `<h2>` is a child of `<section>`
* `<p>` is a child of `<section>`

This creates a hierarchy.

```text
main
└── section
    ├── h2
    └── p
```

Understanding this hierarchy is important because HTML documents are built using nested elements.

---

# 13. Nesting

**Nesting** means placing one HTML element inside another.

Correct nesting:

```html
<p>
    This is <strong>important</strong> information.
</p>
```

Incorrect nesting:

```html
<p>
    This is <strong>important information.
</p>
</strong>
```

Elements should be properly opened and closed in the correct order.

---

# 14. Comments

The example also contains an HTML comment:

```html
<!-- Main content of the webpage -->
```

Comments are written for developers and are not displayed as normal webpage content.

Syntax:

```html
<!-- Your comment here -->
```

Comments can be useful for:

* Explaining sections of code
* Organizing large files
* Leaving notes
* Temporarily explaining code

---

# 🧩 Putting Everything Together

The structure of the `index.html` file can be visualized like this:

```text
<!DOCTYPE html>
        │
        ▼
     <html>
       │
       ├── <head>
       │     ├── <meta>
       │     ├── <meta>
       │     └── <title>
       │
       └── <body>
             │
             ├── <header>
             │     ├── <h1>
             │     └── <p>
             │
             ├── <main>
             │     │
             │     ├── <section>
             │     │     ├── <h2>
             │     │     └── <p>
             │     │
             │     └── <section>
             │           ├── <h2>
             │           └── <p>
             │
             └── <footer>
                   └── <p>
```

This shows how an HTML document is organized as a hierarchy of nested elements.

---

# 📖 Important Concepts Learned

| Concept           | Purpose                                |
| ----------------- | -------------------------------------- |
| `<!DOCTYPE html>` | Declares the document as HTML5         |
| `<html>`          | Root element of the document           |
| `lang`            | Specifies the document language        |
| `<head>`          | Contains information about the webpage |
| `<meta>`          | Provides metadata                      |
| `<title>`         | Sets the browser/page title            |
| `<body>`          | Contains visible webpage content       |
| `<header>`        | Contains introductory content          |
| `<main>`          | Contains the primary content           |
| `<section>`       | Groups related content                 |
| `<footer>`        | Contains footer information            |
| Nesting           | Places elements inside other elements  |
| Comments          | Adds notes to the code                 |

---

# 🧪 What I Practiced

In `index.html`, I practiced:

* Creating a complete HTML5 document
* Using `<!DOCTYPE html>`
* Creating the root `<html>` element
* Setting the document language with `lang`
* Creating a `<head>` section
* Adding character encoding
* Adding viewport settings
* Setting a page title
* Creating a `<body>` section
* Organizing content using `<header>`, `<main>`, `<section>`, and `<footer>`
* Nesting HTML elements
* Using HTML comments
* Maintaining proper indentation

---

# 🔑 Key Takeaways

1. Every HTML document has a basic structure.
2. `<html>` is the root element.
3. `<head>` contains information about the document.
4. `<body>` contains the webpage's visible content.
5. HTML elements can be nested inside one another.
6. `<main>`, `<header>`, `<section>`, and `<footer>` help organize webpage content.
7. Proper indentation makes HTML easier to read and maintain.
8. HTML structure creates a hierarchy between parent and child elements.

---

## 📁 Folder Contents

```text
02-html-document-structure/
├── index.html
└── README.md
```

`index.html` contains the practical example, while this `README.md` explains the concepts demonstrated in the code.