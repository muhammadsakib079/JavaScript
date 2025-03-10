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