# Semantic HTML & Modern Web Structure

This topic focuses on using semantic HTML elements to create webpages that have a clear, meaningful, and well-organized structure.

Semantic HTML helps developers, browsers, search engines, and assistive technologies understand the purpose of different parts of a webpage.

## What Is Semantic HTML?

Semantic HTML means using HTML elements according to the meaning and purpose of their content.

For example:

```html
<header>
```

communicates that the content is a header, while:

```html
<nav>
```

communicates that the content contains navigation.

This is more meaningful than using generic elements for everything.

## Semantic vs Non-Semantic Elements

### Semantic elements

Semantic elements describe the purpose of their content.

Examples:

```html
<header>
<nav>
<main>
<section>
<article>
<aside>
<footer>
<address>
```

### Non-semantic elements

The most common generic containers are:

```html
<div>
<span>
```

These elements do not describe the meaning of their content.

They are useful when no more appropriate semantic element exists.

## Basic Semantic Page Structure

A typical webpage can be organized like this:

```text
<body>
│
├── <header>
│   └── <nav>
│
├── <main>
│   ├── <section>
│   │   └── <article>
│   │
│   ├── <section>
│   │
│   └── <aside>
│
└── <footer>
```

This structure gives the webpage a clear hierarchy.

---

## The `<header>` Element

The `<header>` element contains introductory content for a webpage or a section.

Example:

```html
<header>

    <h1>Semantic HTML & Modern Web Structure</h1>

    <p>
        This page demonstrates semantic HTML.
    </p>

</header>
```

A header can contain:

* Headings
* Introductory text
* Logos
* Navigation
* Other introductory content

A webpage can also contain more than one `<header>`, for example, a separate header inside an article.

---

## The `<nav>` Element

The `<nav>` element contains major navigation links.

Example:

```html
<nav aria-label="Main navigation">

    <a href="#about">About</a>
    <a href="#topics">Topics</a>
    <a href="#contact">Contact</a>

</nav>
```

The `aria-label` gives the navigation a descriptive name for assistive technologies.

Not every group of links needs to be inside `<nav>`. It is intended for important navigation sections.

---

## The `<main>` Element

The `<main>` element contains the primary content of the webpage.

Example:

```html
<main>

    <section>
        <h2>About This Page</h2>
        <p>Main webpage content goes here.</p>
    </section>

</main>
```

A document should normally have one main `<main>` element representing its primary content.

---

## The `<section>` Element

A `<section>` represents a thematic grouping of related content.

Example:

```html
<section>

    <h2>About This Page</h2>

    <p>
        This section contains information about the page.
    </p>

</section>
```

Sections normally have a heading that describes their content.

For example:

```html
<section>
    <h2>Programming Languages</h2>
    ...
</section>
```

---

## The `<article>` Element

The `<article>` element represents a self-contained piece of content.

It is useful for content that could stand on its own.

Examples include:

* Blog posts
* News articles
* Forum posts
* Product reviews
* Individual publications

Example:

```html
<article>

    <h2>Why Semantic HTML Matters</h2>

    <p>
        Semantic HTML makes webpage structure clearer.
    </p>

</article>
```

An article can contain its own `<header>` and `<footer>`.

---

## The `<aside>` Element

The `<aside>` element contains content related to the surrounding content but not part of its main flow.

Example:

```html
<aside>

    <h3>Quick Tip</h3>

    <p>
        Choose an HTML element based on meaning.
    </p>

</aside>
```

Common uses include:

* Sidebars
* Related information
* Tips
* Advertisements
* Additional resources

---

## The `<footer>` Element

The `<footer>` contains closing or supporting information.

Example:

```html
<footer>

    <p>Created as part of my HTML learning journey.</p>

</footer>
```

A footer can contain:

* Copyright information
* Contact information
* Related links
* Author information
* Additional navigation

A webpage can have a page-level footer, and an `<article>` can also have its own footer.

---

## The `<address>` Element

The `<address>` element is used for contact information related to the page or its author.

Example:

```html
<address>
    Email:
    <a href="mailto:example@email.com">
        example@email.com
    </a>
</address>
```

It should be used for contact information rather than for ordinary physical addresses that have no contact meaning.

---

## `<div>` vs Semantic Elements

The `<div>` element is a generic block-level container.

Example:

```html
<div>
    <h2>My Content</h2>
    <p>Some information.</p>
</div>
```

It does not tell us what the content means.

Compare that with:

```html
<section>
    <h2>My Content</h2>
    <p>Some information.</p>
</section>
```

The `<section>` tells us that the content forms a meaningful section.

### When to use `<div>`

Use `<div>` when:

* No suitable semantic element exists.
* You need a generic container for CSS or JavaScript.
* The grouping does not have a specific semantic meaning.

Do not use `<div>` automatically for every part of a webpage.

---

## The `<span>` Element

`<span>` is a generic inline container.

Example:

```html
<p>
    I am learning
    <span>HTML</span>
    every day.
</p>
```

It is commonly used when styling or targeting a small piece of inline content.

Like `<div>`, `<span>` does not provide semantic meaning by itself.

---

## Heading Hierarchy

Semantic structure also includes using headings correctly.

HTML provides six heading levels:

```html
<h1>Main heading</h1>
<h2>Section heading</h2>
<h3>Subsection heading</h3>
<h4>Subsection heading</h4>
<h5>Subsection heading</h5>
<h6>Subsection heading</h6>
```

Headings should represent the hierarchy of the content.

A simplified structure might look like:

```text
<h1>Website Title</h1>
    ├── <h2>About</h2>
    ├── <h2>Services</h2>
    │      ├── <h3>Web Design</h3>
    │      └── <h3>Development</h3>
    └── <h2>Contact</h2>
```

Do not choose headings only because of their default visual size. CSS should be used when you need to change appearance.

---

## Accessibility and Semantic HTML

Semantic HTML can make webpages easier for assistive technologies to understand.

For example:

```html
<nav>
```

provides meaningful information that the content is navigation.

Likewise:

```html
<main>
```

identifies the primary content area.

This can help users who navigate webpages using screen readers or other assistive technologies.

### Important Accessibility Practices

Use:

* Meaningful semantic elements.
* Proper heading hierarchy.
* Descriptive link text.
* Labels for form controls.
* Alternative text for meaningful images.
* Appropriate ARIA attributes when necessary.

Semantic HTML should generally be preferred before adding ARIA unnecessarily.

---

## The `aria-label` Attribute

ARIA attributes can provide additional information for assistive technologies.

Example:

```html
<nav aria-label="Main navigation">
```

Here, `aria-label` gives the navigation a descriptive name.

ARIA can be useful when native HTML does not provide enough accessible information, but it should not replace semantic HTML when an appropriate HTML element already exists.

---

## The `<meta>` Description

The `<head>` of the example page contains:

```html
<meta
    name="description"
    content="A practical example of semantic HTML and modern webpage structure."
>
```

This provides a description of the webpage.

Meta information is not normally displayed as page content, but it can provide useful information about a webpage to browsers and search engines.

---

## Why Semantic HTML Matters

Using semantic HTML can provide several benefits:

| Benefit         | Explanation                                                       |
| --------------- | ----------------------------------------------------------------- |
| Readability     | Developers can understand the structure more easily.              |
| Maintainability | Well-structured code is easier to modify.                         |
| Accessibility   | Assistive technologies can better understand the page.            |
| SEO             | Clear structure can provide useful information to search engines. |
| Organization    | Different parts of the page have clear roles.                     |

Semantic HTML does not automatically make a website accessible or highly ranked in search engines, but it provides a strong foundation for both.

---

## Example of a Semantic Webpage

The main structure used in `index.html` is:

```html
<body>

    <header>

        <h1>Semantic HTML & Modern Web Structure</h1>

        <nav>
            ...
        </nav>

    </header>

    <main>

        <section>
            ...
        </section>

        <section>

            <article>
                ...
            </article>

            <aside>
                ...
            </aside>

        </section>

    </main>

    <footer>
        ...
    </footer>

</body>
```

This makes the purpose of each major part of the page clear.

---

## Common Mistakes

1. Using `<div>` for everything when a semantic element would be more appropriate.
2. Using headings only to make text look bigger.
3. Skipping heading levels without a structural reason.
4. Using `<nav>` for every small group of links.
5. Using `<article>` when the content is not meaningfully self-contained.
6. Using `<aside>` for content that is actually part of the main content.
7. Adding unnecessary ARIA attributes when native HTML already provides the required meaning.
8. Forgetting meaningful `alt` text on informative images.
9. Choosing elements based only on appearance instead of meaning.

---

## What I Practiced

In `index.html`, I practiced:

* Creating a semantic webpage structure.
* Using `<header>`.
* Creating navigation with `<nav>`.
* Organizing primary content with `<main>`.
* Grouping related content with `<section>`.
* Creating self-contained content with `<article>`.
* Adding supplementary content with `<aside>`.
* Creating page and article footers.
* Using `<address>` for contact information.
* Using `aria-label` for navigation.
* Adding a meta description.
* Organizing content with heading levels.
* Understanding the difference between semantic and generic elements.

---

## Practice Tasks

Try improving the page by:

1. Adding another `<article>` about HTML.
2. Adding a second navigation link group.
3. Adding an additional `<section>` for resources.
4. Adding an image with meaningful `alt` text.
5. Creating an `<aside>` containing related links.
6. Replacing any unnecessary generic containers with suitable semantic elements.
7. Checking the page using a browser accessibility inspection tool.

---

## Key Takeaways

* Semantic HTML describes the meaning and purpose of content.
* `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, and `<footer>` are important semantic elements.
* `<div>` and `<span>` are generic containers and should be used when no more appropriate semantic element exists.
* Good heading hierarchy improves document organization.
* Semantic HTML provides a stronger foundation for accessibility and maintainability.
* ARIA can provide additional accessibility information, but native semantic HTML should generally be preferred when available.
* Structure and meaning should come before visual styling.

## Folder Contents

```text
09-semantic-html/
├── index.html
└── README.md
```

## Learning Progress

This topic is part of my HTML learning journey. It builds on document structure, headings, links, images, lists, tables, and forms by focusing on how to organize a webpage using meaningful HTML elements.
