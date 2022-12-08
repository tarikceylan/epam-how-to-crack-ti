# **Work With The Feedback: Dry-Run Interview #2**

## **1. JavaScript**

## **1. 1 Scope**

### **1. Feedback:**

> Forgot how to set default values to function params

**Answer:**

> Default parameters can be set by assigning a value with `=` > **Example:**
>
> ```javascript
> function multiply(a, b = 2) {
>   return a * b;
> }
>
> multiply(5); // will return 10 by assigning value of 2 as a default for `b`
> ```

### **2. Feedback:**

> blurry explaining of block/function scopes

**Answer:**

> - **Block scope** means that the variable is only accessible within the **block** which it's declared.
> - **Function scope** means that the variable is only accessible within the **function** which it's declared
>
> **Example:**
>
> ```javascript
> function myfunc() {
>   let a = 5;
>   if (a === 5) {
>     let b = a;
>   }
>   console.log(b); // returns b is not defined. `b` is block scoped inside the `if` statement so is not accessible from the function scope.
> }
> ```

### **3. Feedback:**

> confusion around closures - how they work

**Answer:**

> **Closures** allow us to access outer function's scope from an inner function, evene after the outer function has returned.
>
> **EXAMPLE:**
>
> ```javascript
> function outerFn() {
>   let name = 'John';
>   console.log(`${name} Doe`); // John Doe
>   function innerFn() {
>     name += ' Smith';
>     console.log(name);
>     //Because of closures, name variable is grabbed from the lexical scope
>   }
>   return innerFn;
> }
> const fn = outerFn();
> fn(); // John Smith
> fn(); // John Smith Smith
> ```

### **4. Feedback:**

> how variables are stored (mixing with prototype chains)

**Answer:**

> Variables are stored in **lexical environment**. If a variable that needs to be accessed can't be found in an inner lexical environment, the outer lexical environment is searched and the next outer lexical environment and so on until the search has reached the global lexical environment.

## **1. 2 Strict Mode**

### **1. Feedback:**

> Said that semicolons are required in strict mode

**Answer:**

> Strict Mode can be invoked `"use strict"` decleration which enables us to write safer JavaScript code.
>
> Strict Mode makes several changes on normal JavaScript behaviour
>
> - Eliminates some JavaScript silent errors by changing them to throw errors.
> - Fixes mistakes that make it difficult for JavaScript engines to perform optimizations: strict mode code can sometimes be made to run faster than identical code that's not strict mode.
> - Prohibits some syntax likely to be defined in future versions of ECMAScript.
>
> Some of the limitations that strict mode enables are as follows:
>
> - Assigning values to variables without declaring them (e.g. `x = 5` or `obj = {x: 10, y: 5}` will throw an error)
> - Duplicate parameter names are not allowed (e.g. `function(x, x){// ...}`)
> - `eval` and `arguments` keywords can not be used as variable names
>   and so on...

## **1. 3 PWA**

### **1. Feedback:**

> Blurry understanding, couldn't explain, Mixing with compatibility with mobile devices

**Answer:**

> **PWA (Progressive Web App)** is a web app that uses number of specific technologies and standart patterns to take advantage of both web and native app features.
> For a web application to be considered as **PWA**, it should have the following properites:
>
> - **Discoverable**, so the contents can be found through search engines.
> - **Installable**, so it can be available on the device's home screen or app launcher.
> - **Linkable**, so you can share it by sending a URL.
>   Network independent, so it works offline or with a poor network connection.
> - **Progressively enhanced**, so it's still usable on a basic level on older browsers, but fully-functional on the latest ones.
> - **Re-engageable**, so it's able to send notifications whenever there's new content available.
> - **Responsively designed**, so it's usable on any device with a screen and a browser—mobile phones, tablets, laptops, TVs, refrigerators, etc.
> - **Secure**, so the connections between the user, the app, and your server are secured against any third parties trying to get access to sensitive data.

## **2. Node.JS**

## **2. 1 Encoding vs Encryption vs Hashing**

### **1. Feedback**

> Incorrect understanding of hashing (said it's reversible), provided no use-cases for hashing

**Answer:**

> **Hashing** is the process of ensuring the integrity of the information. Data that will be sent over a network can be hashed using a hashing algorithm which would create a string in a fixed length from the given string.
>
> A common use-case for hashing in web apps would be password verification.

## **2. 2 Monitoring and Logging**

### **1. Feedback**

> Incorrect understanding of health checks, their implementation. Mixing health checks and logging

**Answer:**

> **Health Check** is a review of QA processes which involves a thorough investiagion of testing process, tools metrics and the team.
>
> We use health check to identify the efficiency or the open to improvement parts of the system, whereas **logging** can be used to detect attacks, application misuse or errors that makes our system unavailable and so on.

### **3. Feedback**

> no idea about correlation/tracing IDs

**Answer:**

> **Correlation IDs/Trace IDs** are unique identifiers that link the log messages together to track a specific request or operation as it flows through the system.

## **2. 3 NestJS**

### **1. Feedback**

> Couldn’t say anything

**Answer:**

> NestJS is a framework for building, efficient and scalable Node.js server-side applications. NestJS is built with and fully supports TypeScript.
>
> Three key components of NestJS
>
> - **Controllers** are responsible for handling incoming requests and responding to the application’s client-side.
> - **Modules** are used to structure code and separate functionality into logical, reusable chunks.
> - **Providers or services** which abstract complexity and logic away from the user. It’s possible to inject the service into controllers or other services.

## **2. 4 GraphQL**

### **1. Feedback**

> Couldn't name drawbacks of GraphQL

**Answer:**

> - Caching Implementation complexity
> - Query Complexity with nested fields
> - Rate Limiting implmentation

## **2. 5 Software Design**

### **1. Feedback**

> Event-driven architectures mixed with Event Emitter

**Answer:**

> **Event Driven Architecture** is asoftware architecture and model for application design which is based on production and consumption of events where the event is transmitted between producers and consumers. `Event emitter` class is the core component of event-driven architecture in Node.js

### **2. Feedback**

> Blurry explainations of microservice architectures, their details

**Answer:**

> Microservice architecture is an architectural style that structures an application as a collection of services that are
>
> - Highly maintainable and testable
> - Loosely coupled
> - Independently deployable
>
> The microservice architecture enables the rapid, frequent and reliable delivery of large, complex applications. It also enables an organization to evolve its technology stack.

### **3. Feedback**

> Blurry understanding of event buses

**Answer:**

> An **Event Bus** is the mediator that transfers a message from a **sender** to a **receiver**. They provide a loosely coupled communications between services

### **4. Feedback**

> Mixing 3-tier Web-applications vs Layered architectures;

**Answer:**

> **3-tier Web Application** is an application where the application is divided into three main layers.
>
> - **Presentation Tier (Physical)** where the user interface live and interaction with the user happens.
> - **Application Tier (Logical)** where the data is processed and business logic executes
> - **Data Tier (Phyiscal)** where the data is stored and managed.

---

> **Layered Architecture** is a pattern where each layer is responsible of a specific functionality within the system. Most layered architectures consists of four standard layers
>
> - **Presentation** is responsible for handling the user interface and interaction.
> - **Business** is responsible for business logic and validations.
> - **Persistence** is responsible for interacting with the database also known as data access layer
> - **Database** is responsible for data storage which consists the database technology and cod to access and handle database.

---

> **Difference between 3-Tier Architecture and Layered Architecture**
>
> - In **Layered Architecture**, the **Database Access Layer (DAL)**, **Business Logic Layer (BLL)** and **User Interface Layer (UIL)** resides different project and the output of these projects must be together in the same server or on same machine in order for the system to run.
> - However in **3-Tier architecture**, the **Database Access Layer (DAL)**, **Business Logic Layer (BLL)** and U**ser Interface Layer (UIL)** reside as 3 different projects. But each of the projects can be deployed at the different server or at the different machines and distributed functionality is explored.

### **6. Feedback**

> OOP principles — missed some details, blurry understanding of inheritence and polymorphism

**Answer:**

> - **Abstraction** is protecting the inner details of a class from the others which use it.
> - **Encapsulation** is hiding the certain data behind access methods.
> - **Inheritance** is creating reusable classes without affecting the original.
> - **Polymorphisim** is the ability of an object to take may forms.

## **2. 6 Security Threats**

### **1. Feedback**

> Blurry about prevention of SQL-query injections;

**Answer:**

> There are few ways to prevent an SQL Injection. Some of them as follow:
>
> - Do not insert raw input into a query string, use placeholders.
> - Validate user input

### **2. Feedback**

> Blurry about how .env file works, evniron,ment variables, how to set secrets in PROD

**Answer:**

> `.env` file provides a way to store secrets and defines environment variables in our system.

The environment variables are stored in the node process that is running on production environment, so they can be read from `process.env`.

## **3 TypeScript**

### **1. Feedback**

> Decided to skip TS questions as no much more knowledge since last time

**Answer:**

> TypeScript is a language that I need to have more practice on. I believe I'm familiar with the very basics and the need for it but I'll need to practice to understand its components and structure more in-depth.
