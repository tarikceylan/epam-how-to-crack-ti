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

<!--- It is incorrect to say "have their bindings to", better to omit word "bindings to" -->
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
<!--- Wants to see more info about structure of async/await, their built from promises and generators -->
> `async/await` provides a way for more readable and maintainable (cleaner) code compared to `Promise`. It's just a wrapper to restyle our code.

---

## **2. Node.js**

## **2. 1. Node.js Structure**

### **1. Feedback**

> Might be doubts on where event loop and async operations are running

**Answer:**
<!--- Provide more info about async operations, different queues and etc -->
> Event loop runs on the single-thread within Node.js process.
> Async operations are sent to libuv by event loop and handled by libuv

---

## **2. 2 NPM**

### **1. Feedback**

> Doesn't seem to know about package linking (npm link)

**Answer:**

> `npm-link` is used for package linking which is a two step process.
>
> - **Step 1:** a symlink gets created with `npm-link`
> - **Step 2:** package name is provided as `npm-link <package_name>`

This process allows us to work on both application and the dependancy at the same time

### **2. Feedback**

> may be doubts on checking for available package upgrades

**Answer:**

> To check available updates for our packages, we can use `npm-check-updates` package.
> To see outdated packages, we can use `npm outdated`
> To update outdated packages manually, we can use `npm update`

---

## **2. 3 Event Loop**

### **1. Feedback**

> Might be doubts on microtasks

**Answer:**
  <!--- What is the order of executing marco/micro tasks? -->
> **Microtasks** are the tasks that needs to be executed asynchronously and they have a higher priority over **macrotasks**

---

## **2. 4 I/O Operations in Node.js**

### **1. Feedback**

> Might be doubts on related blocking/non-blocking operations being fast/slow in comparison

**Answer:**
  <!--- Why sync operation faster when async? -->
> Generally, blocking(sync) operations are faster than the async operations. Depending on the data that I/O operation would be performed or the behaviour we want (e.g. being have to validate a certificate), we could prefer to use synchronous operation. Otherwise, when we're working with an API or an external resource within a network, non-blocking(asynchronous) operations should be used in order to not to block the event loop even though they might be slower

### **2. Feedback**

> Couldn't find cases for sync operations usage

**Answer:**

> reading/writing a small piece of data from/onto disk would be a good case to use synchronous operation.

---

## **2. 5 Node.js Core Modules**

### **1. Feedback**

> Doubts on Using common js vs es modules (f.e. in one project)

**Answer:**

> CommonJS modules and ES Modules can be used in the same project. CommonJS modules can still be imported with ES Modules `import` keyword as long as `type: module` is not used in `package.json`. Instead, we can just use `.mjs` file extension for ES Modules

---

## **2. 6 Streams**

### **1. Feedback**

> Doubts about Transform streams, zipping/encrypting

**Answer:**

> **Transform streams** allow us to modify the data as it is being read or written. For example; `zlib.createGzip` stream can compress the data using gzip.

---

## **2. 7 RDBMS, SQL, PostgreSQL**

### **1. Feedback**

> Normalization, Deeper knowledge on Lock Levels

**Answer:**

> **Normalization** is the process of organizing the data in the database to minimize the redundancy from a relation or to eliminate the anomalies.

---

### **2. 9 Testing**

### **1. Feedback**

> FIRST principles — some doubts on details

**Answer:**

> **FIRST** principles stand for:
>
> - **FAST** indicates that unit tests should be able to be ran at any time during development cycle regardless of the test count, and should provide feedback or desired output in the matter of seconds.
>
> - **ISOLATED** indicates any given unit test should be independent from any other part of the software as well as its results.
>
> - **REPEATABLE** means that the tests must be repeatable and their values shouldn't change for different environments while being independant from any external condition.
>
> - **SELF-VALIDATING** means that it shouldn't need any manual interaction.
>
> - **THROUGH** indicates that the test should cover all cases including illegal input, security issues and so on while having a %100 code coverage.

### **2. Feedback**

> Couldn't explain Given/When/Then pattern

**Answer:**

> **Given-When-Then** pattern is a style of representing tests.
>
> - **'given'** represents the behaviour.
> - **'when'** represents the action that needs to be completed.
> - **'then'** represents the expected outcome.

---

### **2. 10 REST**

### **1. Feedback**

> Doubts about REST Levels

**Answer:**

> Levels of a REST API is defined by [**Richardson Maturity Model**](https://restfulapi.net/richardson-maturity-model/)
>
> According to this model, there are four levels of maturity for a REST API:
>
> - **Level 0** services have a single URI and uses a single HTTP Method
> - **Level 1** services uses multiple URIs but single HTTP Method
> - **Level 2** services uses multiple URIs and HTTP Methods but doesn't use HATEOAS
> - **Level 3** services uses all three: Multiple URIs, HTTP Methods and HATEOAS

### **2. Feedback**

> what makes API RESTful

**Answer:**
A system that complies some or all of the following guideline constraints is considered RESTful

> - **Uniform Interface**
    >   APIs interface for the resources should be consistent within the system. Resources should only have one logical URI which provides a way to fetch related data.
> - **Stateless**
    >   All client-server interactions should be stateless. The server shouldn't store anything about the previous requests and treat each request as a new one. No client context should be stored for the next request except authentication and authorization information required for services.
> - **Cachable**
    >   Caching should be applied wherever its applicable. Caching improves scalability and performance by eliminating some client-server interactions.
> - **Client-Server**
    >   Client and Server shouldn't depend on each other. They must be replaced and developed independently when needed.
> - **Layered System**
    >   REST allow to use layered sytstem architecture. API server can be deployed on a different server than the server that stores the data and so on.
> - **Code On Demand** (optional)
    >   Most of the time a static representation of a resource will be sent. But returning executable code to support part of the application is also possible.

---

## **2. 11 NoSQL, MongoDB**

### **1. Feedback**

> Doubts on Vertical vs. Horizontal scaling of DBs

**Answer**
<!--- We can't say that NoSQL databases scaled only horizontally and SQL - vertically -->
> - **Horizontal Scaling** is based on partitioning the data between different phyiscal resources where as **Vertical Scaling** depends on a single physical resource.
> - NoSQL Databases are scaled horizontally, whereas SQL databases scaled vertically as long as there is no sharding.

---

## **3. TypeScript**

## **3. 1 TypeScript Infrastructure**

### **1. Feedback**

> Doubts on components of TS (didn't mention language services)

**Answer:**

> TypeScript is iternally divided into three main layers:
>
> - **Language** is where language specific syntax and keywords are defined.
> - **TypeScript Compiler** is a configurable, internal compiler of TypeScript which converts TypeScript code into JavaScript code. During the conversion it also >performs operations like type checking and parsing.
> - **TypeScript Language Services** provides information to help editors and other tools about the structure of language.

---

## **3. 2 Access Modifiers**

### **1. Feedback**

> Doubts on protected access, Abstract classes

**Answer:**

> - In TypeScript, `protected` members are only visible to subclasses of the class they're declared in.
>
> - **Abstract Classes** serve as a base class for subclasses which implements all abstract members.

---

## **3. 3 Utility Types**

### **1. Feedback**

> Could only mention Awaited

**Answer:**

> - `Awaited` is used for handling async operations like `async` and `await`, or `.then()` method on `Promise`s.
> - `Partial` is used for constructing types where all properties of the type is set to optional.
> - `Required` is used for constructing types where all properties of the type is set to required (the opposite of `Partial`)
> - `Readonly` is used for constructing types where all properties are `readonly` which means they can't be re-assigned

---

## **3. 4 Advanced Typing**

> Basic knowledge of interfaces and types; no details on difference

**Answer:**
   <!--- There are more differences between Interfaces and Types -->
> `interface` can be extended by declaring it a second time, whereas `type` can not. `type` can not be changed outside of its declaration
