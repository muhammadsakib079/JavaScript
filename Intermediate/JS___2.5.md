### ⚠️ **2.5 Error Handling in JavaScript**  

Error handling is crucial for building **robust and bug-free applications**. JavaScript provides mechanisms to handle errors gracefully using `try`, `catch`, `finally`, and `throw`.  

---

## 🔹 **2.5.1 `try`, `catch`, `finally`**  
The `try` block contains code that may throw an error, while `catch` handles the error. The `finally` block (optional) executes **regardless of whether an error occurs**.  

#### **Syntax:**  
```javascript
try {
    // Code that may cause an error
} catch (error) {
    // Handle the error
} finally {
    // (Optional) Code that always runs
}
```
#### **Example:**  
```javascript
try {
    let result = 10 / 0; // No actual error, but logical issue
    console.log(result);
} catch (error) {
    console.log("An error occurred: ", error.message);
} finally {
    console.log("Execution completed.");
}
```
✔ **`try`**: Runs the main code.
✔ **`catch`**: Captures and processes errors.
✔ **`finally`**: Runs whether an error occurs or not.

---

## 🔹 **2.5.2 `throw` Statement**  
The `throw` statement lets you **manually trigger errors** in specific situations.  

#### **Syntax:**  
```javascript
throw new Error("Custom error message");
```
#### **Example:**  
```javascript
function divide(a, b) {
    if (b === 0) {
        throw new Error("Division by zero is not allowed");
    }
    return a / b;
}
try {
    console.log(divide(10, 0));
} catch (error) {
    console.log("Error: ", error.message);
}
```
✔ Useful for **custom error messages**.  
✔ Enhances **debugging and validation**.

---

Proper error handling **prevents application crashes** and improves the user experience. Master these techniques to build reliable JavaScript applications! 🚀