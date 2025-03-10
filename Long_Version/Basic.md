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
  

## 🎯 **1.2 Variables & Data Types**  


### 🔹 `var`, `let`, `const`  
JavaScript provides three ways to declare variables:

- **`var`**: Function-scoped, can be redeclared, and hoisted.
- **`let`**: Block-scoped, cannot be redeclared, but can be updated.
- **`const`**: Block-scoped, cannot be redeclared or updated.


Example:
```js
var x = 10;  // Function-scoped
let y = 20;  // Block-scoped
const z = 30; // Block-scoped, immutable
```


### 🔹 Primitive vs Reference Data Types  
JavaScript has two main categories of data types:


#### 📌 **Primitive Data Types**
These are immutable and stored directly in memory:
- **Number**: `let num = 42;`
- **String**: `let str = "Hello";`
- **Boolean**: `let isTrue = true;`
- **Undefined**: `let u;`
- **Null**: `let n = null;`
- **Symbol**: `let sym = Symbol("unique");`


#### 📌 **Reference Data Types**
These are mutable and stored as references:
- **Object**: `let obj = { name: "John" };`
- **Array**: `let arr = [1, 2, 3];`
- **Function**: `function greet() { console.log("Hello"); }`


Example:
```js
let person = { name: "Alice" };
let numbers = [1, 2, 3, 4];
function sayHello() {
  console.log("Hello!");
}
```

### ✨ **1.3 Operators in JavaScript**  

Operators in JavaScript are symbols that perform operations on values and variables. They can be categorized into different types based on their functionality.  

---

#### ➕ **1.3.1 Arithmetic Operators**  
Arithmetic operators perform basic mathematical operations:  

| Operator | Description  | Example  | Result  |
|----------|-------------|----------|---------|
| `+`      | Addition    | `5 + 3`  | `8`     |
| `-`      | Subtraction | `5 - 3`  | `2`     |
| `*`      | Multiplication | `5 * 3`  | `15`    |
| `/`      | Division    | `5 / 2`  | `2.5`   |
| `%`      | Modulus (Remainder) | `5 % 2`  | `1`     |

---

#### 📝 **1.3.2 Assignment Operators**  
Assignment operators assign values to variables.  

| Operator | Example | Equivalent To |
|----------|---------|---------------|
| `=`      | `x = 5`  | `x = 5`      |
| `+=`     | `x += 3` | `x = x + 3`  |
| `-=`     | `x -= 2` | `x = x - 2`  |
| `*=`     | `x *= 4` | `x = x * 4`  |
| `/=`     | `x /= 2` | `x = x / 2`  |
| `%=`     | `x %= 3` | `x = x % 3`  |

---

#### ⚖️ **1.3.3 Comparison Operators**  
Comparison operators compare two values and return `true` or `false`.  

| Operator | Description | Example | Result |
|----------|-------------|---------|--------|
| `==`     | Equal (loose) | `5 == "5"`  | `true`  |
| `===`    | Strictly Equal | `5 === "5"` | `false` |
| `!=`     | Not Equal | `5 != "5"` | `false` |
| `!==`    | Strictly Not Equal | `5 !== "5"` | `true`  |
| `>`      | Greater Than | `5 > 3` | `true`  |
| `<`      | Less Than | `5 < 3` | `false` |
| `>=`     | Greater Than or Equal | `5 >= 5` | `true`  |
| `<=`     | Less Than or Equal | `5 <= 3` | `false` |

---

#### 🔀 **1.3.4 Logical Operators**  
Logical operators are used to combine multiple conditions.  

| Operator | Description | Example | Result |
|----------|-------------|---------|--------|
| `&&`     | Logical AND | `(5 > 3) && (8 > 5)` | `true`  |
| `||`     | Logical OR | `(5 > 3) || (8 < 5)` | `true`  |
| `!`      | Logical NOT | `!(5 > 3)` | `false` |

---

### 🔄 **1.4 Conditional Statements in JavaScript**  

Conditional statements allow you to execute different blocks of code based on certain conditions. JavaScript provides several ways to handle conditions.  

---

## 📌 **1.4.1 `if`, `else`, `else if` Statements**  
These statements execute different code blocks depending on whether a condition is `true` or `false`.  

### ✅ **`if` Statement**  
The `if` statement executes a block of code **only if** a specified condition is `true`.  

#### **Syntax:**  
```javascript
if (condition) {
    // Code to execute if the condition is true
}
```
#### **Example:**  
```javascript
let age = 20;

if (age >= 18) {
    console.log("You are an adult.");
}
```
✔ If `age >= 18`, the message **"You are an adult."** is displayed.  
✖ If `age < 18`, nothing happens.  

---

### 🔀 **`if...else` Statement**  
The `if...else` statement provides an **alternative block** to execute if the condition is `false`.  

#### **Syntax:**  
```javascript
if (condition) {
    // Code if condition is true
} else {
    // Code if condition is false
}
```
#### **Example:**  
```javascript
let age = 16;

if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```
✔ If `age >= 18`, it prints **"You are an adult."**  
✔ If `age < 18`, it prints **"You are a minor."**  

---

### 🔄 **`if...else if...else` Statement**  
The `else if` statement checks **multiple conditions** in sequence.  

#### **Syntax:**  
```javascript
if (condition1) {
    // Code if condition1 is true
} else if (condition2) {
    // Code if condition2 is true
} else {
    // Code if none of the above conditions are true
}
```
#### **Example:**  
```javascript
let score = 85;

if (score >= 90) {
    console.log("Grade: A");
} else if (score >= 80) {
    console.log("Grade: B");
} else if (score >= 70) {
    console.log("Grade: C");
} else {
    console.log("Grade: F");
}
```
✔ If `score >= 90`, it prints **"Grade: A"**  
✔ If `score >= 80` but `< 90`, it prints **"Grade: B"**  
✔ If `score >= 70` but `< 80`, it prints **"Grade: C"**  
✔ If none of the conditions match, it prints **"Grade: F"**  

---

#### ❓ **1.4.2 Ternary Operator**  
The ternary operator is a shorthand for `if-else` statements.  

##### **Syntax:**  
```javascript
condition ? value_if_true : value_if_false;
```
##### **Example:**  
```javascript
let age = 18;
let status = (age >= 18) ? "Adult" : "Minor";
console.log(status); // Output: "Adult"
```
- If `age >= 18` is `true`, it returns `"Adult"`.  
- If `age >= 18` is `false`, it returns `"Minor"`.  

---

## 📌 **1.4.3 `switch` Statement**  
The `switch` statement is an alternative to multiple `if...else if` conditions. It compares a value against multiple **cases** and executes the matching case.  

#### **Syntax:**  
```javascript
switch (expression) {
    case value1:
        // Code to execute if expression === value1
        break;
    case value2:
        // Code to execute if expression === value2
        break;
    default:
        // Code to execute if no case matches
}
```
#### **Example:**  
```javascript
let day = "Monday";

switch (day) {
    case "Monday":
        console.log("Start of the workweek.");
        break;
    case "Friday":
        console.log("Weekend is near!");
        break;
    case "Saturday":
    case "Sunday":
        console.log("It's the weekend!");
        break;
    default:
        console.log("A regular weekday.");
}
```
✔ If `day` is `"Monday"`, it prints **"Start of the workweek."**  
✔ If `day` is `"Friday"`, it prints **"Weekend is near!"**  
✔ If `day` is `"Saturday"` or `"Sunday"`, it prints **"It's the weekend!"**  
✔ If `day` is any other value, it prints **"A regular weekday."**  

---

### 🔹 **Key Differences Between `if...else` and `switch`**  
| Feature  | `if...else` | `switch` |
|----------|------------|----------|
| Condition Type | Works with **any** condition | Works with **strict equality (`===`)** |
| Readability | Best for **range-based** conditions | Best for **fixed values** |
| Performance | Can be **slower** with many conditions | Can be **faster** with many fixed cases |

---


### 🔄 **1.5 Loops in JavaScript**  

Loops allow you to execute a block of code multiple times based on a condition. JavaScript provides different types of loops to handle various iteration scenarios.  

---

## 🔃 **1.5.1 `for` Loop**  
The `for` loop is used when the number of iterations is known beforehand.  

#### **Syntax:**  
```javascript
for (initialization; condition; update) {
    // Code to execute in each iteration
}
```
#### **Example:**  
```javascript
for (let i = 1; i <= 5; i++) {
    console.log("Iteration", i);
}
```
✔ Prints numbers from `1` to `5`.  
✔ The loop starts at `i = 1`, runs while `i <= 5`, and increments `i` in each iteration.  

---

## 🔄 **1.5.2 `while` Loop**  
The `while` loop is used when the number of iterations is **unknown** and depends on a condition.  

#### **Syntax:**  
```javascript
while (condition) {
    // Code to execute as long as condition is true
}
```
#### **Example:**  
```javascript
let count = 1;
while (count <= 5) {
    console.log("Count:", count);
    count++;
}
```
✔ Runs until `count` is greater than `5`.  
✔ Use when you **don't know in advance** how many times the loop should run.  

---

## ♻ **1.5.3 `do...while` Loop**  
The `do...while` loop is similar to `while`, but it executes **at least once**, even if the condition is `false`.  

#### **Syntax:**  
```javascript
do {
    // Code executes at least once
} while (condition);
```
#### **Example:**  
```javascript
let num = 1;
do {
    console.log("Number:", num);
    num++;
} while (num <= 5);
```
✔ Executes the block **at least once**, even if `num` is already greater than `5`.  

---

## 📚 **1.5.4 `for...in` Loop**  
The `for...in` loop is used to iterate over the **keys** (properties) of an object.  

#### **Syntax:**  
```javascript
for (let key in object) {
    // Code to execute for each property
}
```
#### **Example:**  
```javascript
let user = { name: "Alice", age: 25, city: "New York" };

for (let key in user) {
    console.log(key + ": " + user[key]);
}
```
✔ Iterates over object properties (`name`, `age`, `city`).  
✔ Prints **both the keys and their corresponding values**.  

---

## 📝 **1.5.5 `for...of` Loop**  
The `for...of` loop is used to iterate over **iterable objects** like arrays, strings, or sets.  

#### **Syntax:**  
```javascript
for (let item of iterable) {
    // Code to execute for each item
}
```
#### **Example:**  
```javascript
let colors = ["red", "green", "blue"];

for (let color of colors) {
    console.log(color);
}
```
✔ Iterates over array elements (`"red"`, `"green"`, `"blue"`).  
✔ Works with arrays, strings, maps, and sets.  

---

### 🔹 **Key Differences Between Loops**  
| Loop Type  | Use Case | Works With |
|-----------|------------|------------|
| `for` | When the number of iterations is known | Any iterable (array, string, etc.) |
| `while` | When the condition determines execution | Any logic-based condition |
| `do...while` | Ensures execution at least once | Any logic-based condition |
| `for...in` | Iterates over object properties | Objects |
| `for...of` | Iterates over values in iterables | Arrays, strings, maps, sets |

---