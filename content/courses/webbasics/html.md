---
title: Let's Start learning HTML  
linktitle: HTML
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  webbasics:
    parent: The Fundamentals
    weight: 1

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

HTML (HyperText Markup Language) is the standard language for creating web pages. It provides the structure of a web page and allows embedding various elements like text, images, and multimedia.

## What is HTML?

HTML is a markup language used to structure content on the web. It uses a series of elements represented by tags to create the desired layout and format for web pages.

### Basic HTML Document Structure

```html
<!DOCTYPE html>
<html>
<head>
  <title>Example Page</title>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>This is a simple web page.</p>
</body>
</html>
```

### Main Components

- **DOCTYPE Declaration:** Defines the document type and HTML version.
- **HTML Tag (`<html>`):** Encloses the entire HTML document.
- **Head Tag (`<head>`):** Contains meta-information about the document (e.g., title, character set).
- **Body Tag (`<body>`):** Contains the content of the document that is displayed to the user.

## HTML Elements

HTML elements are the building blocks of an HTML document. They are defined using tags, which are enclosed in angle brackets.

### Common HTML Tags

| Tag            | Description                                        | Example                          |
|----------------|----------------------------------------------------|----------------------------------|
| `<h1> - <h6>`  | Headings (h1 is the highest, h6 is the lowest)     | `<h1>Heading 1</h1>`             |
| `<p>`          | Paragraph                                          | `<p>This is a paragraph.</p>`    |
| `<a>`          | Anchor (creates hyperlinks)                       | `<a href="https://example.com">Link</a>` |
| `<img>`        | Image                                              | `<img src="image.jpg" alt="Description">` |
| `<ul>`         | Unordered list                                     | `<ul><li>Item 1</li><li>Item 2</li></ul>` |
| `<ol>`         | Ordered list                                       | `<ol><li>First item</li><li>Second item</li></ol>` |
| `<div>`        | Division (container for other elements)            | `<div>Content</div>`             |
| `<span>`       | Inline container                                   | `<span>Inline content</span>`    |
| `<form>`       | Form (collects user input)                         | `<form><input type="text"></form>` |

## Attributes

Attributes provide additional information about HTML elements. They are included in the opening tag and usually come in name/value pairs.

### Common Attributes

| Attribute | Description                                | Example                           |
|-----------|--------------------------------------------|-----------------------------------|
| `href`    | URL for anchor and link elements           | `<a href="https://example.com">Link</a>` |
| `src`     | URL of the image or script file            | `<img src="image.jpg" alt="Description">` |
| `alt`     | Alternative text for images                | `<img src="image.jpg" alt="Description">` |
| `id`      | Unique identifier for an element           | `<div id="unique-id">Content</div>` |
| `class`   | Class name for grouping multiple elements  | `<p class="text">Paragraph</p>`   |
| `type`    | Specifies the type of input element        | `<input type="text">`             |
| `name`    | Name of the input element                  | `<input name="username">`         |

## Semantic HTML

Semantic HTML uses tags that convey the meaning of the content they enclose. This improves accessibility and SEO.

### Examples of Semantic Elements

| Tag         | Description                                    | Example                           |
|-------------|------------------------------------------------|-----------------------------------|
| `<header>`  | Represents a group of introductory content     | `<header><h1>Site Title</h1></header>` |
| `<nav>`     | Contains navigation links                      | `<nav><a href="#">Home</a></nav>` |
| `<article>` | Independent, self-contained content            | `<article><h2>Article Title</h2><p>Article content.</p></article>` |
| `<section>` | Defines a section in a document                | `<section><h2>Section Title</h2><p>Section content.</p></section>` |
| `<footer>`  | Footer for a document or section               | `<footer><p>Footer content.</p></footer>` |

## Forms

Forms are used to collect user input. They consist of form controls like text fields, radio buttons, checkboxes, and submit buttons.

### Example Form

```html
<form action="/submit-form" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name"><br>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email"><br>
  <input type="submit" value="Submit">
</form>
```

### Form Attributes

| Attribute | Description                            | Example                          |
|-----------|----------------------------------------|----------------------------------|
| `action`  | URL to send form data to               | `<form action="/submit-form">`   |
| `method`  | HTTP method to use (GET or POST)       | `<form method="post">`           |
| `id`      | Unique identifier for the form element | `<form id="user-form">`          |

## HTML5 New Elements

HTML5 introduced several new elements to improve the semantic structure and multimedia support.

### Examples of HTML5 Elements

| Tag          | Description                                          | Example                           |
|--------------|------------------------------------------------------|-----------------------------------|
| `<figure>`   | Encapsulates media content and its caption           | `<figure><img src="image.jpg" alt="Description"><figcaption>Caption</figcaption></figure>` |
| `<figcaption>` | Provides a caption for the `<figure>` element      | `<figcaption>Caption text</figcaption>` |
| `<video>`    | Embeds a video                                       | `<video controls><source src="movie.mp4" type="video/mp4"></video>` |
| `<audio>`    | Embeds an audio file                                 | `<audio controls><source src="audio.mp3" type="audio/mp3"></audio>` |
| `<canvas>`   | Used for drawing graphics via scripting (usually JavaScript) | `<canvas id="myCanvas"></canvas>` |

## Example: A Complete HTML Page

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Website</title>
  <style>
    body { font-family: Arial, sans-serif; }
    header, footer { background-color: #f8f9fa; padding: 10px; }
    main { margin: 20px; }
  </style>
</head>
<body>
  <header>
    <h1>Welcome to My Website</h1>
  </header>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
  <main>
    <section id="home">
      <h2>Home</h2>
      <p>This is the home page.</p>
    </section>
    <section id="about">
      <h2>About</h2>
      <p>This is the about page.</p>
    </section>
    <section id="contact">
      <h2>Contact</h2>
      <form action="/submit-form" method="post">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name"><br>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email"><br>
        <input type="submit" value="Submit">
      </form>
    </section>
  </main>
  <footer>
    <p>&copy; 2024 My Website</p>
  </footer>
</body>
</html>
```

## Quiz

### 1. Which tag is used to create a hyperlink?
- [ ] `<p>`
- [ ] `<img>`
- [ ] `<a>`
- [ ] `<div>`

### 2. What does the `alt` attribute provide?
- [ ] URL for the image source
- [ ] Alternative text for images
- [ ] The title of the page
- [ ] Class name for styling

### 3. Which HTML5 element is used for drawing graphics via scripting?
- [ ] `<canvas>`
- [ ] `<video>`
- [ ] `<figure>`
- [ ] `<audio>`

### 4. What is the purpose of semantic HTML?
- [ ] To style the content
- [ ] To structure the content meaningfully
- [ ] To add animations
- [ ] To manage user input

### 5. What attribute is used to specify the destination URL of a form submission?
- [ ] `method`
- [ ] `action`
- [ ] `src`
- [ ] `href`

### 6. Which tag is used to create a paragraph?
- [ ] `<h1>`
- [ ] `<p>`
- [ ] `<div>`
- [ ] `<span>`

### 7. What does the `<header>` element represent?
- [ ] The main content of the document
- [ ] A group of introductory content
- [ ] A section in a document
- [ ] A footer for a document or section

Complete this quiz to test your understanding of HTML fundamentals!

Cras aliquam rhoncus ipsum, in hendrerit nunc mattis vitae. Duis vitae efficitur metus, ac tempus leo. Cras nec fringilla lacus. Quisque sit amet risus at ipsum pharetra commodo. Sed aliquam mauris at consequat eleifend. Praesent porta, augue sed viverra bibendum, neque ante euismod ante, in vehicula justo lorem ac eros. Suspendisse augue libero, venenatis eget tincidunt ut, malesuada at lorem. Donec vitae bibendum arcu. Aenean maximus nulla non pretium iaculis. Quisque imperdiet, nulla in pulvinar aliquet, velit quam ultrices quam, sit amet fringilla leo sem vel nunc. Mauris in lacinia lacus.

Suspendisse a tincidunt lacus. Curabitur at urna sagittis, dictum ante sit amet, euismod magna. Sed rutrum massa id tortor commodo, vitae elementum turpis tempus. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean purus turpis, venenatis a ullamcorper nec, tincidunt et massa. Integer posuere quam rutrum arcu vehicula imperdiet. Mauris ullamcorper quam vitae purus congue, quis euismod magna eleifend. Vestibulum semper vel augue eget tincidunt. Fusce eget justo sodales, dapibus odio eu, ultrices lorem. Duis condimentum lorem id eros commodo, in facilisis mauris scelerisque. Morbi sed auctor leo. Nullam volutpat a lacus quis pharetra. Nulla congue rutrum magna a ornare.

Aliquam in turpis accumsan, malesuada nibh ut, hendrerit justo. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Quisque sed erat nec justo posuere suscipit. Donec ut efficitur arcu, in malesuada neque. Nunc dignissim nisl massa, id vulputate nunc pretium nec. Quisque eget urna in risus suscipit ultricies. Pellentesque odio odio, tincidunt in eleifend sed, posuere a diam. Nam gravida nisl convallis semper elementum. Morbi vitae felis faucibus, vulputate orci placerat, aliquet nisi. Aliquam erat volutpat. Maecenas sagittis pulvinar purus, sed porta quam laoreet at.
