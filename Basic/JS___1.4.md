### 🔄 **1.4 Conditional Statements in JavaScript**  

Conditional statements allow you to execute different blocks of code based on certain conditions. JavaScript provides several ways to handle conditions.  

---

## 📌 **1.4.1 `if`, `else`, `else if` Statements**  
These statements execute different code blocks depending on whether a condition is `true` or `false`.  

### ✅ **`if` Statement**  
The `if` statement executes a block of code **only if** a specified condition is `true`.  

#### **Syntax:**  
```javascript
if (condition) {
    // Code to execute if the condition is true
}
```
#### **Example:**  
```javascript
let age = 20;

if (age >= 18) {
    console.log("You are an adult.");
}
```
✔ If `age >= 18`, the message **"You are an adult."** is displayed.  
✖ If `age < 18`, nothing happens.  

---

### 🔀 **`if...else` Statement**  
The `if...else` statement provides an **alternative block** to execute if the condition is `false`.  

#### **Syntax:**  
```javascript
if (condition) {
    // Code if condition is true
} else {
    // Code if condition is false
}
```
#### **Example:**  
```javascript
let age = 16;

if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```
✔ If `age >= 18`, it prints **"You are an adult."**  
✔ If `age < 18`, it prints **"You are a minor."**  

---

### 🔄 **`if...else if...else` Statement**  
The `else if` statement checks **multiple conditions** in sequence.  

#### **Syntax:**  
```javascript
if (condition1) {
    // Code if condition1 is true
} else if (condition2) {
    // Code if condition2 is true
} else {
    // Code if none of the above conditions are true
}
```
#### **Example:**  
```javascript
let score = 85;

if (score >= 90) {
    console.log("Grade: A");
} else if (score >= 80) {
    console.log("Grade: B");
} else if (score >= 70) {
    console.log("Grade: C");
} else {
    console.log("Grade: F");
}
```
✔ If `score >= 90`, it prints **"Grade: A"**  
✔ If `score >= 80` but `< 90`, it prints **"Grade: B"**  
✔ If `score >= 70` but `< 80`, it prints **"Grade: C"**  
✔ If none of the conditions match, it prints **"Grade: F"**  

---

## 📌 **1.4.2 `switch` Statement**  
The `switch` statement is an alternative to multiple `if...else if` conditions. It compares a value against multiple **cases** and executes the matching case.  

#### **Syntax:**  
```javascript
switch (expression) {
    case value1:
        // Code to execute if expression === value1
        break;
    case value2:
        // Code to execute if expression === value2
        break;
    default:
        // Code to execute if no case matches
}
```
#### **Example:**  
```javascript
let day = "Monday";

switch (day) {
    case "Monday":
        console.log("Start of the workweek.");
        break;
    case "Friday":
        console.log("Weekend is near!");
        break;
    case "Saturday":
    case "Sunday":
        console.log("It's the weekend!");
        break;
    default:
        console.log("A regular weekday.");
}
```
✔ If `day` is `"Monday"`, it prints **"Start of the workweek."**  
✔ If `day` is `"Friday"`, it prints **"Weekend is near!"**  
✔ If `day` is `"Saturday"` or `"Sunday"`, it prints **"It's the weekend!"**  
✔ If `day` is any other value, it prints **"A regular weekday."**  

---

### 🔹 **Key Differences Between `if...else` and `switch`**  
| Feature  | `if...else` | `switch` |
|----------|------------|----------|
| Condition Type | Works with **any** condition | Works with **strict equality (`===`)** |
| Readability | Best for **range-based** conditions | Best for **fixed values** |
| Performance | Can be **slower** with many conditions | Can be **faster** with many fixed cases |

---

These conditional statements help in decision-making in JavaScript programs. Let me know if you need more examples! 🚀
