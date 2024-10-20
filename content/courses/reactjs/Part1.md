---
title: Let's Start learning CSS  
linktitle: CSS
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  webbasics:
    parent: Learn React
    weight: 1

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a document written in HTML or XML. It controls the layout of multiple web pages all at once.

## What is CSS?

CSS defines how HTML elements should be displayed. By separating the content from the presentation, CSS allows for greater flexibility and control in the specification of presentation characteristics.

### Basic Syntax

CSS rules are made up of selectors and declarations. Declarations are enclosed in curly braces and consist of properties and their values.

```css
selector {
  property: value;
}
```

### Example

```css
body {
  background-color: lightblue;
}

h1 {
  color: navy;
  font-family: Arial, sans-serif;
}
```

## CSS Selectors

Selectors are used to "select" the HTML elements you want to style.

### Types of Selectors

| Selector    | Description                                      | Example                |
|-------------|--------------------------------------------------|------------------------|
| Element     | Selects all elements of a specific type          | `p { color: red; }`    |
| ID          | Selects a single element with a specific ID      | `#unique { color: blue; }` |
| Class       | Selects all elements with a specific class       | `.className { color: green; }` |
| Attribute   | Selects elements with a specific attribute       | `[type="text"] { color: black; }` |
| Universal   | Selects all elements                             | `* { color: gray; }`   |
| Descendant  | Selects elements that are descendants of another element | `div p { color: purple; }` |
| Pseudo-class| Selects elements in a specific state             | `a:hover { color: orange; }` |

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .highlight {
      color: red;
    }
    #main {
      background-color: yellow;
    }
    p {
      font-size: 16px;
    }
  </style>
</head>
<body>
  <div id="main">
    <p class="highlight">This is a highlighted paragraph.</p>
    <p>This is a normal paragraph.</p>
  </div>
</body>
</html>
```

## CSS Box Model

The CSS box model describes the rectangular boxes that are generated for elements in the document tree and governs the layout and positioning of these boxes.

### Components of the Box Model

| Component   | Description                                      | Example                          |
|-------------|--------------------------------------------------|----------------------------------|
| Margin      | Space outside the border                         | `margin: 20px;`                  |
| Border      | Surrounds the padding and content                | `border: 1px solid black;`       |
| Padding     | Space inside the border                          | `padding: 10px;`                 |
| Content     | The actual content of the element                | `width: 200px; height: 100px;`   |

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .box {
      width: 200px;
      height: 100px;
      border: 2px solid black;
      padding: 10px;
      margin: 20px;
    }
  </style>
</head>
<body>
  <div class="box">This is a box with padding and margin.</div>
</body>
</html>
```

## CSS Positioning

CSS positioning allows you to position an element precisely where you want it on the page.

### Types of Positioning

| Position    | Description                                      | Example                          |
|-------------|--------------------------------------------------|----------------------------------|
| Static      | Default position; elements are positioned according to the normal flow of the document | `position: static;`              |
| Relative    | Positioned relative to its normal position       | `position: relative; top: 10px; left: 10px;` |
| Absolute    | Positioned relative to the nearest positioned ancestor | `position: absolute; top: 50px; left: 50px;` |
| Fixed       | Positioned relative to the viewport              | `position: fixed; top: 0; right: 0;`         |
| Sticky      | Switches between relative and fixed depending on scroll position | `position: sticky; top: 20px;` |

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .static {
      position: static;
    }
    .relative {
      position: relative;
      top: 10px;
      left: 10px;
    }
    .absolute {
      position: absolute;
      top: 50px;
      left: 50px;
    }
    .fixed {
      position: fixed;
      top: 0;
      right: 0;
    }
  </style>
</head>
<body>
  <div class="static">Static Position</div>
  <div class="relative">Relative Position</div>
  <div class="absolute">Absolute Position</div>
  <div class="fixed">Fixed Position</div>
</body>
</html>
```

## Responsive Design

Responsive design ensures that web pages look good on all devices, from desktops to tablets to mobile phones.

### Techniques for Responsive Design

| Technique   | Description                                      | Example                          |
|-------------|--------------------------------------------------|----------------------------------|
| Media Queries | Apply different styles based on device properties (e.g., width, height) | `@media (max-width: 600px) { ... }` |
| Flexible Grid Layouts | Use relative units like percentages for widths | `width: 50%;`                    |
| Flexible Images | Use relative units or max-width property     | `img { max-width: 100%; height: auto; }` |

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .container {
      width: 100%;
      padding: 10px;
    }
    .box {
      width: 50%;
      padding: 10px;
      float: left;
    }
    @media (max-width: 600px) {
      .box {
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box" style="background-color:lightblue;">Box 1</div>
    <div class="box" style="background-color:lightcoral;">Box 2</div>
  </div>
</body>
</html>
```

## CSS Flexbox

CSS Flexbox is a layout module that allows you to design complex layouts with ease. It provides an efficient way to align and distribute space among items in a container.

### Basic Flexbox Properties

| Property        | Description                                      | Example                          |
|-----------------|--------------------------------------------------|----------------------------------|
| `display`       | Defines a flex container                        | `display: flex;`                 |
| `flex-direction`| Specifies the direction of the flex items       | `flex-direction: row;`           |
| `justify-content` | Aligns items along the main axis               | `justify-content: center;`       |
| `align-items`   | Aligns items along the cross axis               | `align-items: center;`           |
| `flex`          | Specifies the ability to grow or shrink          | `flex: 1;`                       |

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .container {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .box {
      width: 100px;
      height: 100px;
      margin: 10px;
    }
    .box1 { background-color: lightblue; }
    .box2 { background-color: lightcoral; }
    .box3 { background-color: lightgreen; }
  </style>
</head>
<body>
  <div class="container">
    <div class="box box1">1</div>
    <div class="box box2">2</div>
    <div class="box box3">3</div>
  </div>
</body>
</html>
```

## Summary

CSS is a powerful tool for styling HTML documents. It allows for a separation of content and presentation, making web design more flexible and efficient. Understanding the basic syntax, selectors, box model, positioning, responsive design, and layout techniques like Flexbox is essential for creating modern, responsive web pages.

## Quiz

### 1. What is the correct syntax for selecting elements with a specific class in CSS?
- [ ] `#className { ... }`
- [ ] `.className { ... }`
- [ ] `className { ... }`
- [ ] `*className { ... }`

### 2. Which property is used to change the background color of an element?
- [ ] `color`
- [ ] `background-color`
- [ ] `font-color`
- [ ] `text-color`

### 3. What does the `position: absolute;` property do?
- [ ] Positions an element relative to its normal position.
- [ ] Positions an element relative to the nearest positioned ancestor.
- [ ] Positions an element fixed relative to the viewport.
- [ ] Positions an element in a static manner.

### 4. What is the purpose of the CSS Box Model?
- [ ] To create animation effects.
- [ ] To control the layout and positioning of elements.
- [ ] To style text and fonts.
- [ ] To add JavaScript functionality.

### 5. Which CSS technique is used to apply different

 styles based on device properties?
- [ ] Flexbox
- [ ] Grid
- [ ] Media Queries
- [ ] Box Model

### 6. Which property is used to align items along the main axis in Flexbox?
- [ ] `align-items`
- [ ] `justify-content`
- [ ] `flex-direction`
- [ ] `flex-wrap`

### 7. What does the `flex` property do in Flexbox?
- [ ] Sets the direction of the flex container.
- [ ] Aligns items along the cross axis.
- [ ] Specifies the ability of a flex item to grow or shrink.
- [ ] Justifies content along the main axis.

Complete this quiz to test your understanding of CSS fundamentals!
