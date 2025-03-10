### 🎭 **3.3 JavaScript Design Patterns**  

Design patterns are reusable solutions to common programming problems. They improve **code structure, maintainability, and scalability**. Below are three fundamental design patterns in JavaScript.  

---

## 🛠 **3.3.1 Module Pattern**  
The **Module Pattern** encapsulates variables and functions within a private scope, exposing only necessary methods.

#### **Syntax:**  
```javascript
const Module = (function () {
    let privateVar = "I am private";
    function privateMethod() {
        return "This is a private method";
    }
    return {
        publicMethod: function () {
            return `Accessing: ${privateVar}`;
        }
    };
})();
console.log(Module.publicMethod()); // Output: Accessing: I am private
console.log(Module.privateVar); // ❌ Undefined (private scope)
```
✔ Prevents **global namespace pollution**.  
✔ Supports **data encapsulation**.

---

## 🌈 **3.3.2 Factory Pattern**  
The **Factory Pattern** creates objects without using a `class`, making object creation more dynamic.

#### **Syntax:**  
```javascript
function createPerson(name, age) {
    return {
        name,
        age,
        greet() {
            return `Hello, my name is ${this.name}.`;
        }
    };
}
const person1 = createPerson("Alice", 25);
console.log(person1.greet()); // Output: Hello, my name is Alice.
```
✔ Useful when object creation logic is **repetitive**.  
✔ Provides **flexibility** for object creation.

---

## 🏡 **3.3.3 Singleton Pattern**  
The **Singleton Pattern** ensures only **one instance** of an object exists.

#### **Syntax:**  
```javascript
const Singleton = (function () {
    let instance;
    function createInstance() {
        return { message: "I am the only instance" };
    }
    return {
        getInstance: function () {
            if (!instance) {
                instance = createInstance();
            }
            return instance;
        }
    };
})();
const singleA = Singleton.getInstance();
const singleB = Singleton.getInstance();
console.log(singleA === singleB); // Output: true (same instance)
```
✔ Prevents **multiple instances** of an object.  
✔ Useful for **global state management** (e.g., database connections).

---

Using design patterns in JavaScript enhances code **organization, efficiency, and maintainability**. Master these patterns to write scalable applications! 🚀