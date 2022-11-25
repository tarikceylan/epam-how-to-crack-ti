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

- **'given'** represents the a certain behaviour.
- **'when'** represents the sepcified behaviour.
- **'then'** represents the specified behaviour.

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
