# HTML Tables

This topic focuses on learning how to create and organize tables in HTML. Tables are useful for displaying information in rows and columns.

## What Are HTML Tables?

An HTML table is used to present related information in a structured format consisting of:

* **Rows** — horizontal groups of cells.
* **Columns** — vertical groups of cells.
* **Cells** — individual spaces containing information.

For example, a table can be used to display student marks, programming languages, study schedules, or product information.

## Basic Table Syntax

```html
<table>
    <tr>
        <th>Heading 1</th>
        <th>Heading 2</th>
    </tr>

    <tr>
        <td>Data 1</td>
        <td>Data 2</td>
    </tr>
</table>
```

## Important Table Elements

| Element     | Description                               |
| ----------- | ----------------------------------------- |
| `<table>`   | Defines an HTML table.                    |
| `<caption>` | Adds a title or description to the table. |
| `<tr>`      | Defines a table row.                      |
| `<th>`      | Defines a table heading cell.             |
| `<td>`      | Defines a regular table data cell.        |
| `<thead>`   | Groups the heading rows of a table.       |
| `<tbody>`   | Groups the main data rows of a table.     |
| `<tfoot>`   | Groups the footer rows of a table.        |

## Understanding the Table Structure

A table can be understood using this structure:

```text
<table>
│
├── <caption>Table Title</caption>
│
├── <tr>
│   ├── <th>Heading</th>
│   └── <th>Heading</th>
│
└── <tr>
    ├── <td>Data</td>
    └── <td>Data</td>
</table>
```

### 1. The `<table>` Element

The `<table>` element is the main container for all table content.

```html
<table>
    <!-- Table rows and cells go here -->
</table>
```

### 2. The `<tr>` Element

The `<tr>` element creates a table row.

```html
<tr>
    <td>HTML</td>
    <td>Webpage structure</td>
</tr>
```

### 3. The `<th>` Element

The `<th>` element creates a heading cell. It identifies the information contained in a column or row.

```html
<th>Language</th>
<th>Purpose</th>
```

Browsers usually display heading cells in bold text and center them by default.

### 4. The `<td>` Element

The `<td>` element creates a regular data cell.

```html
<td>HTML</td>
<td>Webpage structure</td>
```

### 5. The `<caption>` Element

The `<caption>` element provides a title for the table.

```html
<table>
    <caption>Programming Languages</caption>
</table>
```

A caption helps users understand what the table contains.

## Example: Programming Languages Table

The following example is included in `index.html`:

```html
<table border="1">

    <caption>Programming Languages I Am Learning</caption>

    <tr>
        <th>Language</th>
        <th>Purpose</th>
        <th>Level</th>
    </tr>

    <tr>
        <td>HTML</td>
        <td>Webpage structure</td>
        <td>Beginner</td>
    </tr>

    <tr>
        <td>CSS</td>
        <td>Webpage styling</td>
        <td>Beginner</td>
    </tr>

    <tr>
        <td>JavaScript</td>
        <td>Webpage interaction</td>
        <td>Beginner</td>
    </tr>

</table>
```

### How the Example Works

* `<table border="1">` creates the table and adds a basic visible border.
* `<caption>` gives the table a title.
* The first `<tr>` contains the column headings.
* Each `<th>` identifies a column.
* The following `<tr>` elements contain the data.
* Each `<td>` contains information for one cell.

## Table Rows and Columns

Consider this table:

| Language   | Purpose             | Level    |
| ---------- | ------------------- | -------- |
| HTML       | Webpage structure   | Beginner |
| CSS        | Webpage styling     | Beginner |
| JavaScript | Webpage interaction | Beginner |

This table contains:

* **3 columns:** Language, Purpose, and Level.
* **4 rows:** One heading row and three data rows.
* **12 cells:** 3 cells in each of the 4 rows.

## Using `border="1"`

The `border` attribute can be used to add a basic border around table cells.

```html
<table border="1">
```

The value `1` specifies a basic border size.

> The `border` attribute is useful for simple practice, but modern websites usually use CSS to style table borders.

Example using CSS:

```html
<style>
    table,
    th,
    td {
        border: 1px solid black;
        border-collapse: collapse;
    }
</style>
```

## Organizing Tables with `<thead>`, `<tbody>`, and `<tfoot>`

For more organized tables, HTML provides elements for grouping different parts of a table.

```html
<table>

    <thead>
        <tr>
            <th>Subject</th>
            <th>Marks</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>HTML</td>
            <td>85</td>
        </tr>

        <tr>
            <td>C++</td>
            <td>78</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td>Total</td>
            <td>163</td>
        </tr>
    </tfoot>

</table>
```

These elements help organize the table and make it easier to understand.

## Important Concepts

| Concept         | Meaning                                       |
| --------------- | --------------------------------------------- |
| Row             | A horizontal group of cells.                  |
| Column          | A vertical group of cells.                    |
| Heading cell    | A cell created using `<th>`.                  |
| Data cell       | A cell created using `<td>`.                  |
| Caption         | A title describing the table.                 |
| Table border    | A visible line around table cells.            |
| Table structure | The organization of rows, columns, and cells. |

## Common Mistakes

1. Forgetting to close the `<table>` element.
2. Placing table cells outside a `<tr>` element.
3. Using `<td>` instead of `<th>` for column headings.
4. Creating rows with different numbers of cells unintentionally.
5. Forgetting to close table rows or cells.
6. Using tables to design the entire webpage layout instead of displaying tabular data.
7. Relying only on the `border` attribute for modern website styling.

## What I Practiced

In `index.html`, I practiced:

* Creating tables using `<table>`.
* Creating rows using `<tr>`.
* Creating heading cells using `<th>`.
* Creating data cells using `<td>`.
* Adding table titles using `<caption>`.
* Displaying programming languages in a table.
* Creating a weekly study schedule.
* Using the `border` attribute to make table borders visible.

## Practice Tasks

Try improving the tables by:

1. Adding more programming languages.
2. Adding more days to the study schedule.
3. Creating a table showing student marks.
4. Creating a table showing products and prices.
5. Adding `<thead>` and `<tbody>` to one of the tables.
6. Styling the tables using CSS.
7. Researching and practicing `colspan` and `rowspan`.

## Key Takeaways

* The `<table>` element creates a table.
* The `<tr>` element creates a row.
* The `<th>` element creates a heading cell.
* The `<td>` element creates a data cell.
* The `<caption>` element gives a table a title.
* Tables organize information into rows and columns.
* CSS is preferred for modern table styling.
* Tables should be used for tabular information, not general webpage layout.

## Folder Contents

```text
07-tables/
├── index.html
└── README.md
```

## Learning Progress

This topic is part of my HTML learning journey. It builds on previous topics such as document structure, headings, paragraphs, links, images, and lists.
