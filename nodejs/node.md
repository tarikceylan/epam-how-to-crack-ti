# **NodeJS Interview Questions**

## **Week 1**

---

## **1. NodeJS**

### **1.1 What is NodeJS?**

**NodeJS** is an open-source, cross-platform, asynchronous event-driven JavaScript runtime.

> **References:**
>
> - [NodeJS.org](https://nodejs.org/en/about/)

### **1. 2 What is package.json?**

**package.json** holds various metadata about the project which is used to give information to [npm](//todo) about the project itself, its dependencies and their versions

> **References:**
>
> - [What is the file `package.json`?](https://nodejs.org/en/knowledge/getting-started/npm/what-is-the-file-package-json/)

### **1. 7 How Event Loop works?**

**Event Loop** constantly monitors and listens on call stack and callback queue. If the call stack is empty, the event loop will call the next operation from the callback queue and push it to the call stack. This iteration is called a tick in the event loop and it goes on until execution of the whole file is complete

> **References:**
>
> - []()

### **1. 8 Is NodeJS entirely based on a single-thread?**

**No.** NodeJS uses "Single Threaded Event Loop Model" architecture to handle multiple operations. However, libuv works multi-thread behind the scene.

> **References:**
>
> - [Is NodeJS Single Threaded or Multi Threaded?](https://dev.to/arealesramirez/is-node-js-single-threaded-or-multi-threaded-and-why-ab1)

### **1. 10 What kind of streams does NodeJS have?**

- **Writable** streams are the streams that data can be written on.
- **Readable** streams are the streams that data can be read from.
- **Duplex** streams are both `readable` and `writeable` streams.
- **Transform** streams are `Duplex` streams that can modify the data while being written and read.

> **References:**
>
> - [Stream | NodeJS.Org](https://nodejs.org/api/stream.html)

---

## **2. Dealing With Async Code**

### **2. 1 How do you understand the Callback Pattern? What is a callback hell?**

**Callback Pattern** is achieved by providing a function into another function as an argument. The completion of the outer function depends on the callback function that is given. It's a way to ensure a certain operation is complete before the main functionality gets executed.

When we have multiple callbacks that are dependant on each other, the application of the callback pattern eventually cause a pyramid-shaped, nested structure which is called **callback hell**

> **References:**
>
> - [Introducing Asynchronous JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing)

### **2. 2 What is a Promise?**

`Promise` object represents a template for a value that is not yet set. The eventual value depends on the state of the `Promise` object which can be `fulfilled` or `rejected`. Promise's state can also be `pending` which means it's neither resolved or rejected but still waiting for the given operation to complete its execution.

> **References:**
>
> - [Promise | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

### \*\*2. 3 What states does the Promise have? Can the state be changed once it was fulfilled or rejected?

`Promise` has three states:

- `pending` is the inital state. Neither fulfilled or rejected. Still waiting for execution to be completed.
- `fulfilled` means that the operations were completed successfully.
- `rejected` means that the opeartions have failed.

No. Although, if a `promise` returns another `promise` once it's fulfilled or rejected, the final state can be changed by returning another state from the next `promise`. Otherwise, state can not be changed.

> **References:**
>
> - [Promise | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

---

## **3. Express**

### **3. 1 What are the purpose of middlwares in Express?**

**Middlewares** allow us to modify `request` and `response` object to provide extra functionality or to perform certain tasks on the fly.

> **References:**
>
> - [Using Middleware | Express](https://expressjs.com/en/guide/using-middleware.html)

---

## **6. Testing**

### **6. 1 What is a test pyramid? How can you implement it regarding HTTP APIs?**

**Test pyramid** is a framework that determines the order and frequency of tests for each layer of a a software. Provides useful insight for a successful development process.

**Implementation of a test pyramid for HTTP APIs** could follow these steps:

- **Unit Tests** should be performed on smallest, testable piece of code.
- **Integration Tests** should cover any API integration with 3rd pary services.
- **End-To-End Tests** should cover all actions that an end-user could take using our API.

> **References:**
>
> - [What is Testing Pyramid](https://www.headspin.io/blog/the-testing-pyramid-simplified-for-one-and-all)

### ** 6. 5What is Unit-testing? What are the FIRST principles?**

**Unit Testing** is the process of testing the smallest, testable piece of code.

**FIRST** principles stand for:

- **FAST** indicates that unit tests should be able to be ran at any time during development cycle regardless of the test count, and should provide feedback or desired output in the matter of seconds.

- **ISOLATED** indicates any given unit test should be independent from any other part of the software as well as its results.

- **REPEATABLE** means that the tests must be repeatable and their values shouldn't change for different environments while being independant from any external condition.

- **SELF-VALIDATING** means that it shouldn't need any manual interaction.

- **THROUGH** indicates that the test should cover all cases including illegal input, security issues and so on while having a %100 code coverage.

> **References:**
>
> - [F.I.R.S.T Principles of Testing | Medium](https://medium.com/@tasdikrahman/f-i-r-s-t-principles-of-testing-1a497acda8d6)

---

## **7. Software Design**

### **7. 1 REST API: What is it?**

**REST API** is an application programming interface which follows REST architectural style and allows interaction with RESTful web services.

> **References:**
>
> - [What is a REST API? | RedHat](https://www.redhat.com/en/topics/api/what-is-a-rest-api)

### **7. 1. 3 REST API: Name the main Http methods. What is the difference between Put and Patch?**

Main HTTP Methods are as follow:

- **GET**
- **POST**
- **PUT**
- **PATCH**
- **DELETE**

Difference between `PUT` and `PATCH` is:

`PUT` request modifies and replaces the entire data with the modified version, where `PATCH` request only modifies a portion of the data without modifying entire data.

> **References:**
>
> - [PATCH vs PUT in REST API](https://josipmisko.com/posts/patch-vs-put-rest-api)

### **7. 2 Explain the MVC model?**

**MVC** stands for Model-View Controller which is an architectural design pattern used to implement seperation of business logic, display and data.

> **References:**
>
> - [MVC | MDN](https://developer.mozilla.org/en-US/docs/Glossary/MVC)

### **7. 4 Name the key principles of OOP?**

- **Abstraction** is protecting the inner details of a class from the others which use it.
- **Encapsulation** is hiding the certain data behind access methods.
- **Inheritance** is creating reusable classes without affecting the original.
- **Polymorphisim** is the ability of an object to take may forms.

> **References:**
>
> - [Four Principles Of OOP | Medium](https://medium.com/@cancerian0684/what-are-four-basic-principles-of-object-oriented-programming-645af8b43727)
> - [Polymorphism Explained Simply | Medium](https://medium.com/@shanikae/polymorphism-explained-simply-7294c8deeef7)

---

## **8. Databases**

## **8. 1 RDBMS (Postgres or MySQL)**

### **8. 1. 0 RDBMS: What is it?**

**An RDBMS (Relational Database Management System)** is a program which is used to create, update, and manage \*_relational databases_

> **References:**
>
> - [What is RDBMS | Oracle](https://www.oracle.com/database/what-is-a-relational-database/)

### **8. 1. 1 How data is stored in RDBMS?**

**RDBMS** stores data in the form of tables created by columns and rows.

> **References:**
>
> - [What is RDBMS | Oracle](https://www.oracle.com/database/what-is-a-relational-database/)

### **8. 1. 6 How tables can be joined?**

Tables can be joined using **SQL Joins**. There are few different types of joins avaialable:

- **JOIN (INNER JOIN)**
- **LEFT OUTER JOIN**
- **RIGHT OUTER JOIN**
- **CROSS JOIN**
- **NATURAL JOIN**

> **References:**
>
> - [JOIN Operations | Oracle](https://docs.oracle.com/javadb/10.6.2.1/ref/rrefsqlj29840.html)

### **8. 1. 8 Explain Transactions and ACID.**

**A transaction** is the work unit that performs single or multiple operations in the database.

**ACID** stands for:

- **Atomicity** indicates that all operations on the data are performed as if they're a single operation. It's either all or none of the changes are performed.
- **Consistency** means that the data is in a **consistent** state when a transaction starts and ends
- **Isolation** indicates that each transaction should be decoupled from another.
- **Durability** ensures that transactions are done and irreversable.

> **References:**
>
> - [Database Transaction | Wikipedia](https://en.wikipedia.org/wiki/Database_transaction)
> - [ACID Properties Of Transactions | IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=processing-acid-properties-transactions)

### **8. 1. 10 What type of indexes do you know? When to use them?**

- **Clustered Index** stores the data in a sorted structure based on arranged order. Can be used for improving performance for searching operations.
- **Filtered Index** allows us to apply certain conditions. Can be used to improve query performance and storage costs
- **Unique Index** ensures that the index key has no duplicate values. Can be used to eliminate duplicate data.

> **References:**
>
> - [RDBMS Indexes | Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/indexes/indexes?view=sql-server-ver16)

### **8. 1. 12 TypeORM**

#### **8. 1. 12. 5 How to change an already defined table structure with TypeORM?**

**Migrations** can be used to update a defined tabled structure in TypeORM. **A migration** is a file that contains SQL queries to update an existing table structure.

> **References:**
>
> - [Migrations | TypeORM](https://typeorm.io/migrations)

## **8. 2 NoSQL DB**

### **8. 2. 1 What is MongoDB?**

**MongoDB** is a scalable, flexible, cross-platform document database which uses JSON-like documents.

> **References:**
>
> - [What is MongoDB? | MongoDB](https://www.mongodb.com/what-is-mongodb)

### **8. 2. 5 How scaling of NoSQL and SQL differs?**

**SQL databases** are **vertically scalable\***, while **NoSQL databases** are **horizontally scalable\*\***.

**\*Vertical scaling** describes adding more power to your current machines. \***\*Horizontal scaling** refers to adding additional nodes,

> **References:**
>
> - [SQL vs NoSQL](https://www.integrate.io/blog/the-sql-vs-nosql-difference)

---

## **9. Security**

### **9. 7 What is JWT? Is it safe to store sensitive information inside JWT?**

**JWT (JSON Web Token)** is an open standard which defines a secure way to transfer data as a JSON Object.

JWT is not encrypted by default. Therefore, it's not safe to store sensitive data in JWT.

> **References:**
>
> [JWT Introduction](https://jwt.io/introduction)

---

## Week 2

---

## **1. Node.js**

### **1. 2 When to use Node.js and when not to use it?**

Node.js is created with scaling I/O operations in mind. Node is great when it comes to intense I/O applications requiring speed and scalability with concurrent connections. Like video streaming, live chat apps etc.

On the other hand, Node.js is not the best option for computational, CPU-heavy tasks.

> **References:**
>
> - [Node.js: why and where to use it? | freeCodeCamp.org](https://www.freecodecamp.org/news/node-js-what-when-where-why-how-ab8424886e2/)

### **1. 5 What is npm?**

**npm (Node Package Manager)** is the default package manager for Node.js. It makes it possible to install packages, manage dependencies and versions of the packages we use.

> **References:**
>
> - [What is `npm` | Nodejs.org](https://nodejs.org/en/knowledge/getting-started/npm/what-is-npm/)

### **1. 6 What is the difference between Sync vs Async operations?**

- **Sync (Synchronous) Operations** are the operations that blocks the execution of the rest of the code. Synchronous operations happen in the order they're written and they work on a single-thread which means only one task can be completed at a time.

- **Async (Asynchronous) Operations** are the operations that runs without blocking the execution of the rest of the code. Async operations are non-blocking. They're sent to v8 engine by the event loop and handled while other tasks are being completed then sent back.

> **References:**
>
> - [Synchronous vs Asynchronous Programming](https://medium.com/linkit-intecs/what-is-synchronous-vs-asynchronous-in-node-js-4b45ee668e6f)

### **1. 11 When Streams can be used in Node.js?**

Streams can be used when we are reading, writing or modifying data over a network or within the system

> **References:**
>
> - [Stream | Nodejs.org](https://nodejs.org/api/stream.html#stream)

### **1. 15 What is a Memory Leak? How to prevent it?**

**Memory Leak** occurs when an unused block of memory is still on the heap managed by v8. Memory Leaks can be caused by global variables which run during the whole execution, multiple references to an object, closures that holds reference to a large object, timers such as setTimeOut, setInterval when their callbacks are not properly handled.

Therefore, we can prevent memory leaks by monitoring the amount of leakage using certain tools, reducing use of global variables, properly using closures and handling timers and events.

> **References:**
>
> - [Avoiding Memory Leaks in Node.js](https://blog.appsignal.com/2020/05/06/avoiding-memory-leaks-in-nodejs-best-practices-for-performance.html)

---

## **2. Dealing With Async Code**

### **2. 4 What are the advantages of the async/await over Promises?**

Usage of `async/await` provides a cleaner and easier to maintain code structure while also providing an easy error handling compared to promises.

> **References:**
>
> - [`async/await vs Promises`](https://dev.to/deadwin19/5-reasons-why-javascript-async-await-over-promises-1if3)

---

## **3. Express.js**

### **3. 1 What is Express.js and what is its use?**

**Express** is a minimalist web application framework for Node.js that provides easier and feature rich ways to build web apps. Express helps managing servers and routes.

> **References:**
>
> - [Expressjs.com](https://expressjs.com/)

### **3. 2 What are the main building blocks of Express.js?**

- **Server** manages the server that the applicataion runs on
- **App** object handles the app itself. It has methods for HTTP requests, configuring middleware, rendering HTML, and registering a template engine.
- **Route** represents an instance of a single route that we can use to handle HTTP verbs with optional middleware
- **Router** object is an isolated
- **Request** represents the object of a request to a resource
- **Response** represents the object the response that is sent from a resource
- **Middleware** represents the object where we can modify request response cycle and give it more functionality.

> **References:**
>
> - [Expressjs.com](http://expressjs.com/)

### **3. 4 What is the use of next in Express.js?**

`next()` function is a function in the express router that invokes the next middleware or route that is implemented.

> **References:**
>
> - [Writing Middlewares | Expressjs.com](https://expressjs.com/en/guide/writing-middleware.html)

---

## **6. Testing**

### **6. 2 What is a Given-When-Then pattern?**

**Given-When-Then** pattern is a style of representing tests.

- **'given'** represents the state of a situation.
- **'when'** represents some action that is to carried out.
- **'then'** represents the expected outcome.

> **References:**
>
> - [GivenWhenThen | MartinFowler](https://martinfowler.com/bliki/GivenWhenThen.html)

### **6. 3 What mocks and stubs are? How are they used in integration testing?**

When writing tests, we need to control the behaviour of our dependencies especially when tehey're external services or APIs. **Test doubles** can be used to control the behaviour. **Mocks** and **Stubs** are test double types.

- **Mocks** are objects that have predefined behaviour. They register calls they receive and provide feedback about how they're used. Mocks also have pre-programmed expectations about how they'll be used

- **Stubs** are objects that return predefined values. Unlike mocks, they're not programmed to expect specific calls. Instead they return values when they're called.

> **References:**
>
> - [Faking vs. Mocking vs. Stubbing](https://www.educative.io/answers/what-is-faking-vs-mocking-vs-stubbing)

---

## **7. Software Design**

### **7. 1. 2 REST API: What constraints does the REST have?**

- **Uniform Interface**
  APIs interface for the resources should be consistent within the system. Resources should only have one logical URI which provides a way to fetch related data.
- **Stateless**
  All client-server interactions should be stateless. The server shouldn't store anything about the previous requests and treat each request as a new one. No client context should be stored for the next request except authentication and authorization information required for services.
- **Cachable**
  Caching should be applied wherever its applicable. Caching improves scalability and performance by eliminating some client-server interactions.
- **Client-Server**
  Client and Server shouldn't depend on each other. They must be replaced and developed independently when needed.
- **Layered System**
  REST allow to use layered sytstem architecture. API server can be deployed on a different server than the server that stores the data and so on.
- **Code On Demand** (optional)
  Most of the time a static representation of a resource will be sent. But returning executable code to support part of the application is also possible.
  > **References:**
  >
  > - [REST Architectural Constraints | RESTfulAPI.com](https://restfulapi.net/rest-architectural-constraints/)

### **7. 1. 4 REST API: What status should be sent in a response to a create object request?**

**201 Created success** status response code should be sent. It indicates that the request has succeeded and has led to the creation of a resource

> **References:**
>
> - [HTTP Status Codes | RESTfulAPI.com](https://restfulapi.net/http-status-codes/)

### **7. 5 What is a dependency injection?**

**Dependency injection** is a design pattern where instead of requiring dependencies directly inside a module, we pass them as reference which would allows us to create more independent and flexible modules

> **References:**
>
> - [Dependency Injection in Node.js](https://tsh.io/blog/dependency-injection-in-node-js/)

### **7. 6 What is a Layered Architecture? Give a few examples**

**Layered Architecture** is a pattern where each layer is responsible of a specific functionality within the system. Most layered architectures consists of four standard layers

- **Presentation** is responsible for handling the user interface and interaction.
- **Business** is responsible for business logic and validations.
- **Persistence** is responsible for interacting with the database also known as data access layer
- **Database** is responsible for data storage which consists the database technology and cod to access and handle database.

For example for a CRUD app;

- **Front-end** code would be the **presentation layer**.
- Endpoints, routing and server code would represent the **business layer**.
- The functions that allow us to perform database queries and modify the data wowuld represent the **persistence layer**
- Where we establish database connection and set configurations, schemas and so on would be **database layer**

> **References:**
>
> - [The Layered Architecture Pattern in Software Architecture | Medium](https://medium.com/kayvan-kaseb/the-layered-architecture-pattern-in-software-architecture-324922d381ad)

---

## **8. Databases**

## **8. 1 RDBMS (Postgres or MySQL)**

### **8. 1. 2 What is a normalization concept?**

**Normalization** is the process of organizing the data in the database to minimize the redundancy from a relation or to eliminate the anomalies.

> **References:**
>
> - [What is Database Normalization?](https://www.guru99.com/database-normalization.html)

### **8. 1. 3 What table relationships do you know? How to create them?**

- **One to One Relationship** is when both tables have only one record that is related.
- **One to Many Relationship** is when one a record in primary table can relate to one or any number of records in the related table.
- **Many to Many Relationship** is when each record on both tables can relate to any number of records in the other table.

We can create relationships by defining fields for primary keys and foreign keys and connecting records in the table with those keys.

> **References:**
>
> - [Database Relationships | IBM](https://www.ibm.com/docs/en/mam/7.6.0?topic=structure-database-relationships)
> - [Relationship in SQL](https://database.guide/create-a-relationship-in-sql/)

### **8. 1. 4 What is the difference between DDL and DML?**

**DDL (Data Definition Language)** is used to define data structures
**DML (Data Manipulation Language)** is used to modify the data.

> **References:**
>
> - [Difference Between DDL and DML](https://www.geeksforgeeks.org/difference-between-ddl-and-dml-in-dbms/)

---

## **8. 2 NoSQL DB**

### **8. 2. 2 How data is orginized in MongoDB?**

**MongoDB** is a document database. It stores record in individual documents and uses `BSON` format to store data. `BSON` is a combination of `binary` and `JSON` which can be considered as a binary representation of JSON documents.

> **References:**
>
> - [Intorduction to MongoDB](https://www.mongodb.com/docs/manual/introduction/)

### **8. 2. 3 What does the BASE stand for?**

**BASE** describes a database processing model and stands for **Basically Available**, **Soft State**, and **Eventual Consistency**

- **Basically Available** guarantees the availability of data.
- **Soft State** means that the state of the system can change over time.
- **Eventual Consistency** states that the system will eventually become consistent once it stops receivng input.

> **References:**
>
> - [NoSQL Databases](https://www.freecodecamp.org/news/nosql-databases-5f6639ed9574/)

### **8. 2. 4 How to make a relationship between Documents in MongoDB?**

There are two ways to implement a relationship between documents in MongoDB:

- **Embedded Document Pattern** is the approach where we embed a document's all related fields into another document.
- **Subset Pattern** is the approach where we partially embed a document into another one but only bringing in the related feilds.
- **Reference** is the approach where we provide a reference to the related document's id.

> **References:**
>
> - [Relationship Between Documents | MongoDB](https://www.mongodb.com/docs/manual/applications/data-models-relationships/)

---

## **9. Security**

### **9. 1 What is the difference among Encoding, Encryption and Hashing?**

- **Encoding** is a technique to transform the data into another format so it could be understood by different systems that can read the sepcified format.
- **Encryption** is a way to keep data secure and confidential. Encryption transforms the data into a meaningless collection of characters by using a key. Eventually, this process makes the data unreadable by third parties.
- **Hashing** is the process of ensuring the integrity of the information. Data that will be sent over a network can be hashed using a hashing algorithm which would create a string in a fixed length from the given string.

> **References:**
>
> - [Difference Between Encoding, Encrypting, and Hashing | Medium](https://medium.com/swlh/the-difference-between-encoding-encryption-and-hashing-878c606a7aff)

### **9. 2 What are the use cases for Encoding, Encryption and Hashing?**

- **Encoding** can be used to transfer data in formats that are readable by the receiving systems. For example: A .docx file being encoded to Base64 before sending it via mail oruploading it on a system
- **Encryption** can be used to transfer confidential or sensitive data
- **Hashing** can be used for whenever we need our data to be kept unchanged and hidden. Like storing passwords

> **References:**
>
> - [Difference Between Encoding, Encrypting, and Hashing | Medium](https://medium.com/swlh/the-difference-between-encoding-encryption-and-hashing-878c606a7aff)

### **9. 5 What is HTTPS? How it works?**

\*\*HTTPS (Hyper Text Transfer Protocol Secure) is used for secure communication over a network or the internet.

HTTPS uses an encryption protocol to encrypt communications known as Transport Layer Security (TLS), or formerly known as Secure Sockets Layer (SSL). This protocol secures communication by using asymmetric key encryption.

When a client requests a web page's content, said web page sends its SSL certificate containing a public key that is required. Then both the server and the client goes through a process called SSL/TLS handshake which is a series of two-way communication to establish a secure conenction.

> **References:**
>
> - [HTTPS | Wikipedia](https://en.wikipedia.org/wiki/HTTPS)
> - [TLS Handshake | Wikipedia](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_handshake)

### **9. 6 What is Authentication and Authorization?**

**Authentication** is the process of verifying **WHO** a specific user **IS**
**Authorization** is the process of verifying **WHAT** a specific user **HAVE ACCESS TO**

> **References:**
>
> - [Authentication vs Authorization | auth0](https://auth0.com/docs/get-started/identity-fundamentals/authentication-and-authorization)

---

## **10. General Questions**

### **13. 1 Name the main advantages of Microservice architecture over Monolith**

- **Microservice** architecture is built by loosely coupled, independent, single purpose services. Therefore, they're easier to maintain and update when needed compared to Monolithic architecture.
  They have high scalability, more agile-friendly and makes it possible to implement CI/CD.
  > **References:**
  >
  > - [Microservices vs Monolith | Atlassian](https://www.atlassian.com/microservices/microservices-architecture/microservices-vs-monolith)

### **13. 2 How do you understand an event-driven architectures? What is a pub-sub pattern?**

**Event Driven Architecture** is a design pattern which is based on production and consumption of events where the event is transmitted between producers and consumers.
**Pub-Sub Pattern** is one of the patterns that event driven architecture can be based on. In pub-sub pattern, information about the event that occured is sent to the subs (subscribers) of this event from the publishers.

> **References:**
>
> - [What is Event Driven Architecture | RedHat](redhat.com/en/topics/integration/what-is-event-driven-architecture)

---

## **Week 3**

## **1. Node.js**

### **1. 4 What is the difference between dependencies and devDependencies in package.json?**

- `dependencies` are the modules that project requires to function effectively on production.
- `devDependencies` are the modules that is needed by the developer during developmente.

> **References:**
>
> - [dependencies, devDependencies and peerDependencies | GeeksForGeeks](https://www.geeksforgeeks.org/difference-between-dependencies-devdependencies-and-peerdependencies/)

### **1. 9 What is the Event Emitter class? How it is related to other classes?**

**Event Emitter** is a class inside the node's built-in `events` module that is responsible for handling events.

Event Emitter can listen for events triggered by other classes and perform operations when told to.

> **References:**
>
> - [Event Emitter | Nodejs](https://nodejs.org/docs/latest/api/events.html#class-eventemitter)

### **1. 12 What are the differences between worker thread and child_process?**

**Worker Thread** is a **single thread** that can complete a certain task, whereas a **child_process** is a process that can actually spawn new processes with their own memory.

> **References:**
>
> - [Single Thread, Child Process, Worker Threads and Cluster in Nodejs](https://alvinlal.netlify.app/blog/single-thread-vs-child-process-vs-worker-threads-vs-cluster-in-nodejs)

### **1. 13 What is the difference between commonJS and ES modules?**

**CommonJS** module system is the default module system within Nodejs. ES Modules were introducted as a new standard.

- CommonJS and ES Modules have different syntax and execution process for imports and exports.
  CommonJS imports are dynamically resolved at runtime, where ES Modules are executed at parse time.
- File Extensions are another difference between CommonJS and ES Modules
  Files with `.js` extension are treated as CommonJS Modules and files with `.mjs` extension are treated as ES Modules.

> **References:**
>
> - [CommonJS vs ES Modules](https://reflectoring.io/nodejs-modules-imports/)

### **1. 14 How to force node.js to treat your .js files as ES modules?**

We can use `.mjs` file extension and specify that we're using `type: module` in our `package.json` file while using ES6 import/export syntax for our modules

> **References:**
>
> - [CommonJS vs ES Modules](https://reflectoring.io/nodejs-modules-imports/)

## **2. Dealing With Async Code**

### **2. 5 What is Promisification and when it is used?**

**Promisification** is the conversion of a function that takes a callback into a function that returns a promise.

It's used for having cleaner and more maintainable code with a better error handling and prevent memory leaks caused by callback behaviour.

> **References:**
>
> - [Promisification | javascript.info](https://javascript.info/promisify)
> - [Write Your Own Promisification From Scrath | freeCodeCamp.org](https://www.freecodecamp.org/news/write-your-own-promisify-function-from-scratch/)

## **3. Express.js**

### **3. 5 How can you differ an error handling function from a request handler function?**

**Request Handler** functions can take `req`, `res`, and `next` parameters, whereas **error Handler** function additionally have `err` as a parameter

> **References:**
>
> - [Error Handling | Express](https://expressjs.com/en/guide/error-handling.html)

## **4. NestJS**

### **4. 1 What can be a Provider in NestJS?**

Providers are JavaScript classes in a module. Many of the basic NestJS classes can be treated as provider such as services, repositories, factories, helpers etc.

> **References:**
>
> - [Providers | NestJS Documentation](https://docs.nestjs.com/providers#providers)

### **4. 2 What are the use cases for Pipes in NestJS?**

**Pipe** is a class defined with a decorator which implements `PipeTransform` interface

Pipes can be used for:

- **transforming** the input data (ex. from string to number)
- **validation** of the input data

> **References:**
>
> - [Pipes | NestJS Documentation](https://docs.nestjs.com/pipes)

### **4. 3 Is there a possibility to bind extra logic before/after method execution in NestJS?**

**Interceptor** is a class defined with a decorator which implements `NestInterceptor` interface and they can be used to bind extra logic before or after method execution.

> **References:**
>
> - [Interceptors | NestJS](https://docs.nestjs.com/interceptors)

### **4. 4 How all unhandled exceptions are processed in NestJS?**

NestJS has a built-in exception layer which caughts unhandled layer and sends them to a global exception filter. We can also have full control over exception layer by creating custom **exception filters** to process unhandled exceptions.

> **References:**
>
> - [Exception Filters | NestJS](https://docs.nestjs.com/exception-filters)

## **5. Monitoring and Logging**

Low

### **5. 1 What is a Health check? Why do we need it?**

**Health Check** is a review of QA processes which involves a thorough investiagion of testing process, tools metrics and the team.

We use health check to identify the efficiency or the open to improvement parts of the system

> **References:**
>
> - [Health Check Testing](https://www.prolifics-testing.com/testing-services/consultancy/testing-health-check#:~:text=The%20Health%20Check%20is%20a,for%20large%20or%20complex%20projects.)

### **5. 2 What is a correlation ID? How it helps to debug your application?**

The **correlation identifier** is a unique id that is assigned to every transaction which allows to find the root cause in case of a failure by tracking a transaction with the given id

> **References:**
>
> - [Correlation Identifier | Medium](https://medium.com/@scokmen/debugging-microservices-part-ii-the-correlation-identifier-552f9016afcd)

## **6. Testing**

### **6. 4 What test runner libraries do you know?**

- **Jest**
- **Mocha**
- **Jasmine**

> **References:**
>
> - []()

## **7. Software Design**

### **7. 1. 1 REST API: What are the Levels of REST API?**

Levels of a REST API is defined by [**Richardson Maturity Model**](https://restfulapi.net/richardson-maturity-model/)

According to this model, there are four levels of maturity for a REST API:

- **Level 0** services have a single URI and uses a single HTTP Method
- **Level 1** services uses multiple URIs but single HTTP Method
- **Level 2** services uses multiple URIs and HTTP Methods but doesn't use HATEOAS
- **Level 3** services uses all three: Multiple URIs, HTTP Methods and HATEOAS

> **References:**
>
> - [Richardson Maturity Model | restfulapi.net](https://restfulapi.net/richardson-maturity-model/)

### **7. 3 What is GraphQL? What are its advantages over REST API?**

**GraphQL** is a server-side technology for executing queries on data using APIs, whereas REST is an architectural style to design APIs and consume endpoints.

- GraphQL can eliminate over-fetching or under-fetching.
- GraphQL provides better performance in terms of speed by fetching only the data with required fields.

> **References:**
>
> - [GraphQL Advantages & Disadvantages](https://www.javatpoint.com/graphql-advantages-and-disadvantages)

## **8. Databases**

## **8. 1 RDBMS (Postgres or MySQL)**

### **8. 1. 5 What data types are presented in PostgreSQL?**

- **Numeric Types** like `smallint`, `integer`, `bigint`, `decimal`
- **Monetary Types** that can store currency amount
- **Character Types** `character` with fixed length or `text` with unlimited length
- **Date/Time Types** for representing date/time.
- **Boolean Types** for representing boolean values.
  and more

> **References:**
>
> - [Data Types | PostgreSQL Documentation](https://www.postgresql.org/docs/current/datatype.html)

### **8. 1. 7 What is a sub query?**

**Subquery** is a nested query inside of another query or a subquery that returns a result to make use of.

> **References:**
>
> - [Subqueries](https://learn.microsoft.com/en-us/sql/relational-databases/performance/subqueries?view=sql-server-ver16)

### **8. 1. 9 What are Lock Levels in Postgres?**

Locks Levels are used to restrict access to a specific structure.

PostgreSQL provides five levels of locks:

- **Table-Level Locks**
- **Row-Level Locks**
- **Page-Level Locks**
- **Deadlocks**
- **Advisory Locks**

> **References:**
>
> - [Explicit Locking | PostgreSQL Documentation](https://www.postgresql.org/docs/current/explicit-locking.html)

### **8. 1. 11 What is ORM? What problems does it solve?**

**ORM (Object Relational Mapping)** tools allow us to execute queries in anobject-oriented way which allows us to write more readable and maintainable code.

> **References:**
>
> - [What is an ORM | freeCodeCamp.org](https://www.freecodecamp.org/news/what-is-an-orm-the-meaning-of-object-relational-mapping-database-tools/)

## **8. 1. 12 TypeORM**

### **8. 1. 12. 1 What is the Query Builder?**

**Query Builder** makes it possible to write complex queries in a simpler way by constructing a query with the given properties.

> **References:**
>
> - [TypeORM Query Builder](https://www.tutorialspoint.com/typeorm/typeorm_query_builder.htm)

### **8. 1. 12. 2 What are Active Record and Data Mapper patterns?**

- **Active Record** pattern is a way to access data in a relational database. Table is wrapped in a class. Therefore, a single row can be accessed with an obect instance

- **Data Mapper** is a Data Access Layer that performs two-way transfer of data between database and in memory data representation in order to keep them independant of each other.

> **References:**
>
> - [Active Record and Data Mappers of ORM | Medium](https://medium.com/oceanize-geeks/the-active-record-and-data-mappers-of-orm-pattern-eefb8262b7bb)

### **8. 1. 12. 3 What is the difference between Raw Entities and Entities?**

**Entity** is a class that represents a database table in relational databases, whereas **raw entities** represents a collection of specific fields of an entity.

> **References:**
>
> - [Entity | TypeORM Documentation](https://typeorm.io/entities#entities)

### **8. 1. 12. 4 How to process tables with a lot of data inside with typeorm?**

- Streams can be used to slice the data on smaller pieces.
- Define relation tables just to fetch the necessary data.

> **References:**
>
> - []()

## **9. Security**

### **9. 3 How do you understand symmetric and asymmetric encryption?**

- **Symmetric Encryption** uses only one key to both encrypt and decrypt data which is less secure compared to asymmetric encryption. Therefore data needs to be transfered in a secure way.
  **Asymmetric Encryiption** uses one public and one private key which makes the whole encryption and decryption slower but safer.

> **References:**
>
> - [Symmetric and Asymmetric Encryption | GeeksForGeeks](https://www.geeksforgeeks.org/difference-between-symmetric-and-asymmetric-key-encryption/)

### **9. 4 What is the difference between private and public key?**

**Public key** that is provided by the recipent can be used to encrypt data and **private key** is only known by the recipent to decrypt the data.

> **References:**
>
> - [Public vs Private Key](https://www.preveil.com/blog/public-and-private-key/)

### **9. 8 What types of Authentication do you know? When to use them?**

- **Password-Based Authentication** can be used for basic authentication purposes.
- **Multi-Factor Authentication** provides extra layer of security after a basic authentication process is complete.
- **Certificate-Based Authentication** is used to identify both users and devices by validating digital certificates. This method can be used to secure the access to an endpoint from various clients or devices.
- **Biometric Authentication** can be used for securing access to a personal device or a system using biological characteristics.
- **Token-Based Authentication** is used to store credentials of the users and provide certain permissions to access protected content.

> **References:**
>
> - [Authentication Methods](https://www.idrnd.ai/5-authentication-methods-that-can-prevent-the-next-breach/)

## **10 General questions**

### **13. 3 What is a 3-tier WEB Application? Are the tiers logical or physical?**

**Three-tier Web Application** is an application where the application is divided into three main layers.

- **Presentation Tier (Physical)** where the user interface live and interaction with the user happens.
- **Application Tier (Logical)** where the data is processed and business logic executes
- **Data Tier (Phyiscal)** where the data is stored and managed.

> **References:**
>
> - [Thee-Tier Architecture | IBM](https://www.ibm.com/cloud/learn/three-tier-architecture)
