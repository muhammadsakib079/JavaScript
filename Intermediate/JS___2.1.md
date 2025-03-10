### 📂 **2.1 Array Methods in JavaScript**  

Arrays in JavaScript come with powerful built-in methods that make data manipulation easier and more efficient. Here are some of the most commonly used array methods, grouped by functionality.

---

## 🔹 **2.1.1 Transforming Arrays**  
These methods create **new** arrays based on transformations.

### ✅ **`map()`** – Applies a function to each element and returns a new array.
#### **Syntax:**
```javascript
array.map(callbackFunction)
```
#### **Example:**
```javascript
const numbers = [1, 2, 3];
const squared = numbers.map(num => num ** 2);
console.log(squared); // Output: [1, 4, 9]
```
✔ **Does not modify** the original array.

### ✅ **`filter()`** – Returns a new array with elements that match a condition.
#### **Syntax:**
```javascript
array.filter(callbackFunction)
```
#### **Example:**
```javascript
const nums = [10, 20, 30, 40];
const bigNums = nums.filter(num => num > 20);
console.log(bigNums); // Output: [30, 40]
```
✔ Keeps only elements that pass the test.

### ✅ **`reduce()`** – Reduces an array to a single value.
#### **Syntax:**
```javascript
array.reduce(callbackFunction, initialValue)
```
#### **Example:**
```javascript
const values = [1, 2, 3, 4];
const sum = values.reduce((acc, curr) => acc + curr, 0);
console.log(sum); // Output: 10
```
✔ Used for calculations like sums and averages.

---

## 🔹 **2.1.2 Iterating Over Arrays**  

### ✅ **`forEach()`** – Executes a function for each element.
#### **Syntax:**
```javascript
array.forEach(callbackFunction)
```
#### **Example:**
```javascript
const fruits = ["Apple", "Banana", "Cherry"];
fruits.forEach(fruit => console.log(fruit));
// Output:
// Apple
// Banana
// Cherry
```
✔ Does not return a new array.

### ✅ **`find()`** – Returns the first matching element.
#### **Syntax:**
```javascript
array.find(callbackFunction)
```
#### **Example:**
```javascript
const users = [
    { id: 1, name: "Alice" },
    { id: 2, name: "Bob" }
];
const user = users.find(u => u.id === 2);
console.log(user); // Output: { id: 2, name: "Bob" }
```
✔ Returns **only the first** matching item.

### ✅ **`some()` & `every()`** – Check conditions on elements.
#### **Syntax:**
```javascript
array.some(callbackFunction)  // At least one element matches
array.every(callbackFunction) // All elements must match
```
#### **Example:**
```javascript
const numbers = [3, 5, 8, 10];
console.log(numbers.some(n => n > 8));  // Output: true
console.log(numbers.every(n => n > 2)); // Output: true
```
✔ `some()` returns `true` if **at least one** element matches.
✔ `every()` returns `true` **only if all** elements match.

---

## 🔹 **2.1.3 Modifying Arrays**  

### ✅ **`push()` & `pop()`** – Add/remove elements at the end.
#### **Syntax:**
```javascript
array.push(element) // Adds an element to the end
array.pop()         // Removes the last element
```
#### **Example:**
```javascript
const colors = ["Red", "Blue"];
colors.push("Green");
console.log(colors); // Output: ["Red", "Blue", "Green"]
colors.pop();
console.log(colors); // Output: ["Red", "Blue"]
```
✔ `push()` modifies the original array.
✔ `pop()` removes **and returns** the last item.

### ✅ **`shift()` & `unshift()`** – Add/remove elements at the beginning.
#### **Syntax:**
```javascript
array.unshift(element) // Adds an element to the beginning
array.shift()         // Removes the first element
```
#### **Example:**
```javascript
const queue = ["First", "Second"];
queue.unshift("Zero");
console.log(queue); // Output: ["Zero", "First", "Second"]
queue.shift();
console.log(queue); // Output: ["First", "Second"]
```
✔ `unshift()` modifies the array by adding an element at the **beginning**.
✔ `shift()` removes **and returns** the first item.

---

## 🔹 **2.1.4 Extracting & Combining Arrays**  

### ✅ **`slice()`** – Returns a portion of an array.
#### **Syntax:**
```javascript
array.slice(start, end)
```
#### **Example:**
```javascript
const letters = ["a", "b", "c", "d", "e"];
console.log(letters.slice(1, 4)); // Output: ["b", "c", "d"]
```
✔ `slice()` **does not modify** the original array.

### ✅ **`splice()`** – Modifies an array by adding/removing elements.
#### **Syntax:**
```javascript
array.splice(start, deleteCount, item1, item2)
```
#### **Example:**
```javascript
const months = ["Jan", "Feb", "Apr"];
months.splice(2, 0, "Mar"); // Inserts "Mar" at index 2
console.log(months); // Output: ["Jan", "Feb", "Mar", "Apr"]
```
✔ `splice()` **modifies** the original array.
✔ Can **add or remove** elements.

### ✅ **`concat()`** – Merges two or more arrays.
#### **Syntax:**
```javascript
newArray = array1.concat(array2)
```
#### **Example:**
```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
const combined = arr1.concat(arr2);
console.log(combined); // Output: [1, 2, 3, 4]
```
✔ Returns a **new** array.

---

Mastering array methods makes JavaScript **more efficient** and allows for cleaner, more readable code. 🚀
