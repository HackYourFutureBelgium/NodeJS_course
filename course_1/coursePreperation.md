# Index
In this first course you will learn the following
- What is a server
- What is NodeJS
- NodeJS project setup
- NPM
- ES6
- How to make a server

# Intro
_Everyone says one by one his name and favorite website_
We will explain what a server is, based on the favorite websites and why it is important.

## What is a server?
A server is a computer program or a device that provides functionality for other programs or devices, called "clients".

## What is Node.js?
_Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine._

JavaScript runtime => Running JS outside of the browser
Compiles to machine code which makes it very fast

## Installing Node.js
Go to the [NodeJS installer page](https://nodejs.org/en/download/current/) and install the *latest* version of Node.JS.


### Run following code in your terminal
```
Node

console.log("Hello world");

var a = 5;
var b = 10;
console.log(a + b);

process.exit(0);
```

# What is NPM
npm => Node Packaging Manager

# Project setup
Based on: [codementor](https://www.codementor.io/iykyvic/writing-your-nodejs-apps-using-es6-6dh0edw2o) and [Gist](https://gist.github.com/rahman541/f23d7bb242520e17517644d4dd179190)
## Initializing your package.json file
1. Go to your terminal and create a new folder `mkdir <foldername>`
2. Navigate to your folder `cd <foldername>`
3. Initialize your project as an npm package `npm init --yes` //With the yes flag the information extracted from the current directory will be used to create a package.json file
4. Open the directory you just created in your favorite code editor
5. For fun -> print "hello world" in your terminal through the `npm run <>` command
### What is a package.json file?
source: [npm docs](https://docs.npmjs.com/getting-started/using-a-package.json)
- Lists the packages that your project depends on.
- Allows you to specify the versions of a package that your project can use using semantic versioning rules.
- Makes your build reproducible, and therefore much easier to share with other developers.


## Create your app entry point
1. Initialize an empty file called index.js in the project root folder

## Install other dependencies
1. Install [nodemon](https://www.npmjs.com/package/nodemon) as a dev dependency `npm install --save-dev nodemon`
2. Run the following command `npm install babel-preset-env babel-cli`

## Finalise the setup
1. Create a .babelrc config in your project root folder. Insert the following in the file you just created
```
{
  "presets": ["env"]
}
```
2. In package.json add this to "scripts": `"start": "nodemon --exec babel-node index.js"`
3. Now you can run in your terminal: `npm start`




# What is ES6?
[Explanation](https://medium.freecodecamp.org/want-to-learn-es6-take-this-free-23-part-course-and-become-a-javascript-ninja-55002db1ff74)

# Install a dependency
1. Go to [npm express package page](https://www.npmjs.com/package/express)
2. Install the package via the following command `npm install express --save`
3. Create .gitignore file with the following content `node_modules/`


# Server setup
In index.js
```
import express from 'express';

const PORT = 4000;
const server = express();

server.set('port', PORT);

server.listen(server.get('port'), () => {
  console.log('Server is running on port number', server.get('port'));
});

server.get('/', (request, response) => {
  response.send("App is running");
});
```

## What is a "request"?
## What is a "response"?
Let's send a success and an error
https://www.w3schools.com/js/js_es6.asp

# Let's have some fun!
1. Print a variable specified in a route by the user (google is your friend!)
2. Print the desired result of the following route: `/<number>/plus/<number>/is`
3. Convert the result of exercise 3 into cardinal numbers. For example 3 -> three, 6 -> six (use a npm package)
4. Print an error
5. Send an email to an address via the following route `/sendmail/<to>`

Read about ES6


https://en.wikipedia.org/wiki/List_of_HTTP_status_codes

Read more about servers http://ptgmedia.pearsoncmg.com/images/0130225347/samplechapter/0130225347.pdf
Revise ES6 https://medium.freecodecamp.org/want-to-learn-es6-take-this-free-23-part-course-and-become-a-javascript-ninja-55002db1ff74
For the best: https://github.com/getify/You-Dont-Know-JS
