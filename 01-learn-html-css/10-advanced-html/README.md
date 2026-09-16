# Advanced HTML: Media, Metadata & Best Practices

This topic brings together several useful HTML features that help create more complete, accessible, and well-structured webpages.

It covers media, metadata, accessibility, embedded content, validation, and practical HTML best practices.

## What Are Advanced HTML Features?

After learning the basic HTML elements, webpages can be improved by adding features such as:

* Audio and video
* Metadata
* Embedded content
* Accessibility features
* HTML validation
* Better document structure
* Good coding practices

These features help make websites more useful, understandable, and maintainable.

---

## HTML Audio

The `<audio>` element is used to add audio content to a webpage.

Basic syntax:

```html
<audio controls>
    <source src="sample-audio.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```

### `controls`

The `controls` attribute displays controls such as:

* Play
* Pause
* Volume
* Progress

Without `controls`, the user may not have a visible way to interact with the audio.

### `<source>`

The `<source>` element specifies the media file and its type.

```html
<source src="sample-audio.mp3" type="audio/mpeg">
```

The `src` attribute specifies the file location.

The `type` attribute tells the browser what type of media is being used.

### Example

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

---

## HTML Video

The `<video>` element is used to display video content.

Example:

```html
<video controls width="500">
    <source src="sample-video.mp4" type="video/mp4">
    Your browser does not support the video element.
</video>
```

### Common Video Attributes

| Attribute  | Purpose                                   |
| ---------- | ----------------------------------------- |
| `controls` | Displays playback controls.               |
| `width`    | Sets the displayed width.                 |
| `height`   | Sets the displayed height.                |
| `autoplay` | Attempts to start playback automatically. |
| `muted`    | Starts the video without sound.           |
| `loop`     | Repeats the video.                        |
| `poster`   | Displays an image before the video plays. |

Not every attribute should be used automatically. For example, unexpected autoplay can create a poor user experience.

---

## Metadata

Metadata is information about a webpage that is not normally displayed as visible page content.

Metadata is usually placed inside `<head>`.

The page created for this topic uses:

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="...">
<meta name="author" content="Michael Kanyugo">
```

### Character Encoding

```html
<meta charset="UTF-8">
```

This tells the browser which character encoding should be used.

UTF-8 supports a wide range of characters and is commonly used for modern webpages.

### Viewport

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This helps webpages display correctly on different screen sizes, especially mobile devices.

### Description

```html
<meta
    name="description"
    content="A practical demonstration of advanced HTML features."
>
```

The description provides information about the page that can be useful to search engines and other tools.

### Author

```html
<meta name="author" content="Michael Kanyugo">
```

This identifies the author of the webpage.

---

## Embedding External Content

The `<iframe>` element can display another webpage or external resource inside the current webpage.

Example:

```html
<iframe
    src="https://www.example.com"
    title="Example website"
    width="600"
    height="300"
>
</iframe>
```

### Important Attributes

| Attribute | Purpose                                 |
| --------- | --------------------------------------- |
| `src`     | Specifies the embedded resource.        |
| `title`   | Describes the iframe for accessibility. |
| `width`   | Controls displayed width.               |
| `height`  | Controls displayed height.              |

### Important Note

Not every website allows itself to be embedded in an iframe. A website can use security policies that prevent this.

---

## The `<pre>` Element

The `<pre>` element displays preformatted text while preserving spaces and line breaks.

Example:

```html
<pre>
&lt;meta charset="UTF-8"&gt;
&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
</pre>
```

It is useful for:

* Code examples
* Preformatted text
* Text where spacing and line breaks are important

In the example above, HTML entities such as `&lt;` are used so the browser displays `<` as text instead of treating it as an HTML tag.

---

## Accessibility

Accessibility means designing webpages so that people with different abilities can use them effectively.

HTML provides several features that help with accessibility.

### Alternative Text

Meaningful images should have useful `alt` text.

```html
<img
    src="laptop.jpg"
    alt="Person using a laptop for web development"
>
```

The `alt` attribute provides a text alternative when an image cannot be seen.

It can also be used by screen readers.

### Decorative Images

If an image is purely decorative and provides no useful information, an empty `alt` attribute may be appropriate:

```html
<img src="decoration.png" alt="">
```

Do not write unnecessary or misleading alternative text.

---

## Accessible Navigation

The example page uses:

```html
<nav aria-label="Main navigation">
```

The `aria-label` gives the navigation a descriptive name.

ARIA attributes can provide additional information to assistive technologies.

However, native semantic HTML should generally be preferred when an appropriate HTML element already exists.

---

## Why Accessibility Matters

Good accessibility practices can improve the experience for:

* People using screen readers
* People with visual impairments
* People navigating with a keyboard
* People using different devices
* People with temporary or situational limitations

Accessibility should be considered while writing HTML, not added only at the end.

---

## HTML Validation

HTML validation is the process of checking HTML for errors and structural problems.

Validation can help identify things such as:

* Missing closing tags
* Invalid nesting
* Incorrect attributes
* Structural errors
* Invalid HTML syntax

A useful practice is to validate your HTML after completing a project.

### Why Validate?

Validation can help you:

* Find mistakes early.
* Improve code quality.
* Understand HTML rules better.
* Make webpages more reliable.

Validation does not automatically guarantee that a webpage is accessible, well-designed, or useful. It is one part of writing good HTML.

---

## HTML Best Practices

### 1. Use a Proper Document Structure

Start with a standard HTML document structure:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    ...
</head>

<body>
    ...
</body>

</html>
```

### 2. Use Semantic Elements

Prefer meaningful elements such as:

```html
<header>
<nav>
<main>
<section>
<article>
<aside>
<footer>
```

when they accurately describe the content.

### 3. Use Meaningful Headings

Headings should describe the content that follows them.

```html
<h1>Web Development</h1>

<h2>HTML</h2>

<h2>CSS</h2>
```

Do not choose heading levels only because of their visual appearance.

### 4. Write Descriptive Link Text

Prefer:

```html
<a href="https://developer.mozilla.org/">
    Read HTML documentation
</a>
```

rather than:

```html
<a href="https://developer.mozilla.org/">
    Click here
</a>
```

The first example gives more information about where the link leads.

### 5. Use Alternative Text for Meaningful Images

```html
<img
    src="laptop.jpg"
    alt="Laptop displaying HTML code"
>
```

The description should communicate the relevant meaning of the image.

### 6. Keep HTML Properly Nested

Correct:

```html
<p>
    This is <strong>important</strong>.
</p>
```

Incorrect nesting can create unexpected results.

### 7. Use CSS for Presentation

HTML should primarily provide structure and meaning.

CSS should handle most visual presentation.

For example, rather than using outdated presentation attributes, use CSS for styling:

```html
<p class="important-message">
    Important information
</p>
```

and style it with CSS.

### 8. Use Labels with Form Controls

Form controls should have meaningful labels.

```html
<label for="email">Email:</label>
<input type="email" id="email" name="email">
```

### 9. Keep Code Readable

Use:

* Consistent indentation
* Meaningful names
* Clear structure
* Helpful comments where necessary

Readable code is easier to maintain and debug.

### 10. Validate Your HTML

Check your HTML for errors after completing a webpage or project.

---

## SEO Basics

SEO stands for **Search Engine Optimization**.

HTML can provide useful information to search engines through:

* Meaningful page titles
* Descriptive meta descriptions
* Semantic structure
* Proper heading hierarchy
* Descriptive links
* Useful image `alt` text

For example:

```html
<title>HTML Forms Tutorial</title>

<meta
    name="description"
    content="Learn how to create forms using HTML."
>
```

Good HTML can support SEO, but SEO depends on many factors beyond HTML alone.

---

## Common Mistakes

1. Using outdated HTML presentation techniques instead of CSS.
2. Adding media without considering accessibility.
3. Using meaningless `alt` text.
4. Forgetting the `title` attribute on important iframes.
5. Using iframes without considering security or usability.
6. Using autoplay unnecessarily.
7. Writing very long or unclear HTML structures.
8. Using generic `<div>` elements when a semantic element is more appropriate.
9. Ignoring HTML validation errors.
10. Treating metadata as visible webpage content.

---

## What I Practiced

In `index.html`, I practiced:

* Adding audio using `<audio>`.
* Adding video using `<video>`.
* Using `<source>` for media files.
* Adding metadata with `<meta>`.
* Using `<pre>` to display code examples.
* Embedding external content with `<iframe>`.
* Improving accessibility with `alt` text.
* Using `aria-label` for navigation.
* Understanding HTML validation.
* Applying HTML best practices.
* Reviewing basic SEO-related HTML features.

---

## Practice Tasks

Try improving the page by:

1. Adding a real local audio file.
2. Adding a real local video file.
3. Adding a video poster image.
4. Adding another useful meta tag.
5. Adding more accessible content.
6. Testing the page using an HTML validator.
7. Checking the page using browser accessibility tools.
8. Reviewing the entire `Learn-html` repository and identifying places where your HTML could be improved.

---

## Final HTML Checklist

Before considering an HTML page complete, check:

```text
[ ] DOCTYPE is included
[ ] html element has a lang attribute
[ ] head contains important metadata
[ ] title is descriptive
[ ] headings are properly organized
[ ] semantic elements are used where appropriate
[ ] images have appropriate alt text
[ ] links have descriptive text
[ ] forms have proper labels
[ ] HTML is properly nested
[ ] code is readable and indented
[ ] outdated presentation attributes are avoided
[ ] HTML has been validated
```

## Key Takeaways

* `<audio>` and `<video>` allow media to be added directly to webpages.
* `<meta>` provides information about a webpage.
* `<iframe>` can embed external content.
* Accessibility should be considered when writing HTML.
* `alt` text provides alternatives for meaningful images.
* ARIA can provide additional accessibility information when needed.
* Validation helps identify HTML errors.
* Semantic HTML improves structure and meaning.
* Good HTML should be readable, meaningful, maintainable, and accessible.
* HTML provides structure; CSS handles presentation and JavaScript can add behavior.

## Folder Contents

```text
10-advanced-html/
├── index.html
└── README.md
```

## Learning Progress

This is the final planned topic in my HTML learning folder. It brings together media, metadata, accessibility, embedded content, validation, and practical HTML best practices learned throughout this repository.

The next stage is to apply these HTML concepts in projects and continue learning other web technologies.