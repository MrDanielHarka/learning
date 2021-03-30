# OOP and Classes

## Notes

21.03.30.

### General

OOP: Object-Oriented Programming

"Object-oriented programming is a programming paradigm based on the concept of "objects", which can contain data and code: data in the form of fields (often known as attributes or properties), and code, in the form of procedures (often known as methods). OOP languages are diverse, but the most popular ones are class-based, meaning that objects are instances of classes, which also determine their types."
It is a programming paradigm, that is centered around objects rather than functions.

### **The 4 pillars**

**Encapsulation**

Reduce complexity and increase reusability.

f() = Method\
x = Property

Example:

Without OOP

```JavaScript
let baseSalary = 30_000;
let overtime = 10;
let rate = 20;

function getWage(baseSalary, overtime, rate) {
    return baseSalary + (overTime * rate);
}
```

With OOP

```JavaScript
let employee = {
    baseSalary : 30_000,
    overtime : 10,
    rate : 20,
    getWage: function() {
        return this.baseSalary + (this.overtime * this.rate)
    }
};
employee.getWage();
```

**Abstraction**

Reduce complexity and isolate impact of changes.

Pros
- Simpler interface
- Reduce the impact of change

**Inheritance**
Eliminate redundant code.

Helps us to use details that are set already.

**Polymorphism**

Refactor long switch/case statements.

A technique that allows us to get rid of long if & else or switch & case statements.

