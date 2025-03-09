### 🛠 **1.6 Functions in JavaScript**  

Functions are reusable blocks of code that help in organizing and structuring JavaScript programs efficiently. There are different ways to define functions, each with unique features.  

---

## 🎯 **1.6.1 Function Declaration vs Function Expression**  
Functions can be defined using **declarations** or **expressions**.  

### ✅ **Function Declaration**  
A function declaration defines a named function that can be **hoisted**, meaning it can be called before its definition in the code.  

#### **Syntax:**  
```javascript
function greet(name) {
    return `Hello, ${name}!`;
}
```
#### **Example:**  
```javascript
console.log(greet("Alice")); // Output: Hello, Alice!
```
✔ **Hoisted**: Can be used before declaration.  
✔ Ideal for defining functions that are used multiple times.  

---

### ⚡ **Function Expression**  
A function expression stores a function inside a variable. Unlike declarations, function expressions are **not hoisted**.  

#### **Syntax:**  
```javascript
const greet = function(name) {
    return `Hello, ${name}!`;
};
```
#### **Example:**  
```javascript
console.log(greet("Bob")); // Output: Hello, Bob!
```
✔ **Not hoisted**: Cannot be called before definition.  
✔ Useful for **anonymous functions** and callbacks.  

---

## 🔋 **1.6.2 Arrow Functions (`=>`)**  
Arrow functions provide a **shorter syntax** for function expressions and **lexical `this` binding**.  

#### **Syntax:**  
```javascript
const functionName = (parameters) => expression;
```
#### **Example:**  
```javascript
const add = (a, b) => a + b;
console.log(add(5, 3)); // Output: 8
```
✔ **Concise**: No `return` needed for single-line expressions.  
✔ **`this` behavior**: Inherits `this` from its surrounding scope.  

### **Multi-line Arrow Function**  
For multiple statements, use curly braces `{}` and an explicit `return`.  
```javascript
const multiply = (a, b) => {
    let result = a * b;
    return result;
};
```

---

## 🔹 **1.6.3 Default Parameters**  
Default parameters allow setting a **fallback value** if an argument is not provided.  

#### **Syntax:**  
```javascript
function greet(name = "Guest") {
    return `Hello, ${name}!`;
}
```
#### **Example:**  
```javascript
console.log(greet()); // Output: Hello, Guest!
console.log(greet("Charlie")); // Output: Hello, Charlie!
```
✔ Avoids `undefined` when arguments are missing.  
✔ Simplifies function calls.  

---

## 📌 **1.6.4 Rest & Spread Operator (`...`)**  
The **rest (`...`)** and **spread (`...`)** operators enhance function flexibility by handling multiple arguments.  

### **Rest Operator (`...`)**  
The rest operator collects multiple values into an array.  

#### **Syntax:**  
```javascript
function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}
```
#### **Example:**  
```javascript
console.log(sum(1, 2, 3, 4)); // Output: 10
```
✔ Combines multiple values into a single array.  
✔ Useful for handling **unknown numbers of arguments**.  

### **Spread Operator (`...`)**  
The spread operator expands an array into individual elements.  

#### **Syntax:**  
```javascript
const numbers = [1, 2, 3];
console.log(Math.max(...numbers));
```
#### **Example:**  
```javascript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const merged = [...arr1, ...arr2];
console.log(merged); // Output: [1, 2, 3, 4, 5, 6]
```
✔ Expands arrays or objects into individual elements.  
✔ Used for copying or merging data efficiently.  

---

### 🔧 **Key Differences Between Function Types**  
| Function Type | Hoisted? | `this` Behavior | Syntax |
|--------------|---------|---------------|--------|
| Function Declaration | ✅ Yes | Standard | `function func() {}` |
| Function Expression | ❌ No | Standard | `const func = function() {}` |
| Arrow Function (`=>`) | ❌ No | Lexical (`this` inherited) | `const func = () => {}` |

---

Functions are a core part of JavaScript, allowing for **code reusability** and **modular programming**. Let me know if you need further explanations! 🚀
