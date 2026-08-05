# Javascript_EJS6_Notes

# Table of Contents

- [Introduction](#History-and-Evolution-of-JavaScript)
- [Working of JS](#Working-of-JS)





# 01 - History and Evolution of JavaScript

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



# 2. Working of JS

JavaScript is a **high-level programming language**, which means it is written in a way that humans can easily understand. However, computers (specifically the CPU) cannot understand JavaScript directly. They can only execute **machine code (binary instructions)**.

To solve this problem, every browser contains a **JavaScript Engine** whose job is to translate JavaScript into machine code and execute it.

---

# 2. Browser Architecture

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

# 3. What Happens When You Visit a Website?

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

# 4. Why Can't the Browser Execute JavaScript Directly?

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

# 5. Role of the JavaScript Engine

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

# 6. Different JavaScript Engines

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

# 7. How the JavaScript Engine Works

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

# 8. Important Clarification: JavaScript vs Browser APIs

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

# 10. Key Takeaways

* JavaScript is a high-level language and cannot be executed directly by the CPU.
* Every browser includes a JavaScript engine to translate JavaScript into machine code.
* Different browsers use different JavaScript engines (V8, SpiderMonkey, JavaScriptCore), but all follow the ECMAScript specification.
* Before execution, JavaScript goes through several stages: **Tokenization → Parsing → AST Creation → JIT Compilation → Execution**.
* The JavaScript engine is responsible for parsing, compiling, executing, memory management, and optimization.
* Features such as `document`, `window`, `fetch()`, `console`, and `setTimeout()` are **Browser APIs**, not part of the JavaScript language itself.

---



