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

Loops are essential for automating repetitive tasks in JavaScript. Let me know if you need further explanations! 🚀
