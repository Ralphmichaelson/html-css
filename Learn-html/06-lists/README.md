# HTML Lists

## Introduction

Lists are used to organize related information into groups.

HTML provides different types of lists depending on how the information should be presented.

The three main list types are:

1. **Unordered lists**
2. **Ordered lists**
3. **Description lists**

In this topic, I practiced unordered lists, ordered lists, nested lists, and using lists for navigation.

---

## 1. Unordered Lists

An unordered list displays items without implying a particular sequence.

It normally displays items using bullet points.

The `<ul>` element creates an unordered list.

Each item inside the list is created using the `<li>` element.

### Syntax

```html id="3n1f4a"
<ul>
    <li>Item One</li>
    <li>Item Two</li>
    <li>Item Three</li>
</ul>
```

### Example

```html id="5vqp3c"
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

The browser will display the items as a bulleted list.

---

## 2. Ordered Lists

An ordered list is used when the order or sequence of the items is important.

The `<ol>` element creates an ordered list.

Each item is still represented using `<li>`.

### Syntax

```html id="hjxk5a"
<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>
```

The browser normally displays the items using numbers.

### Example

```html id="6px6w0"
<ol>
    <li>Open VS Code</li>
    <li>Create an HTML file</li>
    <li>Write the HTML code</li>
    <li>Open the page in a browser</li>
</ol>
```

The result is approximately:

```text
1. Open VS Code
2. Create an HTML file
3. Write the HTML code
4. Open the page in a browser
```

---

## 3. The `<li>` Element

The `<li>` element represents an individual list item.

`li` stands for **List Item**.

It is normally placed inside either:

```html id="h5d5gg"
<ul>
```

or:

```html id="8kn6t8"
<ol>
```

Example:

```html id="8a6z6m"
<ul>
    <li>HTML</li>
    <li>CSS</li>
</ul>
```

Here:

* `<ul>` creates the list.
* Each `<li>` represents an item in the list.

### Important

An `<li>` should normally be used as a child of a list container such as `<ul>` or `<ol>`.

---

## 4. Nested Lists

A list can contain another list.

This is called a **nested list**.

Nested lists are useful when information has different levels or categories.

### Example

```html id="j5w9is"
<ul>
    <li>
        Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>
    </li>
</ul>
```

The structure is:

```text
Frontend
    ├── HTML
    ├── CSS
    └── JavaScript
```

The inner `<ul>` is nested inside the `<li>` belonging to `Frontend`.

---

## 5. Ordered Lists with a Starting Number

The `<ol>` element can use the `start` attribute to specify the number at which the list should begin.

### Example

```html id="rcr5zj"
<ol start="5">
    <li>Fifth item</li>
    <li>Sixth item</li>
    <li>Seventh item</li>
</ol>
```

The browser displays:

```text
5. Fifth item
6. Sixth item
7. Seventh item
```

The `start` attribute is useful when the numbering needs to continue from an earlier list.

---

## 6. Lists and Navigation

Lists can be used together with the `<nav>` element to create structured navigation.

Example:

```html id="6z7p1c"
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

The structure is:

```text
<nav>
   └── <ul>
       ├── <li>
       │    └── <a>
       ├── <li>
       │    └── <a>
       └── <li>
            └── <a>
```

CSS can later be used to change this from a vertical list into a horizontal navigation menu.

---

## 7. Choosing Between `<ul>` and `<ol>`

The choice depends on whether the order matters.

### Use `<ul>` when:

The items do not need to follow a particular order.

Example:

```html id="kr8j7r"
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

The order of the technologies isn't necessarily a sequence.

### Use `<ol>` when:

The order or sequence is important.

Example:

```html id="7xq8go"
<ol>
    <li>Turn on the computer</li>
    <li>Open VS Code</li>
    <li>Open the project</li>
    <li>Start coding</li>
</ol>
```

Changing the order would change the meaning of the instructions.

---

## 8. Unordered vs Ordered Lists

| Element | Purpose              | Default appearance     |
| ------- | -------------------- | ---------------------- |
| `<ul>`  | Unordered list       | Bullet points          |
| `<ol>`  | Ordered list         | Numbers                |
| `<li>`  | Individual list item | Depends on parent list |

---

## 9. Understanding the `index.html` Example

The practical example demonstrates several ways lists can be used.

### Unordered list

```html id="5gyg9g"
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
    <li>C++</li>
</ul>
```

This demonstrates a simple list of technologies.

### Ordered list

```html id="6d6y5j"
<ol>
    <li>Open VS Code</li>
    <li>Create an HTML file</li>
    <li>Write the HTML structure</li>
    <li>Open the page in a browser</li>
</ol>
```

This demonstrates a sequence of steps.

### Nested list

```html id="b7g75x"
<ul>
    <li>
        Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>
    </li>
</ul>
```

This demonstrates categories and subcategories.

### Starting number

```html id="0bty4w"
<ol start="5">
    <li>Fifth item</li>
    <li>Sixth item</li>
    <li>Seventh item</li>
</ol>
```

This demonstrates the `start` attribute.

### Navigation list

```html id="7ynvcu"
<nav>
    <ul>
        <li>
            <a href="../01-html-introduction/index.html">
                HTML Introduction
            </a>
        </li>

        <li>
            <a href="../04-links-and-navigation/index.html">
                Links and Navigation
            </a>
        </li>
    </ul>
</nav>
```

This demonstrates how lists and links can be combined to create structured navigation.

---

## 10. Common Mistakes

### Mistake 1: Forgetting the `<li>` elements

Incorrect:

```html id="4h7m4e"
<ul>
    HTML
    CSS
    JavaScript
</ul>
```

Better:

```html id="9e1bzi"
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

---

### Mistake 2: Using `<ol>` when order doesn't matter

If you're simply listing technologies, an unordered list is usually more appropriate:

```html id="1jv4vo"
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

Use `<ol>` when the sequence has meaning.

---

### Mistake 3: Incorrect nesting

When creating nested lists, the inner list should normally be placed inside the relevant `<li>`.

Better:

```html id="vlp9cl"
<ul>
    <li>
        Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
        </ul>
    </li>
</ul>
```

---

### Mistake 4: Forgetting that lists can contain other elements

A list item isn't limited to plain text.

For example:

```html id="wz2p1w"
<ul>
    <li>
        <a href="about.html">About</a>
    </li>
</ul>
```

This allows lists to be combined with links and other HTML elements.

---

## What I Practiced

In `index.html`, I practiced:

* Creating unordered lists using `<ul>`.
* Creating ordered lists using `<ol>`.
* Creating list items using `<li>`.
* Creating nested lists.
* Using the `start` attribute with ordered lists.
* Combining lists with links.
* Creating a simple navigation structure using `<nav>`.
* Understanding when to use ordered and unordered lists.

## Key Takeaways

* `<ul>` creates an unordered list.
* `<ol>` creates an ordered list.
* `<li>` represents an individual list item.
* Lists can be nested to create multiple levels of information.
* The `start` attribute can change where an ordered list begins.
* Lists can be combined with links to create navigation menus.
* Use `<ul>` when the order does not matter.
* Use `<ol>` when the sequence is meaningful.

## Folder Contents

```text id="my3c6s"
06-lists/
├── index.html
└── README.md
```
