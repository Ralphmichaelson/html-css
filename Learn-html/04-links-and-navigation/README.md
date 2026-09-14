# HTML Links and Navigation

## Introduction

Links are an important part of the web. They allow users to move from one webpage to another, visit external websites, jump to a specific section of a page, or contact someone through email.

In HTML, links are created using the `<a>` element, also called the **anchor element**.

## 1. The Anchor Element

The basic syntax of an HTML link is:

```html
<a href="URL">Link Text</a>
```

### Explanation

* `<a>` — opening anchor tag.
* `href` — attribute that specifies the destination of the link.
* `URL` — address of the destination.
* `Link Text` — clickable text displayed to the user.
* `</a>` — closing anchor tag.

### Example

```html
<a href="https://www.github.com">Visit GitHub</a>
```

The text **Visit GitHub** becomes clickable.

---

## 2. The `href` Attribute

The `href` attribute means **Hypertext Reference**.

It tells the browser where the link should take the user.

```html
<a href="https://www.example.com">Visit Example</a>
```

Without an `href` attribute, the anchor element does not have a normal destination.

---

## 3. External Links

An external link takes users to another website.

### Example

```html
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML">
    Learn HTML on MDN
</a>
```

External links commonly use complete URLs beginning with:

```text
https://
```

Other examples:

```html
<a href="https://github.com">GitHub</a>

<a href="https://www.w3.org/">W3C</a>
```

---

## 4. Internal Links

An internal link connects pages within the same website or project.

For example, if a project contains:

```text
website/
├── index.html
├── about.html
└── contact.html
```

The homepage can link to the other pages:

```html
<a href="about.html">About Us</a>

<a href="contact.html">Contact Us</a>
```

The value of `href` points to the filename of the destination page.

### Important

The destination file must exist, and the path must be correct.

---

## 5. Links to Sections on the Same Page

HTML can also create links that jump to a particular section of the current page.

First, give the target element an `id`:

```html
<section id="about">
    <h2>About This Page</h2>
    <p>This section contains information about the page.</p>
</section>
```

Then link to that `id` using `#`:

```html
<a href="#about">Go to About</a>
```

### How it works

```text
href="#about"
       ↓
id="about"
```

The `href` value and the `id` value must match.

---

## 6. The `id` Attribute

The `id` attribute gives an HTML element a unique identifier.

Example:

```html
<h2 id="resources">Resources</h2>
```

A link can target this heading:

```html
<a href="#resources">View Resources</a>
```

An `id` should be unique within a page.

---

## 7. Opening Links in a New Tab

The `target="_blank"` attribute tells the browser to open the destination in a new tab or browsing context.

### Example

```html
<a href="https://github.com" target="_blank" rel="noopener noreferrer">
    Visit GitHub
</a>
```

### Explanation

* `target="_blank"` — requests a new tab or browsing context.
* `rel="noopener noreferrer"` — adds protection and prevents the destination from receiving the original page's referrer information.

Use this carefully. Users should generally understand when a link will open somewhere new.

---

## 8. Email Links

HTML can create a link that opens the user's default email application.

Use the `mailto:` scheme:

```html
<a href="mailto:example@email.com">Send Me an Email</a>
```

When clicked, the link may open an email application with the recipient already filled in.

You can also include a subject:

```html
<a href="mailto:example@email.com?subject=HTML%20Question">
    Ask an HTML Question
</a>
```

The `%20` represents a space in a URL.

---

## 9. Navigation Menus

A navigation menu helps users move between important parts of a website.

The semantic `<nav>` element is commonly used to contain navigation links.

### Example

```html
<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
</nav>
```

The `<nav>` element describes a section containing navigation links.

It does not automatically create a visual menu. CSS is used later to style the links.

---

## 10. Descriptive Link Text

Link text should clearly explain where the link leads.

### Good example

```html
<a href="https://developer.mozilla.org/">
    Read HTML documentation
</a>
```

### Less helpful example

```html
<a href="https://developer.mozilla.org/">Click here</a>
```

Descriptive text is more useful for users and improves accessibility, especially for people using screen readers.

---

## 11. Understanding the `index.html` Example

The practical example contains several types of links.

### Navigation links

```html
<a href="#about">About</a>
<a href="#resources">Resources</a>
<a href="#contact">Contact</a>
```

These jump to sections on the same page.

### External website link

```html
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML">
    MDN Web Docs
</a>
```

This opens an external website.

### New-tab link

```html
<a href="https://github.com/" target="_blank" rel="noopener noreferrer">
    Visit GitHub
</a>
```

This requests that GitHub open in a new tab.

### Email link

```html
<a href="mailto:example@email.com">email</a>
```

This creates a link for sending an email.

---

## 12. Common Link Syntax

| Purpose              | Syntax                                        |
| -------------------- | --------------------------------------------- |
| External website     | `<a href="https://example.com">Example</a>`   |
| Another page         | `<a href="about.html">About</a>`              |
| Same-page section    | `<a href="#about">About</a>`                  |
| New tab              | `<a href="URL" target="_blank">Open</a>`      |
| Email                | `<a href="mailto:name@example.com">Email</a>` |
| Navigation container | `<nav>...</nav>`                              |

---

## 13. Common Mistakes

### Mistake 1: Forgetting the `href` attribute

```html
<a>Visit GitHub</a>
```

This does not create a normal working link.

### Mistake 2: Using the wrong file path

```html
<a href="abt.html">About</a>
```

If the actual file is named `about.html`, the link will not work.

### Mistake 3: Incorrect section ID

```html
<a href="#about">About</a>

<section id="information">
    ...
</section>
```

The link will not find the section because `about` and `information` do not match.

### Mistake 4: Forgetting quotation marks

```html
<a href=https://example.com>Example</a>
```

Use quotation marks around attribute values:

```html
<a href="https://example.com">Example</a>
```

### Mistake 5: Using unclear link text

Avoid using only phrases such as `Click here` when more descriptive text is possible.

---

## 14. What I Practiced

In `index.html`, I practiced:

* Creating links with the `<a>` element.
* Using the `href` attribute.
* Linking to external websites.
* Creating links to sections on the same page.
* Using the `id` attribute as a link target.
* Opening a link in a new tab.
* Creating an email link.
* Organizing links inside a `<nav>` element.
* Writing descriptive link text.

## Key Takeaways

* The `<a>` element creates hyperlinks.
* The `href` attribute specifies the destination.
* External links use complete URLs.
* Internal links can point to another HTML file.
* A link beginning with `#` targets an element with a matching `id`.
* The `<nav>` element identifies a navigation section.
* `target="_blank"` requests a new browsing context.
* Descriptive link text improves usability and accessibility.
* CSS is used to style links and navigation menus.

## Folder Contents

```text
04-links-and-navigation/
├── index.html
└── README.md
```
