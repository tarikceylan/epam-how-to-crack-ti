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

**- Unit Tests** should be performed on smallest, testable piece of code.
**- Integration Tests** should cover any API integration with 3rd pary services.
**- End-To-End Tests** should cover all actions that an end-user could take using our API.

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
