# Common HTML Mistakes

This section documents common HTML mistakes, why they can cause problems, and how to correct them.

The examples in `index.html` are designed as a practical reference for reviewing and improving HTML code.

## 1. Incorrect Nesting

HTML elements should be properly nested.

### Incorrect

```html
<p>
    This is <strong>important information.
</p>
</strong>
```

The `<strong>` element was opened inside the paragraph but closed after the paragraph.

### Correct

```html
<p>
    This is <strong>important</strong> information.
</p>
```

The last element opened should generally be the first one closed.

---

## 2. Missing Closing Tags

Some HTML elements require closing tags.

### Incorrect

```html
<p>
    This paragraph is missing its closing tag.
```

### Correct

```html
<p>
    This paragraph is correctly closed.
</p>
```

Missing closing tags can make the document structure unclear and may produce unexpected rendering.

> Some HTML elements, such as `<img>` and `<input>`, are void elements and do not have closing tags.

---

## 3. Using Headings Only for Appearance

Headings should describe the structure of the content, not simply make text larger or smaller.

### Not Recommended

```html
<h4>Main Page Title</h4>
```

### Better

```html
<h1>Main Page Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>
```

CSS should be used to change the visual size or appearance of a heading.

---

## 4. Using Poor Link Text

Link text should describe where the link leads.

### Not Recommended

```html
<a href="https://developer.mozilla.org/">
    Click here
</a>
```

### Better

```html
<a href="https://developer.mozilla.org/">
    Read HTML documentation
</a>
```

Descriptive link text helps users understand links more easily, including people using assistive technologies.

---

## 5. Missing `alt` Text on Images

Meaningful images should have appropriate alternative text.

### Not Recommended

```html
<img src="laptop.jpg">
```

### Better

```html
<img
    src="laptop.jpg"
    alt="Laptop displaying HTML code"
>
```

The `alt` attribute provides a text alternative when an image cannot be seen.

For purely decorative images, an empty `alt` attribute may be appropriate:

```html
<img src="decoration.png" alt="">
```

---

## 6. Using Placeholder Text Instead of Labels

A placeholder is a hint, not a replacement for a form label.

### Not Recommended

```html
<input
    type="email"
    placeholder="Enter your email"
>
```

### Better

```html
<label for="email">Email:</label>

<input
    type="email"
    id="email"
    name="email"
    placeholder="Enter your email"
>
```

The label identifies the field even when the placeholder disappears.

---

## 7. Using Generic Elements for Everything

Generic elements such as `<div>` are useful, but they should not replace semantic elements when a suitable semantic element exists.

### Not Recommended

```html
<div>
    Navigation links
</div>
```

### Better

```html
<nav>
    Navigation links
</nav>
```

Other semantic elements include:

```html
<header>
<main>
<section>
<article>
<aside>
<footer>
```

Choose elements based on their meaning.

---

## 8. Missing the `lang` Attribute

The root `<html>` element should identify the primary language of the document.

### Not Recommended

```html
<html>
```

### Better

```html
<html lang="en">
```

The `lang` attribute helps browsers and assistive technologies understand the document's language.

---

## 9. Missing Character Encoding

A page should normally declare its character encoding.

### Recommended

```html
<meta charset="UTF-8">
```

UTF-8 supports a wide range of characters and symbols.

For example:

```text
Hello 👋
Kenya 🇰🇪
HTML 🌐
```

---

## 10. Using Tables for Page Layout

Tables should be used for **tabular data**, not for building the general layout of a webpage.

### Not Recommended

```html
<table>

    <tr>
        <td>Header</td>
    </tr>

    <tr>
        <td>Main content</td>
    </tr>

</table>
```

### Better

```html
<header>
    Header
</header>

<main>
    Main content
</main>
```

CSS should be used for page layout.

---

## 11. Forgetting the Viewport Meta Tag

Modern webpages should include the viewport declaration.

```html
<meta
    name="viewport"
    content="width=device-width, initial-scale=1.0"
>
```

This helps the page behave appropriately on different screen sizes, especially mobile devices.

---

## 12. Poor Indentation

HTML can work even when everything is placed on one line, but poorly formatted code is difficult to read and maintain.

### Hard to Read

```html
<main><section><h2>About</h2><p>Information</p></section></main>
```

### Better

```html
<main>

    <section>

        <h2>About</h2>

        <p>
            Information
        </p>

    </section>

</main>
```

Consistent indentation makes nested structures easier to understand.

---

## 13. Duplicate IDs

An ID should uniquely identify an element within a document.

### Incorrect

```html
<p id="intro">First paragraph</p>
<p id="intro">Second paragraph</p>
```

### Better

```html
<p id="intro">First paragraph</p>
<p id="second">Second paragraph</p>
```

Classes can be reused across many elements, while IDs are intended to identify individual elements.

---

## 14. Using Outdated Presentation Attributes

HTML should mainly provide structure and meaning. CSS should handle presentation.

### Not Recommended

```html
<p align="center">
    Centered text
</p>
```

### Better

```html
<p class="center-text">
    Centered text
</p>
```

CSS:

```css
.center-text {
    text-align: center;
}
```

Separating structure from presentation makes websites easier to maintain.

---

## 15. Forgetting HTML Validation

A page may appear to work even when the HTML contains mistakes.

Validation can help identify:

* Invalid nesting
* Incorrect syntax
* Invalid attributes
* Structural problems
* Other HTML errors

Validation is useful during development and learning because it can help reveal mistakes that are easy to overlook.

---

# Quick Reference Table

| Mistake                      | Better Practice                      |
| ---------------------------- | ------------------------------------ |
| Incorrect nesting            | Properly nest elements               |
| Missing closing tags         | Close elements correctly             |
| Headings chosen for size     | Use headings for structure           |
| "Click here" links           | Use descriptive link text            |
| Missing image `alt`          | Provide appropriate alternative text |
| Placeholder instead of label | Use `<label>` with form controls     |
| `<div>` for everything       | Use semantic HTML where appropriate  |
| Missing `lang`               | Add `lang` to `<html>`               |
| Missing character encoding   | Add `<meta charset="UTF-8">`         |
| Tables for layout            | Use semantic HTML and CSS            |
| Missing viewport             | Add the viewport meta tag            |
| Poor indentation             | Format code consistently             |
| Duplicate IDs                | Give each ID a unique value          |
| Presentation in HTML         | Use CSS for styling                  |
| No validation                | Check HTML for errors                |

---

# Common HTML Checklist

Before considering an HTML page complete, check:

```text
[ ] Doctype is included
[ ] html element has a lang attribute
[ ] charset is declared
[ ] viewport meta tag is included
[ ] title is descr
```
