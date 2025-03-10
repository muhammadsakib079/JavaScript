### 🚀 **2.3 ES6+ Features (Modern JavaScript)**  

ES6 and later versions introduced powerful features that improve code readability, maintainability, and performance. Below are some key modern JavaScript features:  

---

## 📌 **2.3.1 Template Literals**  
Template literals allow **string interpolation** using backticks (`` ` ``) instead of quotes.  

#### **Syntax:**  
```javascript
`String text ${expression} more text`
```

#### **Example:**  
```javascript
const name = "Alice";
console.log(`Hello, ${name}!`); // Output: Hello, Alice!
```
✔ Enables multi-line strings.  
✔ Supports embedded expressions.  

---

## 🛠 **2.3.2 Destructuring Assignment**  
Destructuring simplifies extracting values from arrays and objects.  

#### **Syntax (Object Destructuring):**  
```javascript
const { key1, key2 } = objectName;
```
#### **Example:**  
```javascript
const user = { name: "Bob", age: 30 };
const { name, age } = user;
console.log(name); // Output: Bob
console.log(age); // Output: 30
```
✔ Extracts properties into variables efficiently.  
✔ Avoids repetitive object references.  

#### **Syntax (Array Destructuring):**  
```javascript
const [var1, var2] = arrayName;
```
#### **Example:**  
```javascript
const numbers = [10, 20, 30];
const [first, second] = numbers;
console.log(first);  // Output: 10
console.log(second); // Output: 20
```
✔ Simplifies working with arrays.  

---

## 🔧 **2.3.3 Default Function Parameters**  
Set default values for function parameters.  

#### **Syntax:**  
```javascript
function functionName(param1 = defaultValue) {
    // Function body
}
```
#### **Example:**  
```javascript
function greet(name = "Guest") {
    return `Hello, ${name}!`;
}
console.log(greet());      // Output: Hello, Guest!
console.log(greet("Eve")); // Output: Hello, Eve!
```
✔ Prevents `undefined` values in functions.  
✔ Enhances function flexibility.  

---

## 🛠 **2.3.4 Rest & Spread Operator (`...`)**  
The **rest operator** collects multiple values into an array, while the **spread operator** expands iterable elements.  

### ✅ **Rest Operator (`...`)**  
#### **Syntax:**  
```javascript
function functionName(...restParams) {
    // Function body
}
```
#### **Example:**  
```javascript
function sum(...numbers) {
    return numbers.reduce((acc, num) => acc + num, 0);
}
console.log(sum(1, 2, 3, 4)); // Output: 10
```
✔ Gathers multiple arguments into an array.  

### ✅ **Spread Operator (`...`)**  
#### **Syntax:**  
```javascript
const newArray = [...existingArray];
const newObject = { ...existingObject };
```
#### **Example:**  
```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];
console.log(arr2); // Output: [1, 2, 3, 4, 5]
```
✔ Easily copies or merges arrays and objects.  
✔ Avoids mutation of original data.  

---

## 🌐 **2.3.5 Modules (`import/export`)**  
ES6 modules allow splitting code into reusable files.  

### ✅ **Exporting a Module**  
#### **Syntax:**  
```javascript
export const variableName = value;
export function functionName() {}
export default function functionName() {}
```
#### **Example:**  
```javascript
export const pi = 3.1415;
export function greet() {
    return "Hello!";
}
```

### ✅ **Importing a Module**  
#### **Syntax:**  
```javascript
import { variableName, functionName } from './moduleFile';
import defaultFunction from './moduleFile';
```
#### **Example:**  
```javascript
import { pi, greet } from './mathUtils.js';
console.log(pi);     // Output: 3.1415
console.log(greet()); // Output: Hello!
```
✔ Encourages **code reusability** and maintainability.  
✔ Supports **named and default exports**.  

---

Modern JavaScript (ES6+) improves code **clarity, efficiency, and maintainability**. Mastering these features helps write cleaner and more powerful JavaScript! 🚀