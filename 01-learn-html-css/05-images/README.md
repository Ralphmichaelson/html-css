# HTML Images

## Introduction

Images are an important part of many webpages. They can be used to provide information, illustrate ideas, make content more engaging, and improve the visual appearance of a webpage.

In HTML, images are added using the `<img>` element.

Unlike elements such as `<p>` and `<h1>`, the `<img>` element does not have a closing tag because it is a **void element**.

---

## 1. The `<img>` Element

The basic syntax for adding an image is:

```html
<img src="image.jpg" alt="Description of the image">
```

### Explanation

* `<img>` — tells the browser to display an image.
* `src` — specifies the location of the image.
* `alt` — provides alternative text describing the image.

Example:

```html
<img
    src="photo.jpg"
    alt="A person working on a laptop"
>
```

---

## 2. The `src` Attribute

The `src` attribute specifies where the image comes from.

`src` stands for **source**.

### Example

```html
<img
    src="https://example.com/image.jpg"
    alt="Example image"
>
```

The browser uses the URL in `src` to find and display the image.

An image source can be:

* A URL to an image on the internet.
* A path to an image stored in the project.

---

## 3. Using a Local Image

Images can also be stored inside your project.

For example:

```text
05-images/
├── images/
│   └── laptop.jpg
├── index.html
└── README.md
```

The image can then be displayed using:

```html
<img
    src="images/laptop.jpg"
    alt="A laptop"
>
```

The path tells the browser where to find the image relative to `index.html`.

---

## 4. The `alt` Attribute

The `alt` attribute provides alternative text for an image.

Example:

```html
<img
    src="laptop.jpg"
    alt="A laptop displaying computer code"
>
```

The alternative text is useful when:

* The image cannot be loaded.
* A user is using a screen reader.
* The image needs to be understood from its description.

### Good `alt` text

```html
<img
    src="car.jpg"
    alt="A black Toyota parked outside a building"
>
```

### Poor `alt` text

```html
<img
    src="car.jpg"
    alt="image"
>
```

The second example provides very little useful information.

### Important

The `alt` text should describe the **purpose or meaningful content** of the image.

---

## 5. Image Dimensions

The `width` attribute can be used to control the displayed width of an image.

Example:

```html
<img
    src="laptop.jpg"
    alt="A laptop displaying computer code"
    width="500"
>
```

This displays the image at a width of 500 pixels.

You can also specify a height:

```html
<img
    src="laptop.jpg"
    alt="A laptop displaying computer code"
    width="500"
    height="300"
>
```

However, setting width and height without considering the original image proportions can distort the image.

CSS is normally used for more flexible image sizing and responsive layouts.

---

## 6. Making an Image a Link

An image can be placed inside an `<a>` element.

This makes the image clickable.

Example:

```html
<a href="https://github.com/">
    <img
        src="github-logo.png"
        alt="GitHub logo"
        width="100"
    >
</a>
```

The structure is:

```text
<a>
   └── <img>
```

The anchor element provides the destination, while the image becomes the clickable content.

---

## 7. Opening an Image Link in a New Tab

An image link can also use `target="_blank"`:

```html
<a
    href="https://github.com/"
    target="_blank"
    rel="noopener noreferrer"
>
    <img
        src="github-logo.png"
        alt="GitHub logo"
        width="100"
    >
</a>
```

### Attributes

* `target="_blank"` — requests that the destination open in a new tab or browsing context.
* `rel="noopener noreferrer"` — provides additional security and privacy protection for the new browsing context.

---

## 8. Images and Accessibility

Images should be considered when designing accessible webpages.

For meaningful images, provide useful alternative text:

```html
<img
    src="computer.jpg"
    alt="A laptop displaying HTML code"
>
```

A screen reader can use the `alt` text to communicate the image's meaning to the user.

For purely decorative images, an empty `alt` attribute can be appropriate:

```html
<img
    src="decoration.png"
    alt=""
>
```

This tells assistive technologies that the image does not add meaningful information.

---

## 9. Understanding the `index.html` Example

The practical page demonstrates several image concepts.

### First image

```html
<img
    src="https://images.unsplash.com/photo-1497366754035-f200968a6e72"
    alt="A modern workspace with a desk and computer"
    width="600"
>
```

This demonstrates:

* The `<img>` element.
* An external image source.
* The `alt` attribute.
* The `width` attribute.

### Another image

```html
<img
    src="https://images.unsplash.com/photo-1498050108023-c5249f4df085"
    alt="A laptop displaying computer code"
    width="500"
>
```

This demonstrates how multiple images can be placed on the same webpage.

### Clickable image

```html
<a href="https://github.com/" target="_blank" rel="noopener noreferrer">
    <img
        src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png"
        alt="GitHub logo"
        width="100"
    >
</a>
```

Here, the `<img>` element is nested inside the `<a>` element, making the image clickable.

---

## 10. Common Image Syntax

| Purpose                     | Syntax                                                             |
| --------------------------- | ------------------------------------------------------------------ |
| Basic image                 | `<img src="image.jpg" alt="Description">`                          |
| Image with width            | `<img src="image.jpg" alt="Description" width="500">`              |
| Image with width and height | `<img src="image.jpg" alt="Description" width="500" height="300">` |
| Local image                 | `<img src="images/photo.jpg" alt="Description">`                   |
| Image link                  | `<a href="URL"><img src="image.jpg" alt="Description"></a>`        |

---

## 11. Common Mistakes

### Mistake 1: Forgetting `alt`

```html
<img src="laptop.jpg">
```

A meaningful image should normally have alternative text.

Better:

```html
<img
    src="laptop.jpg"
    alt="Laptop displaying computer code"
>
```

---

### Mistake 2: Using the wrong image path

If your image is stored here:

```text
images/
└── laptop.jpg
```

Your HTML needs to correctly reference that location:

```html
<img src="images/laptop.jpg" alt="Laptop">
```

Using an incorrect path can result in a broken image.

---

### Mistake 3: Forgetting that `<img>` is a void element

Do not write:

```html
<img src="photo.jpg" alt="Photo"></img>
```

The normal HTML syntax is:

```html
<img src="photo.jpg" alt="Photo">
```

---

### Mistake 4: Stretching an image

Specifying unrelated width and height values can distort the image.

For example:

```html
<img
    src="photo.jpg"
    alt="Photo"
    width="800"
    height="200"
>
```

The image may appear stretched if its original proportions do not match those dimensions.

---

## What I Practiced

In `index.html`, I practiced:

* Adding images using the `<img>` element.
* Using the `src` attribute.
* Using the `alt` attribute.
* Setting image width.
* Using images from external URLs.
* Placing an image inside an anchor element.
* Creating a clickable image.
* Opening an image link in a new tab.
* Understanding the importance of alternative text.
* Using semantic sections to organize image-related content.

## Key Takeaways

* Images are added using the `<img>` element.
* The `src` attribute specifies the image source.
* The `alt` attribute provides alternative text.
* `<img>` is a void element and does not need a closing tag.
* Images can be stored locally or loaded from external URLs.
* Images can be placed inside `<a>` elements to make them clickable.
* `width` and `height` can control displayed dimensions.
* Good `alt` text improves accessibility.
* CSS will provide more control over image sizing and responsive design later.

## Folder Contents

```text
05-images/
├── index.html
└── README.md
```
