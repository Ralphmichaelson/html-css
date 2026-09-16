# HTML Forms

This topic focuses on learning how to create forms in HTML. Forms allow users to enter, select, and submit information on a webpage.

## What Are HTML Forms?

An HTML form is a section of a webpage that allows users to provide information.

Forms are commonly used for:

* Login pages
* Registration pages
* Contact forms
* Search boxes
* Surveys
* Feedback forms
* Online applications
* Checkout pages

The main element used to create a form is the `<form>` element.

## Basic Form Syntax

```html
<form>

    <!-- Form controls go here -->

</form>
```

The `<form>` element acts as a container for the different input controls.

## The `<label>` Element

The `<label>` element provides a description for a form control.

```html
<label for="name">Full Name:</label>
<input type="text" id="name">
```

The `for` attribute connects the label to an input.

The value of `for` should match the `id` of the input.

```text
for="name"
      ↓
id="name"
```

This connection is useful for accessibility and also allows users to click the label to focus the associated input.

## The `<input>` Element

The `<input>` element is used to create different types of form controls.

Unlike many HTML elements, `<input>` does not require a closing tag.

Example:

```html
<input type="text">
```

The `type` attribute determines what kind of input control is displayed.

## Common Input Types

### 1. Text Input

Used for entering ordinary text.

```html
<input type="text" id="name" name="name">
```

Example uses:

* Names
* Usernames
* Short text

### 2. Email Input

Used for entering an email address.

```html
<input type="email" id="email" name="email">
```

Browsers can perform basic validation to check whether the entered value looks like an email address.

### 3. Password Input

Used for entering passwords.

```html
<input type="password" id="password" name="password">
```

The characters entered are hidden from normal view.

### 4. Number Input

Used for numerical values.

```html
<input type="number" id="age" name="age">
```

It can be useful for values such as:

* Age
* Quantity
* Scores
* Other numerical information

### 5. Date Input

Allows the user to select a date.

```html
<input type="date" id="date" name="date">
```

## Radio Buttons

Radio buttons are useful when the user should select **one option from a group**.

Example:

```html
<input type="radio" id="html" name="language" value="HTML">
<label for="html">HTML</label>

<input type="radio" id="css" name="language" value="CSS">
<label for="css">CSS</label>

<input type="radio" id="javascript" name="language" value="JavaScript">
<label for="javascript">JavaScript</label>
```

The important part is that the radio buttons have the same `name`:

```html
name="language"
```

This groups them together so that the user can select one option.

### Radio Button Structure

```text
Language
   │
   ├── ○ HTML
   ├── ○ CSS
   └── ○ JavaScript
```

## Checkboxes

Checkboxes allow users to select **multiple options**.

Example:

```html
<input type="checkbox" id="frontend" name="interest" value="Frontend">
<label for="frontend">Frontend</label>

<input type="checkbox" id="backend" name="interest" value="Backend">
<label for="backend">Backend</label>

<input type="checkbox" id="database" name="interest" value="Database">
<label for="database">Database</label>
```

Unlike radio buttons, multiple checkboxes can be selected at the same time.

### Checkbox Structure

```text
Technologies
   │
   ├── ☑ Frontend
   ├── ☑ Backend
   └── ☐ Database
```

## Radio Buttons vs Checkboxes

| Radio Buttons                     | Checkboxes                             |
| --------------------------------- | -------------------------------------- |
| Usually used to choose one option | Can be used to choose multiple options |
| Options share the same `name`     | Options can have the same `name`       |
| Uses `type="radio"`               | Uses `type="checkbox"`                 |
| Example: choose one language      | Example: choose several interests      |

## The `<select>` Element

The `<select>` element creates a dropdown list.

```html
<select id="country" name="country">

    <option value="kenya">Kenya</option>
    <option value="uganda">Uganda</option>
    <option value="tanzania">Tanzania</option>

</select>
```

The `<select>` element contains `<option>` elements.

### `<option>`

Each `<option>` represents one choice in the dropdown.

```html
<option value="kenya">Kenya</option>
```

The text between the opening and closing tags is what the user sees.

The `value` attribute represents the value associated with that option when the form is submitted.

## The `<textarea>` Element

The `<textarea>` element creates a larger area for entering text.

```html
<textarea id="message" name="message" rows="5" cols="40"></textarea>
```

It is useful for:

* Messages
* Comments
* Feedback
* Descriptions

Unlike `<input>`, `<textarea>` has both an opening and closing tag.

## The `<button>` Element

The `<button>` element creates a clickable button.

Example:

```html
<button type="submit">Submit Form</button>
```

A form can also have a reset button:

```html
<button type="reset">Reset Form</button>
```

### Submit Button

```html
<button type="submit">Submit Form</button>
```

The submit button is used to submit the form.

### Reset Button

```html
<button type="reset">Reset Form</button>
```

The reset button returns the form controls to their initial values.

## The `name` Attribute

The `name` attribute identifies a form control when form data is submitted.

Example:

```html
<input type="text" name="username">
```

The `name` attribute is particularly important when form data is sent to a server.

## The `id` Attribute

The `id` attribute gives an element a unique identifier.

Example:

```html
<input type="text" id="name">
```

The `id` is also used to connect an input with its `<label>`:

```html
<label for="name">Full Name:</label>
<input type="text" id="name">
```

## Understanding `id`, `name`, and `value`

These three attributes have different purposes.

```html
<input
    type="text"
    id="name"
    name="name"
    value="Michael"
>
```

| Attribute | Purpose                                           |
| --------- | ------------------------------------------------- |
| `id`      | Uniquely identifies the element in the page.      |
| `name`    | Identifies the form field when data is submitted. |
| `value`   | Represents the value associated with the control. |

## Form Structure

The form created in `index.html` can be represented like this:

```text
<form>
│
├── <label>
├── <input type="text">
│
├── <label>
├── <input type="email">
│
├── <label>
├── <input type="password">
│
├── <label>
├── <input type="number">
│
├── <label>
├── <input type="date">
│
├── Radio Buttons
│
├── Checkboxes
│
├── <select>
│   └── <option>
│
├── <textarea>
│
└── <button>
```

## Form Attributes

The `<form>` element can also use attributes that control how and where form data is submitted.

### `action`

The `action` attribute specifies where the form data should be sent.

Example:

```html
<form action="/submit">
```

### `method`

The `method` attribute specifies how the form data should be sent.

Two commonly used methods are:

```html
<form method="get">
```

and:

```html
<form method="post">
```

These concepts become more important when working with backend programming.

## Required Fields

The `required` attribute can be used to make a field mandatory.

Example:

```html
<input type="text" id="name" name="name" required>
```

The browser will normally prevent submission until the required field has been filled.

## Placeholder Text

The `placeholder` attribute provides a hint inside an input.

Example:

```html
<input
    type="text"
    id="name"
    name="name"
    placeholder="Enter your name"
>
```

Placeholder text is a hint, not a replacement for a proper `<label>`.

## Form Validation

HTML provides some built-in validation through input types and attributes.

For example:

```html
<input type="email" required>
```

This tells the browser that:

* The field must be completed.
* The entered value should have an email-like format.

More advanced validation can be performed using HTML, CSS, and JavaScript.

## What I Practiced

In `index.html`, I practiced:

* Creating a form using `<form>`.
* Creating labels using `<label>`.
* Creating text inputs.
* Creating email inputs.
* Creating password inputs.
* Creating number inputs.
* Creating date inputs.
* Creating radio buttons.
* Creating checkboxes.
* Creating dropdown menus.
* Creating text areas.
* Creating submit and reset buttons.
* Using `id`, `name`, `for`, and `value` attributes.
* Grouping related form controls.

## Common Mistakes

1. Forgetting to connect a `<label>` to its input using `for` and `id`.
2. Using different `name` values for radio buttons that should belong to the same group.
3. Forgetting the closing `</form>` tag.
4. Using `<input>` with an unnecessary closing tag.
5. Forgetting the `name` attribute when learning how form data is submitted.
6. Using placeholder text instead of labels.
7. Using tables to create form layouts.
8. Assuming an HTML form automatically stores data permanently.

## Important Concepts

| Concept       | Meaning                                    |
| ------------- | ------------------------------------------ |
| `<form>`      | Container for form controls.               |
| `<label>`     | Describes a form control.                  |
| `<input>`     | Creates different types of input controls. |
| `type`        | Determines the type of input.              |
| `id`          | Identifies an element uniquely.            |
| `name`        | Identifies a form field during submission. |
| `value`       | Represents the value of a form control.    |
| `<select>`    | Creates a dropdown list.                   |
| `<option>`    | Creates an option inside a dropdown.       |
| `<textarea>`  | Creates a multi-line text input.           |
| `<button>`    | Creates a clickable button.                |
| `required`    | Makes a field mandatory.                   |
| `placeholder` | Provides a hint inside an input.           |
| `action`      | Specifies where form data is sent.         |
| `method`      | Specifies how form data is sent.           |

## Practice Tasks

Try modifying `index.html` by:

1. Adding a phone number field.
2. Adding a gender selection using radio buttons.
3. Adding more countries to the dropdown.
4. Adding a checkbox for accepting terms and conditions.
5. Adding a `required` attribute to important fields.
6. Adding placeholder text to some inputs.
7. Adding another textarea for additional comments.
8. Creating a simple student registration form.

## Key Takeaways

* Forms allow users to enter and submit information.
* `<form>` is the main container for form controls.
* `<input>` can create many different types of controls.
* `<label>` provides a description for an input.
* Radio buttons are generally used when choosing one option from a group.
* Checkboxes allow multiple selections.
* `<select>` and `<option>` create dropdown menus.
* `<textarea>` is used for multi-line text.
* `<button>` creates buttons for actions such as submitting or resetting a form.
* `id`, `name`, and `value` have different purposes.
* HTML provides basic form validation.
* A form's data usually needs a backend or another service to actually be processed and stored.

## Folder Contents

```text
08-forms/
├── index.html
└── README.md
```

## Learning Progress

This topic is part of my HTML learning journey. It builds on previous topics such as document structure, headings, paragraphs, links, images, lists, and tables.
