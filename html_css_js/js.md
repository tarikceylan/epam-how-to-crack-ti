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

When it comes to copying objects there are 2 different approaches.

- Shallow Copy - copies reference to the object. Changes affect both
- Deep Copy - duplicates the object and creates a new reference to the duplicate. Changes affect only the duplicates

**Shallow Copy** allow us copy an object by assigning its reference to another variable and can be achieved in multiple ways. One of them is `Object.assign()` method.

- **`Object.assign([target], [source])`** method takes two parameters which are `target` object and `source` object in that order and a copy of the object's reference gets created. Therefore, copied object would be a **shallow copy**

**Deep Copy** on the other hand, create a duplicate which does not share the reference with the original object. The duplicate is a new object and can be changed without affecting the original. There are few ways to create a deep copy.

- `JSON.parse(JSON.stringify([sourceObject]))` first creates a JSON string from a given `sourceObject` and then parses that string with `JSON.parse()` to convert it into a completely new JavaScript object.

- `structuredClone()` is another built-in method that we can use to deep copy an object.

> **References:**
>
> - [Shallow Copy | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Shallow_copy)
> - [Deep Copy | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Deep_copy)

### **2. 2 What are classes in ES6?**

**Classes** are a template for creating objects that encapsulates data and provide ways to work on the data. In JavaScript they're built on prototypes

### **2. 3 Explain how prototypal inheritance works.**

In JavaScript, all objects have a hidden property named `[[Prototype]]` which is either `null` or references to a different object called `prototype`. When we try to read a property from an object, if it's missing, JavaScript automatically checks `prototype` for the missing property. This behaviour creates **prototypal inheritance**

We can access `[[Prototype]]` property by using `__proto__` keyword which would let us get and set values for methods and properties.

> **References:**
>
> - [Prototypal Inheritance | JavaScript.info](https://javascript.info/prototype-inheritance)
> - [Inheritance and Prototype Chaining | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)

---

## **3. Context, Scope and Closure**

### **3. 1 How do you assign default values to variables?**

**Assigning default values to variables** can be achieved by first checking the existing of a value and assigning one if there is none.

**EXAMPLE:**

```javascript
let myNum;

// myNum is equal to either myNum's value or 3. Since myNum variable does not have a value yet, will return undefined which is a `falsy` value. Part before `||` will not met the condition. Therefore, myNum will be assigned to value of 3

myNum = myNum || 3;

console.log(mynum); //logs 3 to the console
```

Same behaviour can be achieved using `if/else` statement or `ternary` operator

> **References:**
>
> - [3 Ways to Set Default Value in JavaScript](https://www.samanthaming.com/tidbits/52-3-ways-to-set-default-value/)

### **3. 2 What is the difference between `let`, `const`, `var`?**

`let`, `const` and `var` keywords are used for defining variables. `var` has become the "old way" after introduction of `let` and `const` with ES6.

The key differences between them are as follows:

- `var` has a global scope and is [hoisted](#3-5-what-is-hoisting)
- `let` is function scoped and used to define variables with a value that can be changed.
- `const` is also function scoped but used to define varaibles with non-changeable values.

`let` and `const` are also [hoisted](#3-5-what-is-hoisting) but they live in [Temporal Dead Zone](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#temporal_dead_zone_tdz). Therefore, they can't be accessed during runtime and cause errors.

> **References:**
>
> - [Variables | JavaScript.info](https://javascript.info/variables)

### **3. 3 What are the differences between undeclared and undefined variables?**

**undeclared** is the absolute absence of a variable declaration with either `var`, `let` or `const`, whereas `undefined` represents the existance of a variable without a value assigned to it.

> **References:**
>
> - [Undefined vs Undeclared](https://www.codingem.com/undefined-and-undeclared-in-javascript/)

### **3. 4 What are global variables?**

**A Global Variable** is a variable that is declared in the global scope which becomes a property of the global object

> **References:**
>
> - [Global Object | JavaScript.info](https://javascript.info/global-object)

### **3. 5 What is Hoisting?**

When a variable declared without **initialization**, it'll be moved to the top of its scope and will be available to use.

Variables declared with `var` are hoisted. Variables declared with `let` and `const` keywords are hoisted too but they're not accessible during runtime because they live in [Temporal Dead Zone](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#temporal_dead_zone_tdz)

> **References:**
>
> - [Hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)

### **3. 6 What is scope in javascript?**

**Scope** is the current context of execution where all values are visible and can be accessed.

> **References:**
>
> - [Scope | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Scope)

### **3. 7 What is the closure?**

**Closure**(in JavaScript) provides access to an outer function's scope from an inner function.

> **References:**
>
> - [Closures | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

### **3. 8 How does closure implemented in the javascript?**

**Closure** can be implemented by creating two nested functions.

The outer function would have an expression in its body and the inner function would be able to grab it, if there is a need for the use of that variable.

**EXAMPLE:**

```javascript
function outerFn() {
  let name = 'John';
  function innerFn() {
    console.log(name);
    //Because of closures, name variable is grab from the `outerFn` inside the `innerFn`
  }
  return innerFn;
}

const fn = outerFn();
fn(); // logs out 'John'
```

> **References:**
>
> - [Closures | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

### **3. 9 What is the difference between Call, Apply and Bind?**

- `call()` method invokes a function with a given `this` and arguments are provided into it one by one. `call()` allow us to specify the value of `this`

- `apply()` method invokes a function and arguments are passed in as an `Array`

- `bind()` returns a completely new function which is bind to `this` keyword. Any number of arguments can be passed.

> **References:**
>
> - [JavaScript Function Methods: Call vs Apply vs Bind | Medium](https://medium.com/@jhawleypeters/javascript-call-vs-apply-vs-bind-61447bc5e989)

### **3. 10 What does 'this loses context' mean?**

"`this` loses context" means that `this` keyword does not refer to its surrounding object anymore. Such as when `this` is used inside of a nested function, it'll be out of its scope

> **References:**
>
> - [What to do when “this” loses context](https://www.freecodecamp.org/news/what-to-do-when-this-loses-context-f09664af076f/)

---

## 4. JSON

### **4. 1 What is JSON and its common operations?**

**JSON - JavaScript Object Notation** is a standard format to represent structured data based on JavaScript's object syntax. JSON is commonly used for transmitting and storing data.

Its common methods are:

- `JSON.parse()` which is used for converting a JSON string into a Javascript object.
- `JSON.stringify()` which is used for converting an JavaScript object into a JSON string

> **References:**
>
> - [Working with JSON | MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)

### **4. 2 How do you parse a JSON string?**

`JSON.parse()` method can be used to parse a JSON string into a JavaScript Object

> **References:**
>
> - [Working with JSON | MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)

### **4. 3 What is the purpose JSON stringify?**

`JSON.stringify()` can be used for converting a JavaScript Object into a JSON string.

> **References:**
>
> - [Working with JSON | MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)

---

## **5. Array Methods**

### **5. 1 What array methods do you know?**

- `splice()` - modifies an array by either adding, removing or replacing an element
- `slice()` - returns a new, modified array where only a portion of original array exists depending on given arguments.
- `map()` - takes an `Array` and a `callback` as arguments, applies `callback` function operations onto the given `Array` and returns a **new `Array`**
- `forEach` - iterates over an `Array`'s elements. Returns nothing
- `includes()` - checks if a given argument exist in the `Array`. Returns a `boolean` value.
- `indexOf()` - checks if the given element exists in the array and returns the `Number` value of a given element's index. Returns `-1` if element is not found.
- `push()` - inserts given element to the end of an `Array`. Returns the length of the new array.
- `pop()` - remove the last element of the `Array` it's called on and returns it.
- `shift()` - removes the first element from an `Array` and returns the removed element.
- `unfshift()` - inserts one or more new element(s) to the start of an `Array`. Returns the length of the new `Array`
- `every()` - checks if every element in an `Array` pass the given condition. Returns `boolean`
- `some()` - checks if at least one element in an `Array` pass the given condition. Returns `boolean`
- `filter()` - returns a new, modified `Array` which consists only the elements that passed the given filter conditions in the original array.
- `reduce()` - goes over every element in an `Array` and applies the given `callback` operations. Each iteration returns a single result which will be applied on the next element. Finally, **"reduces"** the result into a single value and returns it.

> **References:**
>
> - [Array Methods | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#array_methods_and_empty_slots)

### **5. 2 What is the difference between Array.forEach() and Array.map()?**

- `forEach()` method iterates over the `Array`, applies given `callback` operations but does not return anything.
- `map()` method also iterates over the `Array` and applies given `callback` operations on each element. Creates a new `Array` populated with the new elements and returns the new `Array`

> **References:**
>
> - [Array.prototype.forEach() | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
> - [Array.prototype.map() | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

---

## **6. Functions**

### **6. 1 What are the lambda or arrow functions?**

**Arrow Functions**, are introduced with ES6 and are an alternative way to traditional function expressions. However, arrow functions are not the best choice for every situation.

- Arrow functions don't have their own bindings to `this`, `arguments` or `super`. Therefore, they shouldn't be used as **methods**
- Arrow functions can not be used as `constructors`. Calling them with `new` keyword throws a `TypeError`

> **References:**
>
> - [Arrow Functions | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

### **6. 2 What is a pure function?**

**A Pure Function** is a function that always returns the same result if the same arguments are passed.

**EXAMPLE:**

```javascript
function doublePrice(price) {
  return price * 2;
}
```

> **References:**
>
> - [Pure Functions in JavaScript](https://www.geeksforgeeks.org/pure-functions-in-javascript/)

### **6. 3 What is IIFE(Immediately Invoked Function Expression)?**

**An IIFE** is a function that runs as soon as it's defined. They're usually used for quick and non-repetetive tasks.

> **References:**
>
> - [IIFE | MDN](https://developer.mozilla.org/en-US/docs/Glossary/IIFE)

### **6. 4 What is a callback function?**

A `callback` function is a function that is passed into another function as an argument. Callback function gets invoked to complete certain operations before the main function ends.

> **References:**
>
> - [Callback Function | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)

---

## **7. Async JavaScript**

### **7.1 What is a promise?**

`Promise` object represents a template for a value that is not yet set. The eventual value depends on the state of the `Promise` object which can be `fulfilled` or `rejected`. Promise's state can also be `pending` which means it's neither resolved or rejected but still waiting for the given operation to complete its execution.

> **References:**
>
> - [Promise | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

### **7.2 Why do we need a promise?**

`Promises` are used to handle asynchronous operations.

> **References:**
>
> - [Promise | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

### **7.3 List all states of a promise?**

`Promise` has three states:

- `pending` is the inital state. Neither fulfilled or rejected. Still waiting for execution to be completed.
- `fulfilled` means that the operations were completed successfully.
- `rejected` means that the opeartions have failed.

> **References:**
>
> - [Promise | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

### **7.4 Why do we need callbacks?**

Callbacks are needed to continue the code execution after a certain operation is complete. These operations can be both synchronous or asynchronous.

> **References:**
>
> - [Callback Function | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)

### **7.5 What is a callback hell?**

When we need multiple steps of operations that are dependant on each other, we use callbacks inside callbacks which causes a pyramid-shaped, nested function structure that is called **"callback hell"**

> **References:**
>
> - [Introducing Asynchronous JavaScrirpt | MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing#callbacks)

### **7.6 What is promise chaining?**

Executing two or more asynchronous operations one after another would require us to create a callback hell. In order to solve this problem, we can use **promise chaining** using `.then()` method. `.then()` returns a promise, which could be handled by a callback as well. Instead, we can chain in another `.then()` which would wait for the previous promise to resolve and then execute next call.

**Promise Chaining** provides a more readable and maintainable code structure.

> **References:**
>
> - [Using Promises | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises#chaining)

### **7.7 What is the purpose of using setTimeout?**

**`setTimeOut()`** executes a given callback after certain amount of time.
We can use `setTimeOut` to perform asynchronous operations.

> **References:**
>
> - [setTimeOut() | MDN](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout)

### **7.8 What is the purpose of using setInterval?**

**`setInterval()`** is used to perform a certain task over and over again in a certain frequency.

> **References:**
>
> - [setInterval() | MDN](https://developer.mozilla.org/en-US/docs/Web/API/setInterval)

### **7.9 What is an event loop?**

**Event Loop** is a constantly running process that monitors both the **callback queue** and the **call stack** which is responsible for:

- Executing the code,
- Collecting and processing events,
- Executing queued sub-tasks

> **References:**
>
> - [Event Loop | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)

### **7.10 What is call stack?**

**Call Stack** is a mechanism for an interpreter to keep track of the whole process of code execution including nested functions, asynchronous operations and such. Call Stack is like a finger to keep track of position on a page while reading.

> **References:**
>
> - [Call Stack | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)

---

## **8. Common**

### **8. 1 How do you validate an email in javascript?**

An e-mail validation can be set up using `RegEx` and check if the given input is passing the `RegEx` rules set for an email.

### **8. 2 What are modules?**

A module in JavaScript is just another JavaScript file that can perform certain tasks which can be imported and exported through the system.

Those modules can be built-in modules, external modules and custom developed modules.

> **References:**
>
> - [JavaScript Modules | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)

### **8. 3 Why do you need modules?**

**Modules** allow us to break up our code into smaller pieces which makes the code more maintainable and cleaner.

> **References:**
>
> - [JavaScript Modules | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)

### **8. 4 What is a rest parameter?**

**Rest Parameter** allows a function to take infinite number of arguments which can be implemented by `...` syntax and given arguments will be stored in an array.

**P.S.:** Rest parameter can be used after a certain number of arguments for the unknown value of arguments

> **References:**
>
> - [Rest Parameters | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters)

### **8. 5 What is a spread operator?**

**Spread Operator** does the reverse of [rest parameter](#8-4-what-is-a-rest-parameter), allows us to turn an iterable, like `Array` or `String`, into a list of arguments. Spread Operators can be used in the function calls to create a list of arguments from an iterable

> **References:**
>
> - [Spread Syntax | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

### **8.6 What is NodeJs?**

**NodeJS** is an open-source, cross-platform, asynchronous event-driven JavaScript runtime.

> **References:**
>
> - [NodeJS.org](https://nodejs.org/en/about/)

---

## **9. Browser API**

### **9. 1 What is the difference between window and document?**

**window** object is the main JavaScript object which is also can be called `global object` in a browser. On the other hand, **document** is actually a property of global window object which represents the visual (rendered) structure inside the global window object known as [**DOM (Document Object Model)**](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)

> **References:**
>
> - [Window | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Window)
> - [Window.document | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Window)

---

## **Week 2**

---

## **1. Data Types**

### **1. 12 Explain what a `Symbol` is in JavaScript?**

`Symbol` is a primitive type that is used for creating unique property keyts to an object

> **References:**
>
> - [Symbol | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)

### **1. 13 How do you check whether a string contains a substring?**

There are two methods to check if a string contains a certain substring.

- `.includes()` method returns `true` or `false` depending on if the string it's called on contains the given argument.

- `.indexOf()` method retunrs the index of the given argument where it first appears.

> **References:**
>
> - [`String.prototype.includes()` | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes)
> - [`String.prototype.indexOf()` | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf)

---

## **2. Objects, Classes, Prototypal inheritance**

### **2. 4 How do you check if a key exists in an object?**

`hasOwnProperty()` method or `in` operator can be used to check if a key exists in an object.

- `hasOwnProperty()` method returns `true` or `false` depending on if the given string or symbol is a key of the object that it's called on.

- `in` operator also returns a boolean value which is either `true` or `false`. The only difference it has from `hasOwnProperty()` method is, `in` operator also checks the objects that we call `in` on inherits from.

> **References:**
>
> - []()

### **2. 5 What is the main difference between Object.values and Object.entries method?**

> **References:**
>
> - [How To Check If A `key` Exists In Object | freeCodeCamp.org](https://www.freecodecamp.org/news/how-to-check-if-an-object-has-a-key-in-javascript/)

### **2. 6 How can you get the list of keys of any object?**

`.keys()` method returns an array of strings which are the keys of the object that it is called on.

> **References:**
>
> - [Object.keys() | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)

### **2. 7 What is a WeakSet?**

`WeakSet` object lets us to store collections of objects and objects only where each object must be unique.

> **References:**
>
> - [WeakSet | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet)

### **2. 8 What are the differences between WeakSet and Set?**

- `WeakSet` can store only `object` where `Set` can store any type.
- References to object in a `WeakSet` are held weakly. Which means, if there is no other reference to an object in a `WeakSet`, that object will be lost after its use and will be garbage collected unlike the values stored in a `Set`
  > **References:**
  >
  > - [WeakSet | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet)

### **2. 9 What is a WeakMap?**

`WeakMap` is a collection of key/value pairs where keys must be an object. Like `WeakSet`, `WeakMap` also doesn't create a strong reference to its keys.

> **References:**
>
> - [WeakMap | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)

### **2. 10 What are the differences between WeakMap and Map?**

`WeakMap` doesn't allow any method for retrieving its keys and their keys are not enumerable, unlike `Map`. Therefore, its keys can be garbage collected after all references to its keys are lost.

> **References:**
>
> - [WeakMap | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)

### **2. 11 What is the difference between proto and prototype?**

`__proto__` is the property that is added by default for any object that is used for lookup in the prototype chain to resolve methods and it points to the `prototype` of the object which is used to build `__proto__` when an object created with `new` keyword.

> **References:**
>
> - [`__proto__` vs Prototype in JavaScript | StackOverflow](https://stackoverflow.com/questions/9959727/proto-vs-prototype-in-javascript)

---

## **3. Context, Scope and Closure**

### **3. 11 What are the problems with global variables?**

Global variables can cause variable collisions in JavaScript when working on large scale projects since it's not a strongly typed language.

Global variables clutter up the golobal namespace and slower to lookup than the local varaibles.

> **References:**
>
> - [Why It Is A Bad Idea To Use Global Variables in JavaScript | Medium ](https://medium.com/@kumar.pranjal123fgiet/why-it-is-a-bad-idea-to-use-global-variables-in-javascript-d8028d1da04f)

### **3. 12 That is the Funarg problem?**

**Funarg** problem occurs when a function calls another function, and the nested functions body refers directly to the variables defined in the scope that function is defined.

**Funarg** problem is basically a scope problem that we can solve using closures.

> **References:**
>
> - [Funarg Problem | Wikipedia](https://en.wikipedia.org/wiki/Funarg_problem)

### **3. 13 How does 'this' work in the arrow functions?**

**Arrow functions** does not bind `this` in its local content. They point to the surrounding scope of where they're defined

> **References:**
>
> - [this | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

---

## **4. JSON**

### **4. 4 Why do you need JSON?**

\*\*JSON (JavaScript Notation Object) format is used for trasmitting structured data over a network.

> **References:**
>
> - [Working with JSON | MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)

---

## **5. Array methods**

### **5. 3 What is the purpose of the array slice method?**

`.slice()` method returns a shallow copy of a portion of an array. The original array is not mutated but the returned copy is a modified verison with the given arguments.

> **References:**
>
> - [`Array.prototype.slice()` | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)

### **5. 4 What is the purpose of the array splice method?**

`.splice()` changes the content of an array by either removing or replacing existing elements and adding new elements

> **References:**
>
> - [`Array.prototype.splice()` | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)

### **5. 5 List arrays methods, that mutate source array?**

`pop()`, `push()`, `shift()`, `unshift()`, `reveerse()`, `sort()`, `splice()`

> **References:**
>
> - [Mutable & Immutable Array Methods in JavaScript](https://www.sitepoint.com/immutable-array-methods-javascript/)

### **5. 6 List arrays methods, that return new array?**

`slice()`, `concat()`, `map()`, `filter()`

> **References:**
>
> - [Mutable & Immutable Array Methods in JavaScript](https://www.sitepoint.com/immutable-array-methods-javascript/)

---

## **6. Functions**

### **6. 5 What is a first class function?**

A programming language is said to have 'first class functions' when functions are treated like any other varaible and can be passed as an argument or returned as a result of another funcftion

> **References:**
>
> - [First Class Function | MDN](https://developer.mozilla.org/en-US/docs/Glossary/First-class_Function)

### **6. 6 What is a first order function?**

> **References:**
>
> - [First Class Function](#6-5-what-is-a-first-class-function)

### **6. 7 What is a Higher order function?**

A function which takes other functions as argument or a function returning another function is called **Higher Order Function**

> **References:**
>
> - [First Class Function | MDN](https://developer.mozilla.org/en-US/docs/Glossary/First-class_Function)

### **6. 8 What is a unary function?**

**Unary Functions** are the functions that takes only one argument.

> **References:**
>
> - [Unary Function](https://en.wikipedia.org/wiki/Unary_function)

### **6. 9 What is the currying function?**

Currying function is a transformed version of a normal function with arguments. It helps to run partial calls on functions when needed.

Transforms `regularFn(a, b ,c)` into `curryFn(a)(b)(c)`

> **References:**
>
> - [Currying | JavaScript.info](https://javascript.info/currying-partials)

### **6. 10 What is an anonymous function?**

**Anonymous functions** are functions that has not been given a name. They're usually used for the tasks that we would not call over and over again.

> **References:**
>
> - [JavaScript Anonymous Functions](https://www.geeksforgeeks.org/javascript-anonymous-functions)

---

## **7. Async JavaScript**

### **7. 11 What does promise.all method do?**

`Promise.all()` method takes an array of promises and resolves when all provided promises are resovled and returns all the values in an array. `Promise.all()` is rejected when any of the provided promises rejects and returns the reject value

> **References:**
>
> - [Promise.all() | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all)

### **7. 12 What is the differance between promise.all and promise.allSettled?**

`Promise.all()` gets a rejected state immediately when any of the given promises is rejected. However, `Promise.allSettled()` is always resolved and returns the completed state of given promises.

> **References:**
>
> - [`Promise.all() `| MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all)
> - [`Promise.allSettled()` | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/allSettled)

### **7. 13 What is the purpose of race method in promise?**

`Promise.race()` takes an array as an argument and returns the first value of the promise that is settled. It can be used to get the fastest resolving result of multiple promises.

> **References:**
>
> - [`Promise.race()` | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/race)

---

## **8. Common**

### **8. 7 What is a strict mode in javascript?**

**Strict mode** can be enabled with `'use strict'` phrase at the top of the file. Strict mode enables JavaScript to throw errors where the silent JavaScript errors occur.

> **References:**
>
> - [Strict Mode | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)

### **8. 8 What are PWAs?**

**PWA (Progressive Web App)** is a web app that uses number of specific technologies and standart patterns to take advantage of both web and native app features.

> **References:**
>
> - [Progressive Web Apps (PWAs) | MDN](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)

### **8. 9 What is memoization?**

**Memoization** is an optimization technique. It's really similar to `caching`. Memoization, stores the output value of a function and stores it in the `cache`. If the value is required again, JavaScript first checks the cache and returns the value if exists.

> **References:**
>
> - [What is Memoization? | freeCodeCamp.org](https://www.freecodecamp.org/news/memoization-in-javascript-and-react/)

### **8. 10 How do you encode an URL?**

`encodeURIComponent()` or `encodeURI()` functions encode a URI by replacing certain characters with their UTF-8 representations.

`encodeURI()` can't form HTTP Requests and have limitations for certain characters.

> **References:**
>
> - [encodeURI() | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/encodeURI)
> - [encodeURIComponent() | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/encodeURIComponent)

### **8. 11 How do you decode an URL?**

`decodeURI()` or `decodeURIComponent()` functions can be used to decode URIs encoded with `encodeURI()` or `encodeURIComponent()` functions respectively.

> **References:**
>
> - [decodeURI() | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/decodeURI)
> - [decodeURIComponent | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/decodeURIComponent)

---

## **9. Browser API**

### **9. 2 How do you get the current url with javascript?**

`window.location.href` property can be used to get the current url.

> **References:**
>
> - [location.href | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Location/href)

### **9. 3 What is a Fetch API?**

**Fetch API** provides a way to fetching resources using JavaScript. It's similar to `XMLHTTPRequest` but with more powerful and flexible features.

It can be used with the `fetch()` function which returns a promise that resolves to the response to the request to the given path.

> **References:**
>
> - [Fetch API | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

### **9. 4 How to open two-way interactive session between browser and server?**

**WebSocket API** makes it possible to open a two-way interactive communication between the client and the server.

> **References:**
>
> - [Websocket API (WebSockets) | MDN](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)

### **9. 5 How to abort async operation?**

`AbortController` interface represents a controller object which makes it possible to abort web requests when needed.

`.abort()` method of `AbortController` can be used to abort a DOM request before it has completed.

> **References:**
>
> - [AbortController | MDN](https://developer.mozilla.org/en-US/docs/Web/API/AbortController)

---

## **Week 3**

## **2. Objects, Classes, Prototypal inheritance**

## **2. 12 How do you create an object with prototype?**

`Object.create()` method can be used to create a new object using an existing objet as a prototype.

> **References:**
>
> - []()

## **2. 13 What is a proxy object?**

> **References:**
>
> - [`Object.create()` | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create)

## **4. JSON**

## **4. 5 How do you define JSON arrays?**

**JSON Arrays** can be defined by using square brackets (`[..]`)

> **References:**
>
> - [JSON | MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)

## **8. Common**

## **8. 12 What is tree shaking?**

**Tree shaking** is a term that is used for removal of dead code which depends on the module system and checks if the modules are imported or exported between JavaScript files.

> **References:**
>
> - [Tree Shaking | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Tree_shaking)

## **8. 13 How do you detect javascript disabled in the page?**

We can set up `<noscript>` tag in our HTML file to prompt a certain content to detect if JavaScript is disabled.

> **References:**
>
> - [`<noscript>` element | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/noscript)

## **9. Browser API**

## **9. 6 How do you detect a mobile browser?**

`navigator.userAgentData` object has a property called `mobile` which has a value of a boolean. We can use that property's value to detect if a browser is mobile or not.

> **References:**
>
> - [`Navigator.userAgentData | MDN`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/userAgentData)

## **9. 7 How can we draw something in the browser?**

**Canvas API** provides functionality of drawing graphics via JavaScript and HTML `<canvas>` element.

> **References:**
>
> - [Canvas API | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

## **9. 8 How to copy value to the clipboard?**

Using **Clipboard API**, we can have access to clipboard functions. `clipboard.writeText()` method allow us to take a value from a DOM element and save it.

> **References:**
>
> - [Clipboard.writeText() | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard/writeText)

## **9. 9 How to read value from the clipboard?**

Using **Clipboard API**, we can have access to clipboard functions. `clipboard.readText()` method allow us to read a value that exists in the clipboard.

> **References:**
>
> - [Clipboard.readText() | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard/readText)
