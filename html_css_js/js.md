# **JavaScript Interview Questions**

## **Week 1**

---

## **1. Data Types**

### **1. 1 What are data types in JavaScript?**

- **Primitive Types**
  - **Number** represents both integer and float numbers
  - **BigInt** represents integer values greater or lesser than ±$2^{53}-1$ with precision.
  - **String** represents collection of characters
  - **Boolean** represents logical values `true` or `false`
  - **`null`** is a type of its own which contains only the `null` value
  - **`undefined`** represents the absence of value assignment
- **Non-Primitive Types**
  - **Object** type is used to represent complex data structures
  - **Symbol** type is used to create unique identifiers for objects

> **References:**
>
> [Data Types | JavaScript.info](https://javascript.info/types)

### **1. 2 What are primitive data types?**

- **Number** represents both integer and float numbers
- **BigInt** represents integer values greater or lesser than ±$2^{53}-1$ with precision.
- **String** represents collection of characters
- **Boolean** represents logical values `true` or `false`
- **`null`** is a type of its own which contains only the `null` value. It represents **"nothing"**, **"empty"**, **"value unknown"**
- **`undefined`** represents the absence of value assignment

> **References:**
>
> [Data Types | JavaScript.info](https://javascript.info/types)

### **1. 3 What is the differance between primitives vs objects?**

The main and most important difference between primitives and `objects` are; **primitive types** are **passed by value** which means, the variable that holds the value is set to that value directly. However, `objects` are **passed by reference** which means they containt a **reference** to the object.

> **References:**
>
> [Primitive vs Reference Data Types in JavaScript](https://www.freecodecamp.org/news/primitive-vs-reference-data-types-in-javascript/)

### **1. 4 What is coercion in JavaScript?**

**Coercion** in JavaScript is the automatic conversion of values to different data types

> **References:**
>
> [Type Coercion | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Type_coercion)

### **1. 5 Do you know what Autoboxing in JS is?**

When a method is called on a primitive type, primitive itself is automatically wrapped into a wrapper object. That way, we can call methods like `valueOf()`, `toString()` etc. This process is called **Autoboxing** in JavaScript

> **References:**
>
> [Autoboxing in JavaScript | Mediium](https://medium.com/weekly-webtips/autoboxing-in-javascript-a368b42d8969)

### **1. 6 What is the difference between == and === operators?**

`==` (loose equality) operator performs a type conversion before comparison, where `===` (strcit equality) checks for data type equality as well.

> **References:**
>
> - [Equality Comparisons and Sameness | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness)

### **1. 7 What is undefined data type?**

`undefined` represents absence of value assignment to a variable.

> **References:**
>
> - [Data Types > `undefined` | JavaScript.info](https://javascript.info/types#the-undefined-value)

### **1. 8 What is null value?**

`null` represents "nothing" in JavaScript. It's not a reference to "non-existing object" or "null pointer" like in other languages.

> **References:**
>
> - [Data Types > `null` | JavaScript.info](https://javascript.info/types#the-null-value)

### **1. 9 What does isNaN function do?**

`isNaN()` function determines whether a value is `NaN`(Not A Number) or not

> **References:**
>
> - [isNaN() | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN)

### **1. 10 What does `NaN` value mean?**

**
`NaN` represents a value that is **"Not-A-Number"\*\*

> **References:**
>
> - [`NaN` | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/NaN)

### **1. 11 What is the difference between null and undefined?**

**`null`** is the intentional assignment of "nothing", "empty" whereas, **`undefined`** is the absence of a value for an existing object.

---

## **2.Objects, Classes, Prototypal Inheritance**

### **2. 1 How do you copy properties from one object to another?**
