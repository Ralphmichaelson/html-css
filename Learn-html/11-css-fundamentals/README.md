# CSS Fundamentals

This topic introduces the fundamental concepts of **CSS (Cascading Style Sheets)** and how CSS is used to style and control the appearance of HTML webpages.

The `index.html` file demonstrates the main CSS concepts covered in this topic.

## What Is CSS?

CSS stands for **Cascading Style Sheets**.

CSS is used to control the presentation of HTML elements, including:

* Colors
* Fonts
* Text
* Spacing
* Borders
* Backgrounds
* Layout
* Element positioning
* Responsive behavior

HTML provides the **structure** of a webpage, while CSS controls its **appearance and presentation**.

For example:

```html
<p class="highlight">Hello World</p>
```

CSS can style the paragraph:

```css
.highlight {
    color: darkblue;
    font-weight: bold;
}
```

---

# CSS Syntax

A CSS rule normally consists of a **selector**, a **property**, and a **value**.

```css
selector {
    property: value;
}
```

Example:

```css
p {
    color: blue;
    font-size: 18px;
}
```

### Parts of the Rule

```text
p
│
└── Selector

color: blue;
│      │
│      └── Value
│
└── Property
```

A CSS declaration ends with a semicolon:

```css
color: blue;
```

Multiple declarations can be placed inside the same rule:

```css
p {
    color: blue;
    font-size: 18px;
    line-height: 1.6;
}
```

---

# Ways to Add CSS

There are three main ways to apply CSS to HTML.

## 1. Inline CSS

CSS can be placed directly inside an HTML element using the `style` attribute.

```html
<p style="color: blue;">
    Hello World
</p>
```

### Advantages

* Quick for testing.
* Applies directly to one element.

### Disadvantages

* Difficult to maintain.
* Repeats styles.
* Makes HTML harder to read.

Inline CSS should generally not be the main styling method for larger projects.

---

## 2. Internal CSS

CSS can be placed inside a `<style>` element in the `<head>`.

```html
<head>

    <style>

        p {
            color: blue;
        }

    </style>

</head>
```

The `index.html` for this topic uses internal CSS.

This is useful for:

* Small webpages
* Learning
* Demonstrations
* Single-page examples

---

## 3. External CSS

CSS can be stored in a separate `.css` file.

Example:

```text
project/
├── index.html
└── style.css
```

HTML:

```html
<link rel="stylesheet" href="style.css">
```

CSS:

```css
body {
    font-family: Arial, sans-serif;
}
```

External CSS is generally preferred for larger websites because the same stylesheet can be reused across multiple HTML pages.

---

# CSS Selectors

Selectors determine which HTML elements receive a style.

## Element Selector

Targets HTML elements directly.

```css
p {
    color: blue;
}
```

This applies to all `<p>` elements.

Another example:

```css
h1 {
    font-size: 40px;
}
```

---

## Class Selector

A class selector begins with a dot `.`.

HTML:

```html
<p class="highlight">
    Important text
</p>
```

CSS:

```css
.highlight {
    color: darkblue;
    font-weight: bold;
}
```

A class can be reused on multiple elements.

---

## ID Selector

An ID selector begins with `#`.

HTML:

```html
<h1 id="main-title">
    CSS Fundamentals
</h1>
```

CSS:

```css
#main-title {
    margin-bottom: 10px;
}
```

An ID is intended to identify a particular element uniquely within a page.

---

## Selector Comparison

| Selector | Syntax    | Example       |
| -------- | --------- | ------------- |
| Element  | `element` | `p`           |
| Class    | `.class`  | `.highlight`  |
| ID       | `#id`     | `#main-title` |

---

# Grouping Selectors

Multiple selectors can share the same CSS rule.

```css
h1,
h2,
h3 {
    font-family: Arial, sans-serif;
}
```

This avoids repeating the same declarations.

---

# Descendant Selectors

A selector can target an element inside another element.

```css
nav a {
    color: white;
}
```

This targets `<a>` elements inside `<nav>`.

HTML:

```html
<nav>

    <a href="#">Home</a>
    <a href="#">About</a>

</nav>
```

---

# Pseudo-Classes

Pseudo-classes style an element based on a particular state.

A common example is `:hover`.

```css
a:hover {
    text-decoration: underline;
}
```

This applies when the user points the mouse over the link.

Other common pseudo-classes include:

```css
:focus
:active
:visited
:first-child
:last-child
```

---

# Colors

CSS provides several ways to specify colors.

## Named Colors

```css
p {
    color: blue;
}
```

## HEX

```css
p {
    color: #0000ff;
}
```

## RGB

```css
p {
    color: rgb(0, 0, 255);
}
```

## RGBA

```css
p {
    color: rgba(0, 0, 255, 0.5);
}
```

The last value represents transparency.

## HSL

```css
p {
    color: hsl(240, 100%, 50%);
}
```

---

# Backgrounds

CSS can change the background of an element.

```css
body {
    background-color: #f4f4f4;
}
```

You can also use background images:

```css
section {
    background-image: url("background.jpg");
}
```

Other useful background properties include:

```css
background-size
background-position
background-repeat
```

---

# Text Styling

CSS provides many properties for controlling text.

## `color`

```css
p {
    color: #333;
}
```

## `font-size`

```css
p {
    font-size: 18px;
}
```

## `font-family`

```css
p {
    font-family: Arial, sans-serif;
}
```

## `font-weight`

```css
p {
    font-weight: bold;
}
```

## `text-align`

```css
p {
    text-align: center;
}
```

## `text-decoration`

```css
a {
    text-decoration: none;
}
```

## `line-height`

```css
p {
    line-height: 1.6;
}
```

---

# Fonts

The `font-family` property determines which font is used.

```css
body {
    font-family: Arial, sans-serif;
}
```

A fallback font can be specified after the primary font.

```css
body {
    font-family: Arial, sans-serif;
}
```

If Arial is unavailable, the browser can use another sans-serif font.

---

# Borders

Borders are placed around elements.

```css
section {
    border: 1px solid #ddd;
}
```

A border can have:

```text
border-width
border-style
border-color
```

Example:

```css
box {
    border-width: 2px;
    border-style: solid;
    border-color: black;
}
```

A shorter form is:

```css
box {
    border: 2px solid black;
}
```

---

# Border Radius

The `border-radius` property creates rounded corners.

```css
section {
    border-radius: 8px;
}
```

---

# Width and Height

CSS can control the size of elements.

```css
.box {
    width: 300px;
    height: 150px;
}
```

Other units can also be used.

```css
.box {
    width: 50%;
}
```

---

# The CSS Box Model

Every HTML element can be understood as a box.

The box model consists of:

```text
┌───────────────────────────────┐
│            Margin             │
│   ┌───────────────────────┐   │
│   │        Border         │   │
│   │   ┌───────────────┐   │   │
│   │   │    Padding    │   │   │
│   │   │  ┌─────────┐  │   │   │
│   │   │  │ Content │  │   │   │
│   │   │  └─────────┘  │   │   │
│   │   └───────────────┘   │   │
│   └───────────────────────┘   │
└───────────────────────────────┘
```

The four main parts are:

1. Content
2. Padding
3. Border
4. Margin

---

# Padding

Padding creates space **inside** an element, between the content and the border.

```css
.box {
    padding: 20px;
}
```

---

# Margin

Margin creates space **outside** an element.

```css
.box {
    margin: 20px;
}
```

---

# Width, Padding, and `box-sizing`

By default, padding and borders can affect the total size of an element.

A common approach is:

```css
* {
    box-sizing: border-box;
}
```

With `border-box`, the declared width and height include the element's padding and border.

---

# CSS Display Property

The `display` property determines how an element participates in layout.

Common values include:

```css
display: block;
display: inline;
display: inline-block;
display: none;
```

## Block

Block elements normally take up the available width and begin on a new line.

```css
div {
    display: block;
}
```

## Inline

Inline elements normally remain within the same line.

```css
span {
    display: inline;
}
```

## Inline-Block

Allows an element to remain inline while accepting width and height.

```css
span {
    display: inline-block;
}
```

## None

Removes the element from the normal page layout.

```css
.hidden {
    display: none;
}
```

---

# CSS Units

CSS supports different units.

## Pixels

```css
font-size: 18px;
```

`px` represents pixels.

## Percentage

```css
width: 50%;
```

Percentage values are relative to another dimension, usually that of a containing element.

## `em`

```css
font-size: 1.2em;
```

`em` is relative to the font size of the relevant element or inherited context.

## `rem`

```css
font-size: 1.2rem;
```

`rem` is relative to the root element's font size.

## Viewport Units

```css
width: 50vw;
height: 50vh;
```

* `vw` = viewport width
* `vh` = viewport height

---

# Styling Lists

CSS can change the appearance of lists.

```css
ul {
    list-style-type: square;
}
```

Common list styles include:

```css
disc
circle
square
decimal
lower-alpha
upper-alpha
```

---

# Styling Links

Links can be styled using CSS.

```css
a {
    color: blue;
    text-decoration: none;
}
```

Different states can also be styled:

```css
a:hover {
    text-decoration: underline;
}
```

---

# Styling Forms

CSS can improve the appearance and usability of form controls.

Example:

```css
input,
textarea,
select {
    width: 100%;
    padding: 10px;
    border: 1px solid #aaa;
    border-radius: 5px;
}
```

Labels can also be styled:

```css
label {
    display: block;
    font-weight: bold;
}
```

Buttons:

```css
button {
    padding: 10px 18px;
    border: none;
    cursor: pointer;
}
```

---

# CSS Positioning

The `position` property controls how an element is positioned.

Common values are:

```css
position: static;
position: relative;
position: absolute;
position: fixed;
position: sticky;
```

## Relative

```css
.container {
    position: relative;
}
```

An element remains in the normal document flow but can become a positioning reference for absolutely positioned children.

## Absolute

```css
.box {
    position: absolute;
    top: 20px;
    right: 20px;
}
```

An absolutely positioned element is positioned relative to its nearest positioned ancestor.

## Fixed

```css
button {
    position: fixed;
    bottom: 20px;
    right: 20px;
}
```

The element remains fixed relative to the viewport while the page scrolls.

## Sticky

```css
header {
    position: sticky;
    top: 0;
}
```

The element behaves normally until a specified scrolling position is reached.

---

# CSS Cascade

The word **Cascading** in CSS refers to the process of determining which styles apply when several rules affect the same element.

For example:

```css
p {
    color: blue;
}

p {
    color: red;
}
```

Both rules target the paragraph. The later rule can take precedence when the selectors have equivalent specificity.

---

# Specificity

Specificity determines which selector has greater priority when multiple rules target the same element.

A simplified order is:

```text
Element selector
      ↓
Class / attribute / pseudo-class
      ↓
ID selector
      ↓
Inline style
```

Example:

```css
p {
    color: blue;
}

.highlight {
    color: green;
}

#special {
    color: red;
}
```

If one paragraph has:

```html
<p id="special" class="highlight">
    Example
</p>
```

the ID selector generally has greater specificity than the class and element selectors.

Avoid using `!important` as a solution to ordinary specificity problems. It can make styles harder to maintain.

---

# Inheritance

Some CSS properties can be inherited from a parent element by its children.

Example:

```css
body {
    color: #222;
    font-family: Arial, sans-serif;
}
```

Many text-related properties can then be inherited by elements inside the body.

Not every CSS property is inherited.

---

# CSS Comments

Comments explain CSS code but are not displayed as webpage content.

Syntax:

```css
/* This is a CSS comment */
```

Comments can be useful for organizing larger stylesheets.

---

# Responsive Design

Responsive design means creating webpages that work well across different screen sizes.

A simple media query looks like this:

```css
@media (max-width: 600px) {

    nav a {
        display: block;
    }

}
```

The styles inside the media query are applied when the viewport meets the specified condition.

Responsive design commonly involves:

* Flexible widths
* Relative units
* Media queries
* Responsive images
* Flexible layouts

---

# CSS Properties Practiced

The `index.html` file demonstrates properties such as:

| Property           | Purpose                         |
| ------------------ | ------------------------------- |
| `color`            | Changes text color              |
| `background-color` | Sets background color           |
| `font-family`      | Changes the font                |
| `font-size`        | Changes text size               |
| `font-weight`      | Controls text thickness         |
| `text-align`       | Aligns text                     |
| `line-height`      | Controls line spacing           |
| `text-decoration`  | Adds or removes text decoration |
| `width`            | Sets width                      |
| `height`           | Sets height                     |
| `margin`           | Creates outside spacing         |
| `padding`          | Creates inside spacing          |
| `border`           | Creates a border                |
| `border-radius`    | Rounds corners                  |
| `display`          | Controls display behavior       |
| `position`         | Controls positioning            |
| `top`              | Controls top offset             |
| `right`            | Controls right offset           |
| `cursor`           | Controls the mouse cursor       |
| `list-style-type`  | Changes list markers            |

---

# Common CSS Mistakes

1. Forgetting the semicolon after a declaration.
2. Forgetting the closing `}` of a CSS rule.
3. Using `#` when a class selector requires `.`.
4. Confusing `margin` with `padding`.
5. Using IDs unnecessarily for reusable styling.
6. Using inline CSS throughout a large project.
7. Forgetting that CSS selectors are case-sensitive in relevant contexts.
8. Overusing `!important`.
9. Writing overly complicated selectors.
10. Ignoring responsive behavior.
11. Using CSS to fix poor HTML structure.
12. Changing visual appearance without considering accessibility and usability.

---

# What I Practiced

In `index.html`, I practiced:

* Writing CSS syntax.
* Using element selectors.
* Using class selectors.
* Using ID selectors.
* Styling text.
* Styling backgrounds.
* Adding borders.
* Using margin and padding.
* Understanding the box model.
* Using width and height.
* Using the `display` property.
* Styling lists.
* Styling links.
* Styling form controls.
* Using pseudo-classes such as `:hover`.
* Using CSS positioning.
* Using CSS units.
* Understanding the cascade.
* Understanding specificity.
* Understanding inheritance.
* Writing CSS comments.
* Using media queries for basic responsive behavior.

---

# Practice Tasks

Try improving the page by:

1. Moving the internal CSS into a separate `style.css` file.
2. Adding more colors and text styles.
3. Creating additional class selectors.
4. Adding a different hover effect to the navigation.
5. Creating a styled card component.
6. Experimenting with `margin` and `padding`.
7. Changing the box model example.
8. Practicing `relative`, `absolute`, `fixed`, and `sticky` positioning.
9. Adding another media query for smaller screens.
10. Experimenting with `px`, `%`, `em`, `rem`, `vh`, and `vw`.

---

# HTML vs CSS

HTML and CSS have different responsibilities.

| HTML                       | CSS                               |
| -------------------------- | --------------------------------- |
| Provides structure         | Controls presentation             |
| Creates headings           | Styles headings                   |
| Creates paragraphs         | Styles paragraphs                 |
| Creates forms              | Styles forms                      |
| Creates links              | Styles links                      |
| Creates images             | Controls image appearance         |
| Defines semantic structure | Controls layout and visual design |

A simple way to remember:

```text
HTML = Structure
CSS  = Presentation
```

---

# Key Takeaways

* CSS stands for **Cascading Style Sheets**.
* CSS controls the presentation of HTML webpages.
* CSS rules contain selectors and declarations.
* Classes use `.` and IDs use `#`.
* CSS can be written inline, internally, or externally.
* External stylesheets are generally the most maintainable option for larger projects.
* The box model consists of content, padding, border, and margin.
* `display` controls how elements participate in layout.
* `position` controls element positioning.
* CSS has different units for sizing and spacing.
* The cascade and specificity determine which styles are applied.
* Some CSS properties are inherited from parent elements.
* Pseudo-classes allow styles to respond to element states.
* Media queries help create responsive webpages.
* Good CSS should be readable, reusable, maintainable, and responsive.

---

# Folder Contents

```text
11-css-fundamentals/
├── index.html
└── README.md
```

## Learning Progress

This topic marks the beginning of my CSS learning after completing the HTML fundamentals in this repository.

It provides the foundation needed before moving into more advanced CSS concepts such as Flexbox, Grid, animations, transitions, and responsive layouts.
