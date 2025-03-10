# 🏁 1.1 Introduction to JavaScript


## ✅ What is JavaScript?
JavaScript is a versatile, high-level programming language primarily used for web development. It enables interactive and dynamic content on websites, such as animations, form validations, and real-time updates.



## ✅ History of JavaScript
- **1995**: Created by **Brendan Eich** at Netscape.
- **Initially called Mocha**, later renamed to LiveScript, and finally JavaScript.
- **1996**: Microsoft introduced JScript.
- **1997**: Standardized as **ECMAScript (ES)**.
- **2015 (ES6)**: Major update introducing modern features like `let`, `const`, arrow functions, and classes.
- **Ongoing updates**: JavaScript continues to evolve with new ECMAScript versions.



## ✅ How JavaScript Works?
1. **Interpreted Language**: Executed line-by-line by the JavaScript engine.
2. **Single-threaded & Non-blocking**: Uses an **event loop** and asynchronous programming.
3. **Client-side & Server-side**: Runs in browsers (frontend) and on servers (backend with Node.js).
4. **Dynamically Typed**: No need to declare variable types explicitly.




## ✅ Running JavaScript
### 📌 Browser
- JavaScript runs natively in web browsers using the **JavaScript Engine** (e.g., V8 in Chrome, SpiderMonkey in Firefox).
- Can be executed inside `<script>` tags in HTML files.
- Example:

  ```html
  <script>
    console.log("Hello, JavaScript!");
  </script>
  ```



### 🖥️ Node.js
- Node.js is a runtime that allows JavaScript to run outside the browser.
- Uses the **V8 engine** and provides additional APIs for file system, networking, etc.
- Run JavaScript files using:
  ```sh
  node script.js
  