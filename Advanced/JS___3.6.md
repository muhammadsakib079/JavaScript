### 🏢 **3.6 JavaScript Frameworks & Libraries**  

JavaScript frameworks and libraries simplify **frontend and backend development**, providing tools to create **dynamic, scalable, and efficient applications**.

---

## 🔹 **3.6.1 Frontend Frameworks & Libraries**  
Frontend frameworks help build **interactive UI components** and manage application states efficiently.

### ✅ **React.js**  
A component-based library developed by **Meta** for building **fast, dynamic UIs**.

#### **Syntax (React Component):**  
```javascript
import React from "react";

function Greeting({ name }) {
    return <h1>Hello, {name}!</h1>;
}

export default Greeting;
```
✔ Uses **JSX** for UI rendering.  
✔ Efficient with **Virtual DOM**.  
✔ Supports **state management** via hooks (`useState`, `useEffect`).  

---

### ✅ **Vue.js**  
A **progressive** framework that is **lightweight, flexible**, and easy to integrate.

#### **Syntax (Vue Component):**  
```html
<template>
  <h1>Hello, {{ name }}!</h1>
</template>

<script>
export default {
  data() {
    return { name: "World" };
  }
};
</script>
```
✔ Uses **two-way data binding** (`v-model`).  
✔ Simple and **easy to learn**.  
✔ Supports **component-based development**.  

---

### ✅ **Angular.js**  
A **TypeScript-based framework** developed by **Google** for building **large-scale applications**.

#### **Syntax (Angular Component):**  
```typescript
import { Component } from '@angular/core';
@Component({
  selector: 'app-greeting',
  template: '<h1>Hello, {{ name }}!</h1>'
})
export class GreetingComponent {
  name: string = 'World';
}
```
✔ Uses **TypeScript** for **strong typing**.  
✔ Provides **dependency injection**.  
✔ Ideal for **enterprise applications**.  

---

## 🔹 **3.6.2 Backend Framework**  
Backend frameworks handle **server-side logic, APIs, and database communication**.

### ✅ **Express.js (Node.js Framework)**  
A minimalist **backend framework** for **creating REST APIs and web applications**.

#### **Syntax (Basic Express Server):**  
```javascript
const express = require("express");
const app = express();

app.get("/", (req, res) => {
    res.send("Hello, World!");
});

app.listen(3000, () => console.log("Server running on port 3000"));
```
✔ Fast and **lightweight**.  
✔ Easy **routing and middleware support**.  
✔ Works well with **MongoDB, PostgreSQL, and other databases**.  

---

## 🔹 **3.6.3 Utility Library**  
Utility libraries simplify **DOM manipulation, animations, and AJAX requests**.

### ✅ **jQuery**  
An older but still-used library for **simplified DOM manipulation**.

#### **Syntax (jQuery Example):**  
```javascript
$(document).ready(function() {
    $("button").click(function() {
        $("#message").text("Button Clicked!");
    });
});
```
✔ Simplifies **AJAX calls, animations, and event handling**.  
✔ Used in **legacy projects** but being replaced by modern frameworks.  

---

By choosing the right **JavaScript framework or library**, developers can build efficient **frontend and backend applications** tailored to their needs! 🚀
