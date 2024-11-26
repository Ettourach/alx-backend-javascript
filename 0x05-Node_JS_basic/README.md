# Node.js Basics

## Table of Contents
1. [What is Node.js?](#what-is-nodejs)
2. [Learning Objectives](#learning-objectives)
   - [Run JavaScript Using Node.js](#1-run-javascript-using-nodejs)
   - [Use Node.js Modules](#2-use-nodejs-modules)
   - [Use Specific Node.js Modules to Read Files](#3-use-specific-nodejs-modules-to-read-files)
   - [Use `process` to Access Command Line Arguments and the Environment](#4-use-process-to-access-command-line-arguments-and-the-environment)
   - [Create a Small HTTP Server Using Node.js](#5-create-a-small-http-server-using-nodejs)
   - [Create a Small HTTP Server Using Express.js](#6-create-a-small-http-server-using-expressjs)
   - [Create Advanced Routes with Express.js](#7-create-advanced-routes-with-expressjs)
   - [Use ES6 with Node.js with Babel-Node](#8-use-es6-with-nodejs-with-babel-node)
   - [Use Nodemon to Develop Faster](#9-use-nodemon-to-develop-faster)

---

## What is Node.js?

Node.js is a cross-platform, open-source JavaScript runtime environment that allows developers to execute JavaScript code on the server side. Built on Chrome's V8 JavaScript engine, Node.js is designed for scalability, performance, and non-blocking asynchronous programming. It enables developers to create fast, scalable network applications using JavaScript.

---

## Learning Objectives

### 1. Run JavaScript Using Node.js

Node.js allows you to execute JavaScript outside of a browser, making it suitable for server-side scripting.

#### Example:
Create a file `hello.js`:
```javascript
console.log('Hello, Node.js!');

*Run it using node.js
'node hello.js'

### 2. Use Node.js Modules

Modules in Node.js help encapsulate code into reusable pieces. You can use built-in modules like fs, http, and path or create your own.

#### Example: Built-in Module
javascript
const path = require('path');
const filePath = path.join('/users', 'docs', 'file.txt');
console.log(filePath);

#### Example: Custom Module
Create a file math.js:
javascript
exports.add = (a, b) => a + b;

#### Use the module in app.js:
javascript
const math = require('./math');
console.log(math.add(2, 3)); // Output: 5


### 3. Use Specific Node.js Modules to Read Files

The fs module lets you interact with the file system to read, write, or manipulate files.

#### Example: Read File
javascript
const fs = require('fs');

fs.readFile('example.txt', 'utf8', (err, data) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log(data);
});

### 4. Use process to Access Command Line Arguments and the Environment

The process object in Node.js provides information about the current runtime environment.

#### Example: Access Command-Line Arguments
javascript
console.log(`Hello, ${process.argv[2]}!`);

*Run the script:

bash
node app.js Ilyas
# Output: Hello, Ilyas!

#### Example:
**Access Environment Variables
javascript
console.log(`Node environment: ${process.env.NODE_ENV}`);

### 5. Create a Small HTTP Server Using Node.js

The http module in Node.js allows you to create a web server to handle HTTP requests and responses.

#### Example:
javascript
const http = require('http');

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Hello, world!');
});

server.listen(3000, () => {
  console.log('Server running at http://localhost:3000/');
});

### 6. Create a Small HTTP Server Using Express.js

Express.js simplifies web server development with built-in features like routing and middleware.

#### Example:
javascript
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello, Express!');
});

app.listen(3000, () => {
  console.log('Server running at http://localhost:3000/');
});

### 7. Create Advanced Routes with Express.js

Express.js supports complex routing patterns for handling URL parameters and HTTP methods.

#### Example:
javascript
const express = require('express');
const app = express();

// Dynamic route
app.get('/user/:id', (req, res) => {
  res.send(`User ID: ${req.params.id}`);
});

// Query parameters
app.get('/search', (req, res) => {
  res.send(`Search query: ${req.query.q}`);
});

app.listen(3000, () => {
  console.log('Server running at http://localhost:3000/');
});

### 8. Use ES6 with Node.js with Babel-Node

Babel allows developers to use modern ES6+ JavaScript syntax with Node.js by transpiling the code.

#### Example:
**Install Babel:
bash
npm install --save-dev @babel/core @babel/cli @babel/preset-env

**Create a .babelrc file:
json
{
  "presets": ["@babel/preset-env"]
}
**Write ES6 code:
javascript
// app.js
import path from 'path';

console.log(path.join('/foo', 'bar'));

*Run the code:
bash
npx babel-node app.js

### 9. Use Nodemon to Develop Faster

Nodemon monitors changes in your application files and automatically restarts the server when changes are detected.

#### Example:
**Install Nodemon:

bash
npm install -g nodemon

*Run your app with Nodemon:
bash
nodemon app.js

