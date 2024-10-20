---
# Course title, summary, and position.
linktitle: Let's learn basics of web development  
summary: Learn Web development concept fundamentals slowly progressing towards HTML, CSS, Javascript
weight: 1

# Page metadata.
title:  
date: "2018-09-09T00:00:00Z"
lastmod: "2018-09-09T00:00:00Z"
draft: false  # Is this a draft? true/false
toc: true  # Show table of contents? true/false
type: docs  # Do not modify.

# Add menu entry to sidebar.
# - name: Declare this menu item as a parent with ID `name`.
# - weight: Position of link in menu.
menu:
  reactjs:
    name: Learn React
    weight: 2
---

# Web Development Fundamentals

Web development is the process of building and maintaining websites. It encompasses a variety of skills and disciplines in the production and maintenance of websites. Here’s a comprehensive guide to the fundamentals and essential knowledge for web developers:

## What is a Server?
A server is a computer system or device that provides resources, data, services, or programs to other computers, known as clients, over a network.

### Types of Servers:
- **Web Server:** Hosts websites and delivers web pages to clients via HTTP/HTTPS.
- **Database Server:** Provides database services to other computer programs or computers.
- **File Server:** Stores and manages files for network users.
- **Mail Server:** Manages and transfers emails over a network.

### Example:
When you type "www.example.com" in your browser, a request is sent to the web server hosting the website, which then sends back the requested web page.

## Client-Server Architecture
Client-server architecture is a network structure where clients (user devices) request services and resources from a server.

### Diagram:
```plaintext
Client (Browser) <---> Internet <---> Server
```

### Components:
- **Client:** The user interface device (like a browser) that requests resources.
- **Server:** The system providing resources or services to the client.

## HTTP Requests and Responses
HTTP (HyperText Transfer Protocol) is the foundation of any data exchange on the Web.

### HTTP Request Methods:
- **GET:** Requests data from a server.
- **POST:** Submits data to be processed to a server.
- **PUT:** Updates data on a server.
- **DELETE:** Deletes data from a server.

### HTTP Response Status Codes:
- **200 OK:** The request was successful.
- **404 Not Found:** The requested resource could not be found.
- **500 Internal Server Error:** The server encountered an error.

### Example Request-Response Cycle:
1. **Request:** Client sends a GET request to `http://example.com`.
2. **Response:** Server responds with status code 200 and the requested HTML page.

```plaintext
GET /index.html HTTP/1.1
Host: www.example.com

HTTP/1.1 200 OK
Content-Type: text/html

<html>
<body>
<h1>Welcome to Example.com!</h1>
</body>
</html>
```

## Front-End Development
Front-end development involves creating the part of the website that users interact with directly.

### Core Technologies:
- **HTML (HyperText Markup Language):** Structures the content.
- **CSS (Cascading Style Sheets):** Styles the content.
- **JavaScript:** Adds interactivity to the content.

### Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>Example Page</title>
  <style>
    body { font-family: Arial, sans-serif; }
  </style>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>This is a simple web page.</p>
  <script>
    console.log('Page loaded');
  </script>
</body>
</html>
```

## Back-End Development
Back-end development involves creating the server-side logic and database interactions.

### Core Languages:
- **Python:** Often used with frameworks like Django or Flask.
- **JavaScript (Node.js):** Server-side JavaScript environment.
- **Java:** Used in large-scale applications.
- **PHP:** Widely used for web development.

### Example (Node.js with Express):
```javascript
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello, World!');
});

app.listen(3000, () => {
  console.log('Server running on port 3000');
});
```

## Databases
Databases store and manage data for websites and applications.

### Types of Databases:
- **SQL Databases:** Structured Query Language databases (e.g., MySQL, PostgreSQL).
- **NoSQL Databases:** Non-relational databases (e.g., MongoDB, CouchDB).

### Example (SQL Query):
```sql
SELECT * FROM users WHERE user_id = 1;
```

## APIs
APIs (Application Programming Interfaces) allow different software systems to communicate with each other.

### Example:
A weather application fetching data from a weather API:
```plaintext
GET /weather?city=Kathmandu
Host: api.weather.com

HTTP/1.1 200 OK
Content-Type: application/json

{
  "city": "Kathmandu",
  "temperature": "22°C",
  "condition": "Sunny"
}
```

## Web Development Tools
Various tools assist developers in building, testing, and maintaining websites.

### Essential Tools:
- **Code Editors:** VSCode, Sublime Text.
- **Version Control:** Git, GitHub.
- **Browser DevTools:** Inspect and debug web pages.
- **Package Managers:** npm, yarn for JavaScript libraries.
- **Frameworks:** React, Angular for front-end; Django, Express for back-end.

## Summary
Web development involves a combination of front-end and back-end technologies. Understanding how servers work, how HTTP requests and responses function, and being familiar with development tools are all crucial for building and maintaining modern web applications.

## Quiz

### 1. What does a web server do?
- [ ] Stores and retrieves emails.
- [ ] Hosts websites and delivers web pages.
- [ ] Manages and organizes files.
- [ ] Provides database services.

### 2. Which HTTP method is used to update data on a server?
- [ ] GET
- [ ] POST
- [ ] PUT
- [ ] DELETE

### 3. What are the core technologies of front-end development?
- [ ] HTML, CSS, Python
- [ ] HTML, CSS, JavaScript
- [ ] JavaScript, SQL, PHP
- [ ] HTML, PHP, CSS

### 4. Which of the following is a NoSQL database?
- [ ] MySQL
- [ ] PostgreSQL
- [ ] MongoDB
- [ ] SQLite

### 5. What is the purpose of APIs?
- [ ] Style web content.
- [ ] Structure web content.
- [ ] Allow software systems to communicate.
- [ ] Manage database interactions.

### 6. Which tool is used for version control?
- [ ] npm
- [ ] Git
- [ ] VSCode
- [ ] Express

### 7. What is the role of back-end development?
- [ ] Create user interfaces.
- [ ] Style web pages.
- [ ] Handle server-side logic and database interactions.
- [ ] Debug web pages.

Complete this quiz to test your understanding of web development fundamentals!
