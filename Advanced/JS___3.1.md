### ⏳ **3.1 Asynchronous JavaScript**  

Asynchronous JavaScript allows executing code **without blocking** the main thread, improving performance and responsiveness. It includes **callbacks, promises, and async/await**.  

---

## 🔹 **3.1.1 Synchronous vs Asynchronous**  
- **Synchronous**: Code executes **line by line**. If one task takes time, the entire program waits.
- **Asynchronous**: Code execution **does not stop** for time-consuming tasks (e.g., API requests, file reading).  

#### **Example (Synchronous Code):**  
```javascript
console.log("Start");
for (let i = 0; i < 3; i++) {
    console.log(i);
}
console.log("End");
```
**Output:**
```
Start
0
1
2
End
```

#### **Example (Asynchronous Code using `setTimeout`):**  
```javascript
console.log("Start");
setTimeout(() => console.log("Async Task"), 2000);
console.log("End");
```
**Output:**
```
Start
End
Async Task (after 2 seconds)
```
✔ Asynchronous code **does not block execution**.

---

## 🔹 **3.1.2 Callbacks**  
A **callback function** is passed as an argument to another function and executes **after** the main function completes.  

#### **Syntax:**  
```javascript
function mainTask(callback) {
    console.log("Task started");
    callback(); // Call the function passed as an argument
}
```
#### **Example:**  
```javascript
function greet(name, callback) {
    console.log("Hello, " + name);
    callback();
}
greet("Alice", function() {
    console.log("Welcome to JavaScript!");
});
```
✔ Callbacks **control execution order**.
✔ Can lead to **callback hell** (deeply nested callbacks).

---

## 🔹 **3.1.3 Promises (`resolve`, `reject`, `then`, `catch`, `finally`)**  
A **Promise** represents a future value (success or failure). It avoids **callback hell**.

#### **Syntax:**  
```javascript
const promise = new Promise((resolve, reject) => {
    if (condition) {
        resolve("Success");
    } else {
        reject("Failure");
    }
});
```
#### **Example:**  
```javascript
const fetchData = new Promise((resolve, reject) => {
    setTimeout(() => {
        let success = true;
        if (success) resolve("Data loaded");
        else reject("Error fetching data");
    }, 2000);
});

fetchData
    .then(response => console.log(response)) // Runs if resolved
    .catch(error => console.log(error)) // Runs if rejected
    .finally(() => console.log("Process completed"));
```
✔ **`then()`**: Runs if resolved.  
✔ **`catch()`**: Runs if rejected.  
✔ **`finally()`**: Runs regardless of success/failure.

---

## 🔹 **3.1.4 Async/Await**  
`async` functions return **promises** and use `await` to pause execution until a promise resolves.

#### **Syntax:**  
```javascript
async function functionName() {
    let result = await promiseName;
}
```
#### **Example:**  
```javascript
async function fetchData() {
    try {
        let response = await new Promise(resolve => setTimeout(() => resolve("Data received"), 2000));
        console.log(response);
    } catch (error) {
        console.log("Error: ", error);
    }
}
fetchData();
```
✔ `await` **pauses execution** until the promise resolves.
✔ Easier to **read** than `.then()` chaining.

---

Asynchronous JavaScript improves performance and user experience. Mastering **callbacks, promises, and async/await** is essential for handling real-world JavaScript applications! 🚀