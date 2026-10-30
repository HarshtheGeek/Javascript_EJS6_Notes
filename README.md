# Javascript_EJS6_Notes

# Table of Contents

- [History and Evolution of JavaScript](#01-history-and-evolution-of-javascript)
- [Working of JS](#02-working-of-js)
- [Client-side vs Server-side JavaScript](#03-client-side-vs-server-side-javascript)
- [Variable Declarations](#4-variable-declarations)
- [JavaScript Data Types](#5-javascript-data-types)
- [Equality Operators (== vs ===)](#6-equality-operators)


# 01 History and Evolution of JavaScript

> "Before learning **how JavaScript works**, it is important to understand **why JavaScript was created in the first place**. Understanding its history helps explain many of the design decisions, strengths, and even the quirks of the language that developers encounter today."

---

# Introduction

Today, JavaScript is one of the most widely used programming languages in the world. It powers interactive websites, backend servers, desktop applications, mobile applications, browser extensions, IoT devices, and even artificial intelligence applications.

However, JavaScript was **never designed** to perform all of these tasks.

When JavaScript was first created in **1995**, its purpose was surprisingly small:

> **Make web pages interactive without requiring communication with the server for every user action.**

To appreciate why JavaScript became so popular, we first need to understand what the internet looked like before JavaScript existed.

---

# The Web Before JavaScript

During the early 1990s, websites were nothing more than digital documents.

A browser's responsibility was extremely simple.

1. Send an HTTP request to the web server.
2. Receive an HTML document.
3. Display that HTML on the screen.

That's all.

The browser had no ability to execute logic, validate user input, update portions of a webpage, or react to user interactions.

It simply displayed whatever HTML the server returned.

Imagine visiting a webpage in 1994.

The page might contain:

- A heading
- Some paragraphs
- Images
- Links

Although users could click hyperlinks to navigate to another page, the content itself never changed dynamically.

The web was essentially a collection of connected documents.

---

# Problems with Static Websites

As websites became more popular, developers wanted users to interact with webpages.

For example, consider a registration form.

```html
<input type="email">
<button>Submit</button>
```

Suppose the user enters:

```
harshgmail.com
```

Notice that the email address is invalid because it is missing the `@` symbol. Today, the browser immediately displays an error message. However, before JavaScript existed, the browser had no way of checking whether the input was valid. Instead, the entire form was sent to the server.

The process looked like this:

1. The user clicked the **Submit** button.
2. The browser sent an HTTP request to the server.
3. The server validated the email address.
4. The server generated a completely new HTML page.
5. The browser discarded the previous webpage.
6. The browser loaded the newly generated HTML page.
7. The user finally saw the message:

```
Invalid Email Address
```

Even though the mistake was only a missing `@` symbol, the browser had to communicate with the server and reload the entire webpage.

This approach had several disadvantages.

- Slow user experience
- Increased server load
- Unnecessary network requests
- Full page refreshes even for tiny changes

The same problem existed for many common tasks.

Examples included:

- Form validation
- Image sliders
- Drop-down menus
- Navigation bars
- Calculators
- Games
- Live clocks
- Animations

Browsers simply could not perform these operations by themselves because they lacked a programming language capable of executing logic.

---

# Why HTML Was Not Enough

Many beginners assume HTML is a programming language.

It is not.

HTML is a **Markup Language**.

Its only responsibility is to describe the structure of a webpage.

For example,

```html
<h1>Hello World</h1>
```

tells the browser,

> "Display a heading."

HTML cannot make decisions.

It cannot execute loops.

It cannot perform calculations.

It cannot respond to button clicks.

Similarly, CSS was designed only for styling webpages.

CSS can define:

- Colors
- Fonts
- Layouts
- Animations
- Spacing

But CSS cannot execute business logic.

Developers therefore needed a language capable of adding behavior to webpages.

---

# The Birth of JavaScript

In 1995, the most popular browser in the world was **Netscape Navigator**.

The company behind Netscape wanted to make websites interactive.

They realized browsers needed a lightweight programming language that could execute directly inside the browser.

Netscape hired **Brendan Eich** for this task.

Surprisingly, Brendan Eich developed the first version of JavaScript in approximately **10 days**.

Because the language was created under extremely tight deadlines, several design decisions were made quickly.

Many of those early decisions still exist today and explain why JavaScript behaves differently from many modern programming languages.

---

# The First Names of JavaScript

The language was originally called

```
Mocha
```

Later it was renamed

```
LiveScript
```

Finally, it became

```
JavaScript
```

This name often confuses beginners.

---

# Why Was It Named JavaScript?

One of the biggest misconceptions among beginners is believing JavaScript is related to Java.

It is not.

The two languages are completely different.

During the mid-1990s, Java was becoming extremely popular.

Netscape wanted to take advantage of Java's popularity.

As a marketing decision, they renamed LiveScript to JavaScript.

The similarity exists only in the name.

Their syntax, runtime, philosophy, and ecosystem are completely different.

---

# JavaScript's Original Goal

JavaScript was never intended to become a general-purpose programming language.

Its original purpose was simply:

- Validate forms
- Respond to button clicks
- Display alerts
- Change webpage content
- Update HTML without refreshing the page

In short,

> **JavaScript was created to make webpages interactive.**

---

# The Browser Wars

JavaScript quickly became popular.

Microsoft wanted Internet Explorer to compete with Netscape.

Instead of adopting Netscape's implementation, Microsoft created its own version called

```
JScript
```

Now different browsers behaved differently.

The same JavaScript code could work perfectly in Netscape but fail in Internet Explorer.

Developers often had to write separate code for different browsers.

Maintaining websites became increasingly difficult.

---

# The Need for Standardization

To solve this compatibility problem, the language needed an official specification.

Rather than allowing every browser company to invent its own rules, a common standard was created.

This standard became known as

> **ECMAScript**

---

# What is ECMAScript?

Many developers incorrectly believe JavaScript and ECMAScript are the same thing.

They are not.

ECMAScript is the official specification that defines how the language should behave.

JavaScript is an implementation of that specification.

Think of it like this.

A recipe describes how a cake should be prepared.

Different bakers may prepare the cake differently, but all of them follow the same recipe.

Similarly,

- ECMAScript defines the rules.
- Chrome, Firefox, Safari, and Node.js implement those rules.

This ensures JavaScript behaves consistently across different environments.

---

# Evolution of JavaScript

## ECMAScript 1 (1997)

The first standardized version of JavaScript.

This solved many compatibility issues between browsers.

---

## ECMAScript 3 (1999)

One of the first major improvements.

It introduced several important language features such as:

- Regular Expressions
- Better String handling
- Exception Handling (`try...catch`)

For many years, ES3 became the dominant version used by developers.

---

## ECMAScript 5 (2009)

ES5 modernized JavaScript significantly.

Major additions included:

- Strict Mode
- Native JSON support
- Array methods

Examples:

```javascript
arr.forEach()
arr.map()
arr.filter()
arr.reduce()
```

These additions encouraged a cleaner and more functional programming style.

---

## ECMAScript 6 (ES2015)

ES6 is considered the biggest update in JavaScript history.

Many features developers use every day were introduced in this version.

Examples include:

- `let`
- `const`
- Arrow Functions
- Classes
- Modules
- Template Literals
- Promises
- Destructuring
- Rest Parameters
- Spread Operator
- Default Parameters

Modern JavaScript development is largely based on ES6 and later versions.

---

## Annual Releases

After ES6, JavaScript adopted yearly updates instead of waiting many years for new features.

Examples include:

- ES2016
- ES2017 (`async/await`)
- ES2018
- ES2019
- ES2020 (Optional Chaining, Nullish Coalescing, BigInt)
- ES2021
- ES2022
- ES2023
- ES2024

This allows the language to evolve continuously while maintaining backward compatibility.

---

# JavaScript Beyond the Browser

For many years, JavaScript could only run inside browsers.

Everything changed in **2009** with the release of **Node.js**.

Node.js embedded Google's **V8 JavaScript Engine** outside the browser.

This allowed JavaScript to run directly on servers.

As a result, developers could now build:

- REST APIs
- Backend servers
- Command-line applications
- Real-time applications
- Automation tools
- Microservices

JavaScript transformed from a browser scripting language into a full-stack programming language.

---

# Modern JavaScript

Today JavaScript powers almost every area of software development.

Examples include:

## Frontend Development

- React
- Angular
- Vue

---

## Backend Development

- Node.js
- Express.js
- NestJS

---

## Mobile Development

- React Native

---

## Desktop Development

- Electron

---

## Game Development

- Phaser.js
- Babylon.js

---

## Cloud & Serverless

- AWS Lambda
- Azure Functions
- Google Cloud Functions

---

JavaScript has become one of the most versatile programming languages in the world.

---

# Timeline of JavaScript

| Year | Event |
|------|-------|
| **1995** | Brendan Eich creates JavaScript in approximately 10 days |
| **1995** | Mocha → LiveScript → JavaScript |
| **1997** | ECMAScript 1 released |
| **1999** | ECMAScript 3 released |
| **2009** | ECMAScript 5 released |
| **2009** | Node.js released |
| **2015** | ECMAScript 6 (ES6) released |
| **2016+** | Annual ECMAScript releases begin |


---



# 02 Working of JS

JavaScript is a **high-level programming language**, which means it is written in a way that humans can easily understand. However, computers (specifically the CPU) cannot understand JavaScript directly. They can only execute **machine code (binary instructions)**.

To solve this problem, every browser contains a **JavaScript Engine** whose job is to translate JavaScript into machine code and execute it.

---

# Browser Architecture

A browser is not a single program. It is a collection of multiple components working together.

```
                    Browser
+--------------------------------------------------+
| User Interface                                   |
|--------------------------------------------------|
| Rendering Engine                                 |
|--------------------------------------------------|
| JavaScript Engine                                |
|--------------------------------------------------|
| Networking                                       |
|--------------------------------------------------|
| Browser APIs (DOM, Fetch, Console, etc.)         |
|--------------------------------------------------|
| Storage & Cache                                  |
+--------------------------------------------------+
```

### Different Components

### User Interface

Responsible for everything the user sees around the webpage.

Examples:

* Address bar
* Back button
* Forward button
* Refresh button
* Bookmarks

---

### Rendering Engine

Responsible for converting HTML and CSS into the webpage you actually see on your screen.

Without the rendering engine, HTML would never become a visible webpage.

---

### JavaScript Engine

Responsible for

* Reading JavaScript code
* Breaking it into tokens
* Parsing the code
* Creating an AST
* Compiling it
* Executing it
* Managing memory
* Garbage Collection
* Optimizing frequently used code

Examples:

* Chrome → V8
* Firefox → SpiderMonkey
* Safari → JavaScriptCore
* Edge → V8

---

### Networking

Responsible for downloading resources like

* HTML
* CSS
* JavaScript
* Images
* Fonts
* Videos

using HTTP/HTTPS requests.

---

### Browser APIs

These provide additional functionality that JavaScript itself does not have.

Examples

```
document

window

fetch()

console.log()

localStorage

setTimeout()

navigator
```

---

### Storage & Cache

Used to store

* Cookies
* Local Storage
* Session Storage
* Cached files

to improve website performance.

---

# What Happens When You Visit a Website?

Suppose you type

```
https://example.com
```

inside your browser.

The sequence of events is:

```
User

↓

Browser sends HTTP Request

↓

Server receives request

↓

Server returns HTML

↓

Browser receives HTML

↓

Browser starts parsing HTML
```

---

Suppose the HTML is

```html
<!DOCTYPE html>

<html>

<head>

</head>

<body>

<h1>Hello World</h1>

<script src="app.js"></script>

</body>

</html>
```

While parsing HTML, the browser encounters

```html
<script src="app.js"></script>
```

Immediately the browser understands

> "This webpage also requires a JavaScript file."

So another request is sent.

```
Browser

↓

Request app.js

↓

Server

↓

Returns app.js

↓

Browser receives JavaScript file
```

Now the browser has the JavaScript code.

---

# Why Can't the Browser Execute JavaScript Directly?

Suppose app.js contains

```javascript
let x = 10;

let y = 20;

console.log(x + y);
```

This is easy for humans to read.

However, the CPU understands only binary instructions like

```
10101010

00011010

10010101
```

Therefore JavaScript cannot be executed directly.

It first needs to be converted into machine code.

This is where the **JavaScript Engine** comes in.

---

# Role of the JavaScript Engine

The JavaScript engine acts like a translator between JavaScript code and the CPU.

```
JavaScript Source Code

↓

JavaScript Engine

↓

Machine Code

↓

CPU Executes
```

Its responsibilities include:

* Reading JavaScript source code
* Breaking it into tokens
* Checking for syntax errors
* Building an Abstract Syntax Tree (AST)
* Compiling the code
* Executing it
* Managing memory
* Performing garbage collection
* Optimizing code using Just-In-Time (JIT) compilation

---

# Different JavaScript Engines

Different browsers have different JavaScript engines.

| Browser        | Engine         |
| -------------- | -------------- |
| Chrome         | V8             |
| Microsoft Edge | V8             |
| Firefox        | SpiderMonkey   |
| Safari         | JavaScriptCore |
| Opera          | V8             |

Although the engines are different, they all implement the **ECMAScript specification**, ensuring that JavaScript behaves consistently across browsers.

---

# How the JavaScript Engine Works

The engine follows several steps before your code is executed.

```
JavaScript Code

↓

Tokenizer

↓

Tokens

↓

Parser

↓

Abstract Syntax Tree (AST)

↓

JIT Compiler

↓

Machine Code

↓

CPU Executes
```

---

# Step 1: Tokenization (Lexical Analysis)

The first step is to break the code into small units called **tokens**.

Example

```javascript
let x = 10;
```

becomes

```
LET

IDENTIFIER(x)

=

NUMBER(10)

;
```

The tokenizer doesn't understand the meaning of the program. It only separates the code into recognizable pieces.

---

# Step 2: Parsing

After tokenization, the parser checks whether the sequence of tokens follows JavaScript grammar rules.

Example

Correct code

```javascript
let age = 20;
```

Incorrect code

```javascript
let age = ;
```

The parser detects the missing value and throws a

```
SyntaxError
```

Only syntactically correct code proceeds to the next stage.

---

# Step 3: Abstract Syntax Tree (AST)

If parsing is successful, the parser creates an **Abstract Syntax Tree (AST)**.

Example

```javascript
let sum = x + y;
```

Conceptually becomes

```
VariableDeclaration

        |

Identifier(sum)

        |

BinaryExpression(+)

      /         \

     x           y
```

The AST is a tree-like representation of your program's structure, which the engine uses for further analysis and compilation.

---

# Step 4: Just-In-Time (JIT) Compilation

Modern JavaScript engines like **V8** use **Just-In-Time (JIT) compilation**.

Instead of compiling the entire program in advance, the engine:

1. Quickly prepares the code for execution.
2. Starts executing it.
3. Monitors which parts of the code run frequently.
4. Optimizes those frequently executed ("hot") sections into highly efficient machine code.

This allows JavaScript to achieve much better performance while remaining dynamic.

---

# Step 5: Execution

After compilation, the generated machine code is executed by the CPU.

At this stage:

* Variables are created.
* Memory is allocated.
* Functions are called.
* Expressions are evaluated.
* Output is produced.

Example

```javascript
let x = 10;

let y = 20;

console.log(x + y);
```

Execution

```
Allocate memory for x

↓

Store 10

↓

Allocate memory for y

↓

Store 20

↓

Calculate x + y

↓

Print 30
```
---

# Important Clarification: JavaScript vs Browser APIs

Many beginners think everything they use in JavaScript comes from the language itself. This is incorrect.

### JavaScript Language (ECMAScript)

These are features defined by the JavaScript language:

```javascript
let

const

var

if

for

while

switch

function

class

Promise
```

The JavaScript engine understands and executes these directly.

---

### Browser APIs

These are **not part of JavaScript**. They are provided by the browser and exposed to the JavaScript engine.

Examples:

```javascript
document

window

console

fetch()

alert()

setTimeout()

localStorage

navigator
```

When you write

```javascript
document.getElementById("title");
```

the JavaScript engine recognizes the syntax, but it relies on the browser to perform the actual DOM operation.

---

# 03 Client-side vs Server-side JavaScript

| Feature | Client-side JavaScript | Server-side JavaScript |
|---------|-------------------------|-------------------------|
| **Definition** | JavaScript that runs inside the user's web browser. | JavaScript that runs on a server before sending a response to the client. |
| **Execution Environment** | Browser (Chrome, Firefox, Edge, Safari, etc.) | Server runtime like **Node.js**, **Deno**, or **Bun** |
| **Purpose** | Makes web pages interactive and responsive. | Handles business logic, APIs, databases, authentication, and server operations. |
| **Executed By** | Browser's JavaScript Engine (V8, SpiderMonkey, JavaScriptCore, etc.) | Server-side JavaScript Runtime (Node.js, Deno, Bun) |
| **Access to DOM** | Yes, can manipulate HTML and CSS using the DOM. | No, there is no browser DOM on the server. |
| **Access to Browser APIs** | Yes (Local Storage, Session Storage, Geolocation, Fetch, Notifications, etc.) | No browser APIs. Has access to server APIs like File System, Process, OS, Network, etc. |
| **Database Access** | Cannot directly access databases securely. | Can connect directly to databases (MongoDB, MySQL, PostgreSQL, Redis, etc.). |
| **File System Access** | Very limited for security reasons. | Full access to the server's file system (with permissions). |
| **Visibility of Code** | Source code is downloaded and visible to users. | Source code remains hidden on the server. |
| **Security** | Less secure since users can inspect or modify the code. | More secure because code never leaves the server. |
| **Performance** | Uses the client's CPU and memory. | Uses the server's CPU and memory. |
| **Network Requests** | Sends requests to the server using Fetch or XMLHttpRequest. | Receives requests, processes them, and sends responses. |
| **Typical Tasks** | Form validation, animations, DOM manipulation, UI updates, event handling. | Authentication, authorization, CRUD operations, API development, payment processing, sending emails. |
| **Examples** | Button clicks, image sliders, dark mode, client-side validation. | Express.js APIs, login system, database queries, file uploads, JWT generation. |
| **Frameworks/Libraries** | React, Angular, Vue, Svelte, Next.js (Frontend). | Express.js, NestJS, Fastify, Hono, Koa. |

## Flow

```text
Client-side JavaScript

User
   │
   ▼
Browser
   │
Runs JavaScript
   │
Updates UI (DOM)
   │
(Optional)
   ▼
Sends API Request
````

```text
Server-side JavaScript

Browser
   │
HTTP Request
   ▼
Server (Node.js)
   │
Business Logic
   │
Database/File System
   │
HTTP Response
   ▼
Browser
```

# 4. Variable Declarations

JavaScript provides three keywords to declare variables:

- `var`
- `let`
- `const`

They differ in terms of scope, reassignment, redeclaration, and hoisting.

## 4.1 var

`var` is the older way of declaring variables in JavaScript.

### Example

```javascript
var name = "Harsh";
var age = 22;

console.log(name);
console.log(age);
```

### Characteristics

- Function-scoped.
- Can be reassigned.
- Can be redeclared within the same scope.
- Hoisted and initialized with `undefined`.
- Does not follow block scope.

### Example: Redeclaration

```javascript
var age = 22;
var age = 23;

console.log(age); // 23
```

Redeclaration is allowed with `var`.

### Example: Block Scope

```javascript
if (true) {
    var x = 10;
}

console.log(x); // 10
```

Even though `x` was declared inside the `if` block, it is accessible outside it.

This happens because `var` is not block-scoped.

---

## 4.2 let

`let` was introduced in ES6 (ECMAScript 2015).

It allows variables to be reassigned but does not allow redeclaration within the same scope.

### Example

```javascript
let name = "Harsh";

name = "Rahul";

console.log(name); // Rahul
```

### Characteristics

- Block-scoped.
- Can be reassigned.
- Cannot be redeclared in the same scope.
- Hoisted but remains in the Temporal Dead Zone (TDZ) until initialization.

### Example: Block Scope

```javascript
if (true) {
    let age = 22;
}

console.log(age); // ReferenceError
```

The variable `age` is accessible only inside the block where it was declared.

### Example: Redeclaration

```javascript
let age = 22;

// SyntaxError
let age = 23;
```

However, you can declare another variable with the same name in a different scope.

```javascript
let age = 22;

{
    let age = 23;
    console.log(age); // 23
}

console.log(age); // 22
```

---

## 4.3 const

`const` is used to declare variables whose bindings cannot be reassigned.

### Example

```javascript
const name = "Harsh";

console.log(name);
```

### Characteristics

- Block-scoped.
- Cannot be reassigned.
- Cannot be redeclared in the same scope.
- Hoisted but remains in the Temporal Dead Zone until initialization.
- Must be initialized during declaration.

### Example: Reassignment

```javascript
const age = 22;

age = 23; // TypeError
```

### Example: Initialization

```javascript
const age; // SyntaxError
```

A `const` declaration must have an initial value.

### Important: const with Objects

`const` does not make objects immutable.

It prevents reassignment of the variable binding, not modification of the object's properties.

```javascript
const user = {
    name: "Harsh",
    age: 22
};

user.age = 23;

console.log(user.age); // 23
```

This is valid.

However:

```javascript
user = {
    name: "Rahul"
}; // TypeError
```

The reference stored in `user` cannot be reassigned.

---

## 4.4 Difference Between var, let and const

| Feature | var | let | const |
|---|---|---|---|
| Scope | Function | Block | Block |
| Reassignment | Yes | Yes | No |
| Redeclaration | Yes | No | No |
| Hoisting | Yes | Yes | Yes |
| Initial Value | undefined | TDZ | TDZ |
| Must initialize | No | No | Yes |

### Which one should you use?

Recommended modern JavaScript practices:

- Use `const` by default.
- Use `let` when reassignment is required.
- Avoid `var` in modern JavaScript.

---

## 4.5 Understanding Scope

Scope determines where a variable can be accessed in your program.

JavaScript has three important types of scope.

### 1. Global Scope

Variables declared outside functions and blocks are generally accessible throughout their applicable script or module scope.

```javascript
let name = "Harsh";

function greet() {
    console.log(name);
}

greet(); // Harsh
```

### 2. Function Scope

Variables declared using `var` inside a function are accessible throughout that function.

```javascript
function test() {
    var x = 10;
    console.log(x); // 10
}

test();

console.log(x); // ReferenceError
```

### 3. Block Scope

Variables declared using `let` and `const` are accessible only within their enclosing block.

```javascript
{
    let x = 10;
    const y = 20;
}

console.log(x); // ReferenceError
console.log(y); // ReferenceError
```

### Scope Summary

| Declaration | Global | Function | Block |
|---|---|---|---|
| var | Yes* | Yes | No |
| let | Yes* | Yes | Yes |
| const | Yes* | Yes | Yes |

*Global declaration behavior depends on whether the code runs in a classic script or an ES module. Top-level declarations in modules are module-scoped.*

---

## 4.6 Understanding Hoisting

Hoisting is JavaScript's behavior of processing declarations before executing the code.

It is important to understand that hoisting does not mean JavaScript physically moves your code to the top.

### Example: var Hoisting

```javascript
console.log(age); // undefined

var age = 22;
```

Conceptually, JavaScript processes this as:

```javascript
var age;

console.log(age); // undefined

age = 22;
```

The declaration is available before its assignment.

### Example: let Hoisting

```javascript
console.log(age); // ReferenceError

let age = 22;
```

`let` is also hoisted, but it cannot be accessed before initialization.

### Example: const Hoisting

```javascript
console.log(age); // ReferenceError

const age = 22;
```

The same Temporal Dead Zone behavior applies to `const`.

### What is Temporal Dead Zone (TDZ)?

The Temporal Dead Zone is the period between entering a scope and initializing a `let` or `const` variable.

During this period, accessing the variable results in a ReferenceError.

```javascript
{
    // TDZ starts

    console.log(name); // ReferenceError

    let name = "Harsh";

    // TDZ ends
}
```

### Hoisting Summary

| Keyword | Hoisted | Initial Value | Accessible Before Declaration |
|---|---|---|---|
| var | Yes | undefined | Yes |
| let | Yes | Uninitialized | No |
| const | Yes | Uninitialized | No |

---

# 5. JavaScript Data Types

JavaScript is a dynamically typed language.

This means you do not need to explicitly specify the data type when declaring a variable.

```javascript
let value = 10;

value = "Hello";

value = true;
```

The same variable can hold values of different types during execution.

JavaScript data types are divided into two major categories:

1. Primitive Data Types
2. Non-Primitive (Reference) Data Types

---

## 5.1 Primitive Data Types

Primitive values are immutable values that are not objects.

JavaScript has seven primitive data types.

### 1. Number

Used for both integers and floating-point numbers.

```javascript
let age = 22;
let price = 99.99;

console.log(typeof age); // number
console.log(typeof price); // number
```

Special numeric values include:

```javascript
let a = Infinity;
let b = -Infinity;
let c = NaN;
```

Note: `NaN` means Not a Number, but its type is still `number`.

### 2. String

Used to represent text.

```javascript
let name = "Harsh";
let language = 'JavaScript';
let message = `Hello ${name}`;

console.log(typeof name); // string
```

Strings can be written using:

- Single quotes `' '`
- Double quotes `" "`
- Backticks `` ` ` ``

### 3. Boolean

Represents logical values.

```javascript
let isLoggedIn = true;
let isAdmin = false;

console.log(typeof isLoggedIn); // boolean
```

### 4. Undefined

A variable declared without an assigned value has the value `undefined`.

```javascript
let age;

console.log(age); // undefined
console.log(typeof age); // undefined
```

### 5. Null

Represents the intentional absence of a value.

```javascript
let user = null;

console.log(user); // null
console.log(typeof user); // object
```

Important: `typeof null` returning `"object"` is a historical JavaScript quirk.

Null is a primitive type, not a reference type.

### 6. BigInt

Used to represent integers larger than the safe integer range of Number.

```javascript
let largeNumber = 12345678901234567890n;

console.log(typeof largeNumber); // bigint
```

The `n` suffix identifies a BigInt literal.

### 7. Symbol

Used to create unique identifiers.

```javascript
let id1 = Symbol("id");
let id2 = Symbol("id");

console.log(id1 === id2); // false
console.log(typeof id1); // symbol
```

Even if two Symbols have the same description, they are unique.

---

## 5.2 Non-Primitive (Reference) Data Types

Non-primitive values are objects.

Variables holding these values contain references to objects rather than the object data itself.

Common examples include:

### 1. Object

Objects store data in key-value pairs.

```javascript
let user = {
    name: "Harsh",
    age: 22,
    role: "Engineer"
};

console.log(user.name); // Harsh
console.log(user.age); // 22
```

### 2. Array

Arrays store ordered collections of values.

```javascript
let numbers = [10, 20, 30, 40];

console.log(numbers[0]); // 10
console.log(typeof numbers); // object
```

Important: Arrays are objects in JavaScript.

To check whether a value is an array:

```javascript
console.log(Array.isArray(numbers)); // true
```

### 3. Function

Functions are reusable blocks of code.

```javascript
function greet() {
    console.log("Hello Harsh");
}

greet();

console.log(typeof greet); // function
```

Technically, functions are callable objects.

### Other Built-in Objects

- Date
- Map
- Set
- RegExp
- Error
- Promise

---

## 5.3 Primitive vs Reference Types

This is one of the most important concepts in JavaScript.

### Primitive Types

Primitive values are immutable and are copied by value.

```javascript
let a = 10;

let b = a;

b = 20;

console.log(a); // 10
console.log(b); // 20
```

Changing `b` does not affect `a`.

### Reference Types

Objects are assigned and passed by sharing their reference.

```javascript
let user1 = {
    name: "Harsh"
};

let user2 = user1;

user2.name = "Rahul";

console.log(user1.name); // Rahul
console.log(user2.name); // Rahul
```

Why?

Both variables refer to the same object.

Changing the object's property through one variable is visible through the other.

### Visual Representation

Primitive:

```text
a = 10
b = 10

a ───> 10
b ───> 10
```

Reference:

```text
user1 ───┐
         ├──> { name: "Harsh" }
user2 ───┘
```

Both variables point to the same object.

---

## 5.4 Comparing Primitive and Reference Values

### Primitive Comparison

Primitive values are compared by their values.

```javascript
let a = 10;
let b = 10;

console.log(a === b); // true
```

### Reference Comparison

Objects are compared by identity, not by their contents.

```javascript
let obj1 = {
    name: "Harsh"
};

let obj2 = {
    name: "Harsh"
};

console.log(obj1 === obj2); // false
```

Although both objects contain identical properties, they are two different objects.

### Same Reference Comparison

```javascript
let obj1 = {
    name: "Harsh"
};

let obj2 = obj1;

console.log(obj1 === obj2); // true
```

Both variables reference the same object.

---

## 5.5 Mutability

### Primitive Values Are Immutable

```javascript
let name = "Harsh";

name.toUpperCase();

console.log(name); // Harsh
```

Strings are immutable. `toUpperCase()` returns a new string rather than modifying the original.

```javascript
name = name.toUpperCase();

console.log(name); // HARSH
```

### Objects Are Mutable

```javascript
let user = {
    name: "Harsh",
    age: 22
};

user.age = 23;

console.log(user.age); // 23
```

Object properties can be modified without creating a new object.

---

## 5.6 typeof Operator

The `typeof` operator returns a string indicating the type of a value.

```javascript
console.log(typeof 10);           // number
console.log(typeof "Hello");      // string
console.log(typeof true);         // boolean
console.log(typeof undefined);    // undefined
console.log(typeof 10n);          // bigint
console.log(typeof Symbol());     // symbol
console.log(typeof {});           // object
console.log(typeof []);           // object
console.log(typeof null);         // object
console.log(typeof function(){}); // function
```

Remember these important exceptions:

| Expression | Result |
|---|---|
| typeof null | "object" |
| typeof [] | "object" |
| typeof {} | "object" |
| typeof function() {} | "function" |
| typeof NaN | "number" |

---

# 06 Equality Operators (== vs ===)

> "JavaScript provides two equality operators, `==` and `===`. Understanding the difference is important because one performs type coercion when necessary, while the other compares values without type conversion."

### 1. Loose Equality (`==`)

- Compares two values after performing type coercion when necessary.
- JavaScript automatically converts types before comparison.

```js
console.log(10 == "10");  // true
console.log(true == 1);   // true
console.log(null == undefined); // true
```

### 2. Strict Equality (`===`)

- Compares both value and data type.
- Does not perform type coercion.
- Returns `true` only when both operands have the same type and equal values.

```js
console.log(10 === "10"); // false
console.log(true === 1);  // false
console.log(null === undefined); // false
```

### 3. Important Exception: NaN

- `NaN` (Not-a-Number) is not equal to itself.
- Both `==` and `===` return `false` when comparing `NaN` with itself.
- Use `Number.isNaN()` to check whether a value is `NaN`.

```js
console.log(NaN == NaN);  // false
console.log(NaN === NaN); // false

console.log(Number.isNaN(NaN)); // true
```

### 4. Best Practice

- Prefer `===` over `==` to avoid unexpected type coercion.








