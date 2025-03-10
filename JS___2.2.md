### 🏷 **2.2 Objects & Properties in JavaScript**  

Objects in JavaScript are **collections of key-value pairs** used to store structured data. They support powerful methods for manipulation and retrieval.  

---

## 🛠 **2.2.1 Object Literals**  
An **object literal** is the simplest way to create an object using curly braces `{}`.  

#### **Syntax:**  
```javascript
const objectName = {
    key1: value1,
    key2: value2,
    key3: value3
};
```

#### **Example:**  
```javascript
const person = {
    name: "Alice",
    age: 25,
    city: "New York"
};
console.log(person.name); // Output: Alice
```
✔ Defines an object with **key-value pairs**.  
✔ Allows easy data grouping.  

---

## 🔧 **2.2.2 Object Methods**  
Objects can have methods (functions stored inside them).  

#### **Syntax:**  
```javascript
const objectName = {
    methodName() {
        // method body
    }
};
```

#### **Example:**  
```javascript
const person = {
    name: "Bob",
    greet() {
        return `Hello, my name is ${this.name}`;
    }
};
console.log(person.greet()); // Output: Hello, my name is Bob
```
✔ Methods are functions stored in objects.  
✔ `this` refers to the object itself.  

---

## 🛠 **2.2.3 Object Destructuring**  
Destructuring **extracts properties** from an object into variables.  

#### **Syntax:**  
```javascript
const { key1, key2 } = objectName;
```

#### **Example:**  
```javascript
const user = { name: "Charlie", age: 30 };
const { name, age } = user;
console.log(name); // Output: Charlie
console.log(age);  // Output: 30
```
✔ Simplifies **property extraction**.  
✔ Avoids repetitive `user.name`, `user.age`.  

---

## 🔹 **2.2.4 Useful Object Methods**  

### ✅ `Object.keys()` – Returns an array of keys.  
#### **Syntax:**  
```javascript
Object.keys(objectName);
```
#### **Example:**  
```javascript
const user = { name: "Eve", age: 28 };
console.log(Object.keys(user)); // Output: ["name", "age"]
```

### ✅ `Object.values()` – Returns an array of values.  
#### **Syntax:**  
```javascript
Object.values(objectName);
```
#### **Example:**  
```javascript
console.log(Object.values(user)); // Output: ["Eve", 28]
```

### ✅ `Object.entries()` – Returns key-value pairs as arrays.  
#### **Syntax:**  
```javascript
Object.entries(objectName);
```
#### **Example:**  
```javascript
console.log(Object.entries(user)); 
// Output: [["name", "Eve"], ["age", 28]]
```
✔ Great for **looping over objects**.  
✔ Converts objects into **iterable arrays**.  

---

Objects are **fundamental** in JavaScript for storing and managing data efficiently. Let me know if you need more details! 🚀