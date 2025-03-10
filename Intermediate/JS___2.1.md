### 🗂️ **2.1 Array Methods in JavaScript**  

Arrays in JavaScript come with powerful built-in methods that help in processing, modifying, and iterating through data efficiently. Here are the most commonly used array methods.  

---

## 📌 **2.1.1 Transforming Arrays**  
These methods create new arrays by transforming elements.

### ✅ `map()` – Creates a new array by applying a function to each element.  
#### **Example:**  
```javascript
const numbers = [1, 2, 3];
const squared = numbers.map(num => num * num);
console.log(squared); // Output: [1, 4, 9]
```
✔ Returns a new array.  
✔ Useful for modifying data while keeping the original array intact.  

### ✅ `filter()` – Creates a new array with elements that pass a condition.  
#### **Example:**  
```javascript
const numbers = [1, 2, 3, 4, 5];
const evens = numbers.filter(num => num % 2 === 0);
console.log(evens); // Output: [2, 4]
```
✔ Returns a new array.  
✔ Useful for **removing unwanted elements**.  

### ✅ `reduce()` – Accumulates values into a single result.  
#### **Example:**  
```javascript
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // Output: 10
```
✔ Reduces an array into a **single value**.  
✔ Used for calculations like sums, averages, and complex operations.  

---

## 🔄 **2.1.2 Iterating Over Arrays**  
These methods loop through arrays without modifying them.

### ✅ `forEach()` – Executes a function for each element (does not return a new array).  
#### **Example:**  
```javascript
const names = ["Alice", "Bob", "Charlie"];
names.forEach(name => console.log(name));
```
✔ Does not return a new array.  
✔ Useful for **logging, modifying elements in place**.  

### ✅ `find()` – Returns the first element that matches a condition.  
#### **Example:**  
```javascript
const numbers = [5, 10, 15, 20];
const firstLarge = numbers.find(num => num > 10);
console.log(firstLarge); // Output: 15
```
✔ Returns **only one element** (the first match).  
✔ Use when you **need a single result**.  

### ✅ `some()` – Checks if **at least one** element matches a condition.  
#### **Example:**  
```javascript
const numbers = [1, 3, 5, 8];
const hasEven = numbers.some(num => num % 2 === 0);
console.log(hasEven); // Output: true
```
✔ Returns `true` or `false`.  
✔ Stops checking after the first match.  

### ✅ `every()` – Checks if **all** elements match a condition.  
#### **Example:**  
```javascript
const numbers = [2, 4, 6];
const allEven = numbers.every(num => num % 2 === 0);
console.log(allEven); // Output: true
```
✔ Returns `true` or `false`.  
✔ Useful when checking all values against a condition.  

---

## 📝 **2.1.3 Modifying Arrays**  
These methods **change the original array**.

### ✅ `push()` – Adds elements to the **end** of an array.  
#### **Example:**  
```javascript
const fruits = ["apple", "banana"];
fruits.push("orange");
console.log(fruits); // Output: ["apple", "banana", "orange"]
```
✔ Modifies the original array.  
✔ Returns the new length of the array.  

### ✅ `pop()` – Removes the **last** element from an array.  
#### **Example:**  
```javascript
const fruits = ["apple", "banana", "orange"];
fruits.pop();
console.log(fruits); // Output: ["apple", "banana"]
```
✔ Modifies the original array.  
✔ Returns the removed element.  

### ✅ `shift()` – Removes the **first** element from an array.  
#### **Example:**  
```javascript
const fruits = ["apple", "banana", "orange"];
fruits.shift();
console.log(fruits); // Output: ["banana", "orange"]
```
✔ Modifies the original array.  
✔ Returns the removed element.  

### ✅ `unshift()` – Adds elements to the **beginning** of an array.  
#### **Example:**  
```javascript
const fruits = ["banana", "orange"];
fruits.unshift("apple");
console.log(fruits); // Output: ["apple", "banana", "orange"]
```
✔ Modifies the original array.  
✔ Returns the new length of the array.  

---

## 🔧 **2.1.4 Extracting and Merging Arrays**  

### ✅ `slice()` – Extracts a section of an array **without modifying** it.  
#### **Example:**  
```javascript
const numbers = [0, 1, 2, 3, 4, 5];
const sliced = numbers.slice(1, 4);
console.log(sliced); // Output: [1, 2, 3]
```
✔ Does **not** modify the original array.  
✔ Extracts elements **from index 1 to 3** (excludes index 4).  

### ✅ `splice()` – Adds or removes elements **within** an array.  
#### **Example:**  
```javascript
const colors = ["red", "green", "blue"];
colors.splice(1, 1, "yellow");
console.log(colors); // Output: ["red", "yellow", "blue"]
```
✔ Modifies the original array.  
✔ Removes `1` element at index `1` and inserts `"yellow"`.  

### ✅ `concat()` – Merges two or more arrays into a **new array**.  
#### **Example:**  
```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
const merged = arr1.concat(arr2);
console.log(merged); // Output: [1, 2, 3, 4]
```
✔ Does **not** modify the original arrays.  
✔ Creates a **new** array with combined values.  

---

### 🔹 **Key Differences Between Array Methods**  
| Method | Returns New Array? | Modifies Original? | Purpose |
|--------|----------------|----------------|---------|
| `map()`, `filter()`, `reduce()` | ✅ Yes | ❌ No | Transformation |
| `forEach()`, `find()`, `some()`, `every()` | ❌ No | ❌ No | Iteration |
| `push()`, `pop()`, `shift()`, `unshift()` | ❌ No | ✅ Yes | Modification |
| `slice()`, `splice()`, `concat()` | ✅/❌ Depends | ✅/❌ Depends | Extraction & Merging |

These methods make array manipulation efficient and easy! Let me know if you need more details. 🚀
