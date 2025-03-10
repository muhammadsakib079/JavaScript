### 📦 **2.4 Classes & Object-Oriented Programming (OOP) in JavaScript**  

ES6 introduced **classes** in JavaScript, making object-oriented programming (OOP) more structured and easier to implement. OOP principles like **encapsulation, inheritance, and polymorphism** enhance code organization and reusability.  

---

## 🏩 **2.4.1 `class` and `constructor`**  
A `class` is a blueprint for creating objects, and the `constructor` initializes object properties.  

#### **Syntax:**  
```javascript
class ClassName {
    constructor(parameter1, parameter2) {
        this.property1 = parameter1;
        this.property2 = parameter2;
    }
}
```
#### **Example:**  
```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
}
const user = new Person("Alice", 25);
console.log(user.name); // Output: Alice
console.log(user.age);  // Output: 25
```
✔ Provides a clear structure for objects.  
✔ The `constructor` method runs when a new object is created.  

---

## 📌 **2.4.2 `this` Keyword**  
`this` refers to the current object instance within a class or function.  

#### **Example:**  
```javascript
class Car {
    constructor(brand) {
        this.brand = brand;
    }
    showBrand() {
        return `This car is a ${this.brand}`;
    }
}
const myCar = new Car("Toyota");
console.log(myCar.showBrand()); // Output: This car is a Toyota
```
✔ `this` dynamically refers to the **object calling the method**.  
✔ Used to access class properties inside methods.  

---

## 🎩 **2.4.3 Inheritance (`extends` & `super`)**  
Inheritance allows a class to derive properties and methods from another class.  

#### **Syntax:**  
```javascript
class ChildClass extends ParentClass {
    constructor(params) {
        super(params); // Calls parent constructor
    }
}
```
#### **Example:**  
```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        return `${this.name} makes a sound.`;
    }
}
class Dog extends Animal {
    constructor(name, breed) {
        super(name);
        this.breed = breed;
    }
    bark() {
        return `${this.name} barks!`;
    }
}
const pet = new Dog("Buddy", "Labrador");
console.log(pet.speak()); // Output: Buddy makes a sound.
console.log(pet.bark());  // Output: Buddy barks!
```
✔ `extends` allows one class to **inherit** another.  
✔ `super()` calls the **parent class constructor**.  

---

## 🔧 **2.4.4 Static Methods**  
Static methods belong to the class itself, not instances.  

#### **Syntax:**  
```javascript
class ClassName {
    static methodName() {
        return "Static method called";
    }
}
```
#### **Example:**  
```javascript
class MathUtils {
    static add(a, b) {
        return a + b;
    }
}
console.log(MathUtils.add(5, 3)); // Output: 8
```
✔ Called on the **class**, not instances (`MathUtils.add(5, 3)`).  
✔ Useful for utility/helper functions.  

---

## 🛠 **2.4.5 Encapsulation & Polymorphism**  
### ✅ **Encapsulation** – Restricts access to class properties using **private fields** (`#`).  

#### **Example:**  
```javascript
class BankAccount {
    #balance; // Private field
    constructor(balance) {
        this.#balance = balance;
    }
    getBalance() {
        return `Your balance is $${this.#balance}`;
    }
}
const account = new BankAccount(1000);
console.log(account.getBalance()); // Output: Your balance is $1000
console.log(account.#balance); // ❌ Error: Private field
```
✔ Private fields prevent direct modification.  
✔ Access is controlled through **getter methods**.  

### ✅ **Polymorphism** – Allows child classes to override parent methods.  

#### **Example:**  
```javascript
class Shape {
    area() {
        return "Calculating area...";
    }
}
class Circle extends Shape {
    constructor(radius) {
        super();
        this.radius = radius;
    }
    area() {
        return Math.PI * this.radius ** 2;
    }
}
const circle = new Circle(5);
console.log(circle.area()); // Output: 78.5398...
```
✔ Child class **overrides** parent method.  
✔ Enables dynamic behavior in **object hierarchies**.  

---

Classes and OOP principles **simplify code organization, improve reusability, and promote clean architecture**. Mastering these concepts enhances JavaScript development! 🚀