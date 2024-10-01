// 0x01. ES6 Promises

Introduction

This project is focused on mastering JavaScript Promises using ES6 features. Promises are used for handling asynchronous operations in JavaScript, and this project will guide you through understanding the concepts of resolve, reject, then, catch, and finally.

The project consists of several tasks that will help you explore how to handle asynchronous code effectively, including error handling, chaining promises, and using the async/await syntax.

Learning Objectives

By the end of this project, you should be able to:

Understand what Promises are and why they are used.
Know how to use the then(), resolve(), and catch() methods.
Work with all the methods of the Promise object.
Use try/catch for error handling.
Understand and implement the await operator in an async function.
Requirements

All files are executed on Ubuntu 18.04 LTS using NodeJS v12.11.x.
You should use vi, vim, emacs, or Visual Studio Code as your editor.
All your files should end with a new line.
A README.md file is mandatory.
Your code should use the .js extension.
Your code will be tested using Jest with the command npm run test.
All functions must be exported.
Project Setup

Install NodeJS 12.x

curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
Install Dependencies
To set up your project, you need to install Jest, Babel, and ESLint. Make sure you are in your project directory

npm install
This will install all the necessary dependencies mentioned in the package.json file.

Project Configuration Files

The project comes with configuration files such as babel.config.js, .eslintrc.js, and package.json. These ensure that your project is set up correctly for linting, transpiling, and testing.

Tasks
0. Keep every promise you make
File: 0-promise.js
Description: Create a function getResponseFromAPI that returns a Promise.
1. Don't make a promise if you know you can't keep it
File: 1-promise.js
Description: Create a function getFullResponseFromAPI(success) that returns a promise. If success is true, resolve with an object; otherwise, reject with an error.
2. Catch me if you can!
File: 2-then.js
Description: Create a function handleResponseFromAPI(promise) that handles the resolution and rejection of a promise.
3. Handle multiple successful promises
File: 3-all.js
Description: Create a function handleProfileSignup that resolves two promises and logs the response.
4. Simple promise
File: 4-user-promise.js
Description: Create a function signUpUser(firstName, lastName) that returns a resolved promise with an object containing the first and last name.
5. Reject the promises
File: 5-photo-reject.js
Description: Create a function uploadPhoto that rejects a promise with an error message.
6. Handle multiple promises
File: 6-final-user.js
Description: Create a function handleProfileSignup(firstName, lastName, fileName) that handles multiple promises and returns their status.
7. Load balancer
File: 7-load_balancer.js
Description: Create a function loadBalancer(chinaDownload, USDownload) that returns the result of the first resolved promise.
8. Throw error / try catch
File: 8-try.js
Description: Create a function divideFunction(numerator, denominator) that throws an error if the denominator is zero.
9. Throw an error
File: 9-try.js
Description: Create a function guardrail that adds a guardrail after executing a function, regardless of the result.
Testing
This project uses Jest for testing. After implementing your functions, run the following command to execute the test cases:

npm run test
ESLint is used for linting your code. Make sure your code is properly formatted by running:
npm run lint

