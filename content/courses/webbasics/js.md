---
title: Let's Start learning Javascript  
linktitle: Javascript
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  webbasics:
    parent: The Fundamentals
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3
---

JavaScript is a versatile, high-level programming language used to create dynamic and interactive effects within web browsers. It is an essential part of web development, alongside HTML and CSS.

## What is JavaScript?

JavaScript enables you to implement complex things on web pages. It can be used to update and change both HTML and CSS, as well as calculate, manipulate, and validate data.

### Basic Syntax

JavaScript code is written in plain text, just like HTML and CSS. It can be included directly in HTML files using the `<script>` tag or in separate files with a `.js` extension.

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Example</title>
  <script>
    function greet() {
      alert('Hello, World!');
    }
  </script>
</head>
<body>
  <button onclick="greet()">Click Me</button>
</body>
</html>
```

## Variables

Variables are containers for storing data values. In JavaScript, you can declare variables using `var`, `let`, or `const`.

### Variable Declaration

```javascript
var name = "John";
let age = 30;
const PI = 3.14;
```

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>Variables Example</title>
  <script>
    var name = "John";
    let age = 30;
    const PI = 3.14;

    function displayInfo() {
      alert("Name: " + name + ", Age: " + age + ", PI: " + PI);
    }
  </script>
</head>
<body>
  <button onclick="displayInfo()">Show Info</button>
</body>
</html>
```

## Data Types

JavaScript supports various data types, including primitive types and objects.

### Primitive Data Types

| Type      | Description                           | Example                       |
|-----------|---------------------------------------|-------------------------------|
| String    | Sequence of characters                | `"Hello, World!"`             |
| Number    | Numeric values                        | `42`, `3.14`                  |
| Boolean   | True or false values                  | `true`, `false`               |
| Null      | Represents the intentional absence of any object value | `null`                     |
| Undefined | Represents an undefined value         | `undefined`                   |
| Symbol    | Unique and immutable data type        | `Symbol('id')`                |

### Objects

Objects are collections of properties and methods.

```javascript
let person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
```

## Functions

Functions are blocks of code designed to perform particular tasks. They are executed when something invokes them (calls them).

### Function Declaration

```javascript
function greet(name) {
  return "Hello, " + name;
}
```

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>Functions Example</title>
  <script>
    function greet(name) {
      return "Hello, " + name;
    }

    function displayGreeting() {
      let name = prompt("Enter your name:");
      alert(greet(name));
    }
  </script>
</head>
<body>
  <button onclick="displayGreeting()">Greet</button>
</body>
</html>
```

## Events

JavaScript can respond to various events triggered by the user, such as clicking a button, hovering over an element, or submitting a form.

### Event Handling

You can assign event handlers directly in HTML or using JavaScript.

```html
<!DOCTYPE html>
<html>
<head>
  <title>Events Example</title>
  <script>
    function changeText() {
      document.getElementById("demo").innerHTML = "Text changed!";
    }
  </script>
</head>
<body>
  <p id="demo">This is a paragraph.</p>
  <button onclick="changeText()">Change Text</button>
</body>
</html>
```

## DOM Manipulation

The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content.

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>DOM Manipulation Example</title>
  <script>
    function changeContent() {
      document.getElementById("demo").innerHTML = "Hello, World!";
      document.getElementById("demo").style.color = "blue";
    }
  </script>
</head>
<body>
  <p id="demo">This is a paragraph.</p>
  <button onclick="changeContent()">Change Content</button>
</body>
</html>
```

## Loops

Loops are used to repeatedly execute a block of code as long as a specified condition is true.

### Types of Loops

| Loop       | Description                                      | Example                           |
|------------|--------------------------------------------------|-----------------------------------|
| `for`      | Loops through a block of code a number of times  | `for (let i = 0; i < 5; i++) { ... }` |
| `while`    | Loops through a block of code while a condition is true | `while (i < 10) { ... }`           |
| `do...while` | Loops through a block of code once, and then repeats the loop as long as a condition is true | `do { ... } while (i < 5);` |

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>Loops Example</title>
  <script>
    function displayNumbers() {
      let numbers = "";
      for (let i = 1; i <= 5; i++) {
        numbers += i + " ";
      }
      document.getElementById("demo").innerHTML = numbers;
    }
  </script>
</head>
<body>
  <button onclick="displayNumbers()">Show Numbers</button>
  <p id="demo"></p>
</body>
</html>
```

## Arrays

Arrays are used to store multiple values in a single variable.

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>Arrays Example</title>
  <script>
    function displayArray() {
      let fruits = ["Apple", "Banana", "Cherry"];
      let fruitList = "";
      for (let i = 0; i < fruits.length; i++) {
        fruitList += fruits[i] + " ";
      }
      document.getElementById("demo").innerHTML = fruitList;
    }
  </script>
</head>
<body>
  <button onclick="displayArray()">Show Fruits</button>
  <p id="demo"></p>
</body>
</html>
```

## Objects

Objects are collections of key-value pairs. Each key-value pair is called a property.

### Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>Objects Example</title>
  <script>
    let car = {
      make: "Toyota",
      model: "Camry",
      year: 2021,
      displayInfo: function() {
        return this.make + " " + this.model + " (" + this.year + ")";
      }
    };

    function showCarInfo() {
      document.getElementById("demo").innerHTML = car.displayInfo();
    }
  </script>
</head>
<body>
  <button onclick="showCarInfo()">Show Car Info</button>
  <p id="demo"></p>
</body>
</html>
```

## Summary

JavaScript is a powerful language that adds interactivity to web pages. Understanding variables, data types, functions, events, DOM manipulation, loops, arrays, and objects is essential for creating dynamic and interactive web applications.

## Quiz

### 1. Which of the following is a valid way to declare a variable in JavaScript?
- [ ] `variable name = "John";`
- [ ] `let name = "John";`
- [ ] `var: name = "John";`
- [ ] `name = "John" var;`

### 2. How do you create a function in JavaScript?
- [ ] `function:myFunction() { ... }`
- [ ] `function myFunction() { ... }`
- [ ] `def myFunction() { ... }`
- [ ] `create function myFunction() { ... }`

### 3. Which event occurs when the user clicks on an HTML element?
- [ ] `onmouseclick`
- [ ] `onclick`
- [ ] `onchange`
- [ ] `onmouseover`

### 4. How can you change the content of an HTML element with id "demo"?
- [ ] `document.getElementByName("demo").innerHTML = "Hello";`
- [ ] `document.getElementById("demo").innerHTML = "Hello";`
- [ ] `document.getElementByIdName("demo").innerHTML = "Hello";`
- [ ] `document.getElement("demo").innerHTML = "Hello";`

### 5. What does the `for` loop do?
- [ ] Loops through a block of code a number of times
- [ ] Loops through a block of code while a condition is true
- [ ] Loops through a block of code once, and then repeats the loop as long as a condition is true
- [ ] Loops through the properties of an object

### 6. How do you declare an array in JavaScript?
- [ ] `let fruits = {"Apple", "Banana", "

Cherry"};`
- [ ] `let fruits = (1:"Apple", 2:"Banana", 3:"Cherry");`
- [ ] `let fruits = ["Apple", "Banana", "Cherry"];`
- [ ] `let fruits = "Apple", "Banana", "Cherry";`

### 7. How do you access the first element in an array called `fruits`?
- [ ] `fruits[0]`
- [ ] `fruits[1]`
- [ ] `fruits(0)`
- [ ] `fruits{0}`

Complete this quiz to test your understanding of JavaScript fundamentals!
