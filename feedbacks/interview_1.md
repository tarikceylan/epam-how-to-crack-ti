# **Work With The Feedback: Dry-Run Interview #1**

## **1. JavaScript**

## **1. 1 Data Types**

### **1. Feedback:**

> Some doubts about type coercion

**Answer:**

> **Coercion** is is the automatic (implicit) conversion of values to different data types.
> **For example**; assigning a `number` to a variable which previously had a `string` would automatically convert the `typeof` that variable to `number`

### **2. Feedback:**

> Some doubts about auto-boxing

**Answer:**

> **Autoboxing** is the process of wrapping a primitive type in a wrapper object of that type which makes it possible to call specific methods.

---

## **1. 2 Context**

### **1. Feedback:**

> Mixing scope, context

**Answer:**

> **Scope** defines the visibility of variables.
> **Context** defines the object that a method belongs to.

### **2. Feedback:**

> couldn't explain call, apply, bind

**Answer:**

> - `.call()` method invokes the function that is applied to with a given `this` value and other arguments
> - `.apply()` is very similar with `.call()` with one difference. Arguments can be passed as an array using `.apply()` where `.call()` allows them to be passed one by one
> - `.bind()` is also very similar with `.call()` but instead of **invoking** the function, it **binds** the given `this` and arguments to a new function and returns the new function.

---

## **1. 3 Scope**

### **1. Feedback**

> Couldn't explain closuers well

**Answer:**

> **Closures** allow us to access outer function's scope from an inner function.
>
> **EXAMPLE:**
>
> ```javascript
> function outerFn() {
>   let name = 'John';
>   function innerFn() {
>     console.log(name);
>     //Because of closures, name variable is grab from the `outerFn` inside the `innerFn`
>   }
>   return innerFn;
> }
>
> const fn = outerFn();
> fn(); // logs out 'John'
> ```

### **2. Feedback**

> As I understood, said var has always global scope

**Answer:**

> `var` has a **global scope** unless it's defined in a `function` block. When defined in a `function` block, `var` has a **local scope**

---

## **1. 4 Prototype**

### **1. Feedback**

> Some doubts about the difference between proto and prototype

**Answer:**

> `__proto__` is the object that provides a way to inherit properties from an object that is created with `new` > `prototype` is a special object that holds shared attributes and behaviours of instances that is available in every function declartion

---

## **1. 5 Array Methods**

### **1. Feedback**

> Some doubts about forEach vs map and their usage

**Answer**

> - `.forEach()` method receives a function as an argument and executes it for each element of an array.
>   - Returns undefined.
>   - `.forEach()` method does not mutate the array it's called on but the given callback might mutate.
> - `.map()` method also receives a function as an argument and applies it on each element.
>   - Returns a new array containing the new values.
>   - Does not mutate the original array

---

## **1. 6 Functions**

### **1. Feedback**

> Doubts about arrow function usage inside class methods

**Answer**

> - **Arrow functions** don't have their bindings to `this`, `super` or `arguments`. Therefore, they shouldn't be used as methods.
> - **Arrow functions** also can not be used as `constructors`. Calling them with `new` keyword would throw a `TypeError`

---

## **1. 6 Async JS**

### **1. Feedback\***

> Some doubts about error handling in callbacks

**Answer:**

> We can provide first argument as en error argument when creating callbacks and then check for an error with a conditional statment like `if(error) {...}`

---

## **1. 7 Promises**

### **1. Feedback**

> Doubts of async/await being a syntactic sugar over Promises

**Answer:**

> `async/await` provides a way for more readable and maintainable (cleaner) code compared to `Promise`. It's just a wrapper to restyle our code.

---
