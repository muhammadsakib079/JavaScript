### 🌍 **3.2 Web APIs & DOM Manipulation**  

JavaScript interacts with web pages using the **Document Object Model (DOM)** and various Web APIs. These tools allow developers to manipulate elements, handle events, and store data efficiently.  

---

## 🔹 **3.2.1 Selecting Elements**  
### ✅ `document.querySelector()` & `getElementById()`  
These methods help select HTML elements dynamically.

#### **Syntax:**  
```javascript
document.querySelector("selector"); // Selects the first matching element
document.getElementById("id"); // Selects an element by ID
```
#### **Example:**  
```javascript
const title = document.querySelector("h1");
const button = document.getElementById("myButton");
console.log(title.textContent);
```
✔ `querySelector()` selects elements using **CSS selectors**.  
✔ `getElementById()` selects elements using their **ID attribute**.  

---

## 🔹 **3.2.2 DOM Events (`click`, `mouseover`, `keydown`)**  
JavaScript can **detect and respond** to user interactions.  

#### **Syntax:**  
```javascript
element.addEventListener("event", callbackFunction);
```
#### **Example:**  
```javascript
const button = document.getElementById("myButton");
button.addEventListener("click", () => {
    alert("Button clicked!");
});
```
✔ `click` – Detects mouse clicks.  
✔ `mouseover` – Detects when the mouse hovers over an element.  
✔ `keydown` – Detects when a key is pressed.  

---

## 🔹 **3.2.3 Event Delegation**  
Event delegation allows efficient event handling **by assigning a listener to a parent element** instead of multiple child elements.

#### **Syntax:**  
```javascript
parentElement.addEventListener("event", function(event) {
    if (event.target.matches("childSelector")) {
        // Handle event
    }
});
```
#### **Example:**  
```javascript
document.querySelector("ul").addEventListener("click", function(event) {
    if (event.target.tagName === "LI") {
        console.log("Clicked on:", event.target.textContent);
    }
});
```
✔ Improves performance by reducing event listeners.  
✔ Useful for **dynamically added elements**.  

---

## 🔹 **3.2.4 Fetch API & AJAX**  
The Fetch API retrieves data asynchronously from servers.  

#### **Syntax:**  
```javascript
fetch("url")
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error("Error:", error));
```
#### **Example:**  
```javascript
fetch("https://jsonplaceholder.typicode.com/posts/1")
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error("Error fetching data:", error));
```
✔ Fetches **JSON, text, or other formats**.  
✔ Replaces older `XMLHttpRequest` (AJAX).  

---

## 🔹 **3.2.5 LocalStorage & SessionStorage**  
These APIs allow saving data **directly in the browser**.

### ✅ **LocalStorage** – Stores data permanently until manually cleared.  
#### **Syntax:**  
```javascript
localStorage.setItem("key", "value");
const value = localStorage.getItem("key");
localStorage.removeItem("key");
localStorage.clear();
```
#### **Example:**  
```javascript
localStorage.setItem("username", "Alice");
console.log(localStorage.getItem("username")); // Output: Alice
```
✔ Data persists even after the page is closed.  

### ✅ **SessionStorage** – Stores data **only while the tab is open**.  
#### **Syntax:**  
```javascript
sessionStorage.setItem("key", "value");
const value = sessionStorage.getItem("key");
sessionStorage.removeItem("key");
sessionStorage.clear();
```
✔ Data is removed when the **browser tab is closed**.  

---

JavaScript's **Web APIs and DOM Manipulation** provide powerful ways to create interactive web pages. Mastering these features enables dynamic, efficient, and user-friendly applications! 🚀