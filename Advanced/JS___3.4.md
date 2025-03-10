### 🎯 **3.4 Functional Programming Concepts**  

Functional programming (FP) is a programming paradigm based on **pure functions, immutability, and first-class functions**. It enhances code **readability, reusability, and testability**.

---

## 🔹 **3.4.1 Higher-Order Functions**  
A **higher-order function** is a function that **takes another function as an argument or returns a function**.

#### **Syntax:**  
```javascript
function higherOrderFunction(callback) {
    return callback();
}
```
#### **Example:**  
```javascript
function greet(name) {
    return `Hello, ${name}!`;
}
function processUser(callback, userName) {
    return callback(userName);
}
console.log(processUser(greet, "Alice")); // Output: Hello, Alice!
```
✔ Enhances **code modularity and flexibility**.  
✔ Used in **`map()`, `filter()`, `reduce()`**, etc.  

---

## 🔹 **3.4.2 Pure Functions**  
A **pure function** produces the same output for the same input **without side effects**.

#### **Syntax:**  
```javascript
function pureFunction(a, b) {
    return a + b;
}
```
#### **Example:**  
```javascript
function add(a, b) {
    return a + b;
}
console.log(add(2, 3)); // Output: 5
console.log(add(2, 3)); // Output: 5 (always the same output)
```
✔ No modification of external variables.  
✔ Easy to **test and debug**.  

---

## 🔹 **3.4.3 First-Class Functions**  
JavaScript treats **functions as values**, allowing assignment, passing, and returning from other functions.

#### **Syntax:**  
```javascript
const functionVariable = function() {
    return "I am a function stored in a variable!";
};
```
#### **Example:**  
```javascript
const sayHello = function(name) {
    return `Hello, ${name}!`;
};
console.log(sayHello("Bob")); // Output: Hello, Bob!
```
✔ Functions can be **stored, passed, and returned dynamically**.  
✔ Enables **higher-order functions and callbacks**.  

---

## 🔹 **3.4.4 Currying**  
Currying transforms a function with multiple parameters into a sequence of **nested functions**.

#### **Syntax:**  
```javascript
function curryFunction(a) {
    return function(b) {
        return a + b;
    };
}
```
#### **Example:**  
```javascript
const multiply = (a) => (b) => a * b;
const double = multiply(2);
console.log(double(5)); // Output: 10
```
✔ Allows **partial application of functions**.  
✔ Useful for **function composition**.  

---

Mastering **functional programming** improves code maintainability, reduces side effects, and enhances efficiency in JavaScript applications! 🚀
