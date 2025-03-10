### ⚡ **3.5 JavaScript Performance Optimization**  

Optimizing JavaScript performance enhances user experience by reducing **lag, improving load times, and minimizing memory usage**. Key techniques include **debouncing, throttling, lazy loading, and memory management**.

---

## 🔹 **3.5.1 Debouncing & Throttling**  

### ✅ **Debouncing**  
Debouncing delays execution of a function until **after a specified delay** when an event stops firing. This is useful for **search bars, resizing windows, and input fields**.

#### **Syntax:**  
```javascript
function debounce(func, delay) {
    let timer;
    return function (...args) {
        clearTimeout(timer);
        timer = setTimeout(() => func.apply(this, args), delay);
    };
}
```
#### **Example:**  
```javascript
const searchInput = document.getElementById("search");
const fetchResults = debounce(() => console.log("Fetching data..."), 500);
searchInput.addEventListener("input", fetchResults);
```
✔ Reduces unnecessary function calls.  
✔ Improves **search input and resize performance**.  

### ✅ **Throttling**  
Throttling ensures a function **executes at most once within a given time frame**. This is useful for **scroll events, mouse movement, and API requests**.

#### **Syntax:**  
```javascript
function throttle(func, limit) {
    let lastCall = 0;
    return function (...args) {
        let now = Date.now();
        if (now - lastCall >= limit) {
            lastCall = now;
            func.apply(this, args);
        }
    };
}
```
#### **Example:**  
```javascript
window.addEventListener("scroll", throttle(() => {
    console.log("Scroll event triggered");
}, 200));
```
✔ Prevents function execution **too frequently**.  
✔ Optimizes **scrolling, resizing, and animations**.  

---

## 🔹 **3.5.2 Lazy Loading**  
Lazy loading defers loading of **non-critical resources** until needed, improving initial page load time.

#### **Example:**  
```html
<img src="placeholder.jpg" data-src="real-image.jpg" class="lazy-load" alt="Lazy Image">
```
```javascript
document.addEventListener("DOMContentLoaded", function() {
    const images = document.querySelectorAll(".lazy-load");
    const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                let img = entry.target;
                img.src = img.getAttribute("data-src");
                observer.unobserve(img);
            }
        });
    });
    images.forEach(img => observer.observe(img));
});
```
✔ Improves **page speed and performance**.  
✔ Saves bandwidth by loading images **only when visible**.  

---

## 🔹 **3.5.3 Memory Management**  
Efficient memory usage prevents **leaks and improves performance**.

### ✅ **Avoiding Global Variables**  
Using too many global variables can **increase memory consumption**.
```javascript
// Avoid this:
window.largeArray = new Array(1000000);
```
✔ Use **local variables and closures** when possible.  

### ✅ **Garbage Collection Awareness**  
JavaScript automatically frees memory, but some references **prevent garbage collection**.
```javascript
let obj = {};
obj.ref = obj; // Circular reference, prevents GC
```
✔ Use `WeakMap` or `WeakSet` for objects that should be **garbage collected** when unreferenced.  

### ✅ **Efficient DOM Manipulation**  
Minimize DOM updates to **reduce reflows and repaints**.
```javascript
// Inefficient:
document.body.innerHTML += "<p>New element</p>";

// Efficient:
const fragment = document.createDocumentFragment();
const newElement = document.createElement("p");
newElement.textContent = "New element";
fragment.appendChild(newElement);
document.body.appendChild(fragment);
```
✔ Reduces **unnecessary re-rendering**.  
✔ Improves **UI responsiveness**.  

---

By implementing these **JavaScript performance optimization techniques**, applications become **faster, smoother, and more efficient**! 🚀
