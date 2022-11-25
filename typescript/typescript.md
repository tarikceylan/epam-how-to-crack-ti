# **TypeScript Interview Questions**

## **Week 1**

---

## **1. General Questions**

### **1. 1 What is TypeScript?**

**TypeScript** is a superset of JavaScript which means TypeScript contains all JavaScript features but adds more. **TypeScript** is a static type checker that allows us to add `types` to JavaScript code.

> **References:**
>
> - [TypeScript Official Documentation](https://www.typescriptlang.org/)

### **1. 2 Why do we need TypeScript? What are the differences between TypeScript and JavaScript?**

**TypeScript** allow to add type safety to written code, which means a variable's type is locked in the scope. Type safety can be critical, especially in large team projects. TypeScript also adds various features like interfaces to JavaScript.

Differences between TypeScript and JavaScript

- TypeScript supports both static and dynamic typing, whereas JavaScript is dynamically typed.
- TypeScript is compiled before run. It doesn't allow type erros occur in the runtime where JavaScript just executes them.
- TypeScript has additional features (generics, interfaces etc.) that benefits OOP compared to JavaScript

> **References:**
>
> - [TypeScript Official Documentation](https://www.typescriptlang.org/)
> - [TypeScript vs JavaScript](https://www.interviewbit.com/blog/typescript-vs-javascript/)

### **1. 3 Pros and cons of using TypeScript**

**TypeScript Pros:**

- Typos and errors caught in compilation time
- Module Support
- Compiles down to JavaScript
- OOP features

**TypeScript Cons:**

- Not as flexible as JavaScript
- In order to run the application, compile step is required.
- Can not fix all of the fundamental JavaScript errors and might create an illusion like it does.

> **References:**
>
> - [TypeScript Pros & Cons](https://medium.com/@BuildMySite1/what-is-typescript-pros-and-cons-8dc5cdc3e78d)

### **1. 4 How to transform TS code into JS?**

When TypeScript code gets compiled by `tsc` using its built-in compiler, it converts into vanilla JavaScript code.

> **References:**
>
> -[tsc - TypeScript Compiler | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/basic-types.html#tsc-the-typescript-compiler)

---

## **2. Basics**

### **2. 1 What is void, and when to use void type?**

`void` implies that there is no type to be assigned. `void` is mostly used for a function's return type. Assigning void to varaibles is not useful since they can only have `null` or `undefined`.

> **References:**
>
> - [Void | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/basic-types.html#void)

### **2. 2 Explain how enums work in TypeScript?**

`enums` provide a way to define set of named constants and associates them with a numeric value.

> **References:**
>
> - [Enums | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/enums.html)

### **2. 3 What is an interface?**

`ìnterface` in TypeScript allows us to define an object type structure that we can pass around and use for type checking.

> **References:**
>
> - [Object Types | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/objects.html)

### **2. 4 Explain the various ways to control member visibility in TypeScript.**

We can use access modifiers like `public`, `protected`, and `private`.

- `public` is the default visibility level for members which means they can be accessed from anywhere in the system.
- `protected` members are only visible to subclasses of the class they're declared in.
- `private` is a more restrictive version of `protected` which doesn't allow access from subclasses

> **References:**
>
> - [Member Visibility | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/classes.html#member-visibility)

### **2. 5 What are Generics in TypeScript?**

**Generics** allow us to track the type of arguments passed into functions and preserve the type to be used as return type of that function as well. Basically, we can set generics to specify whenever we don't want to force upon a certain type and not want to use `any` to be able to perform type checks.

> **References:**
>
> - [Generics | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/generics.html)

### **2. 6 What is the difference between extends and implements in TypeScript?**

- A new class that is created using `extends` becomes the child of the base class and new class will get all properties and methods of the parent.
- With `implements`, new class can be treated as the same but it's not a child.

> **References:**
>
> - [Difference Between extends and implements in TypeScript | StackOverflow](https://stackoverflow.com/questions/38834625/whats-the-difference-between-extends-and-implements-in-typescript)

### **2. 7 List some of the utility types provided by TypeScript and explain their usage**

- `Awaited` is used for handling async operations like `async` and `await`, or `.then()` method on `Promise`s.
- `Partial` is used for constructing types where all properties of the type is set to optional.
- `Required` is used for constructing types where all properties of the type is set to required (the opposite of `Partial`)
- `Readonly` is used for constructing types where all properties are `readonly` which means they can't be re-assigned

> **References:**
>
> - [Utility Types | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/utility-types.html)

### **2. 8 What are type assertions in TypeScript?**

**Type Assertions** can be used whenever the type of a returned value is can not be known by TypeScript. When that happens, we can specify the type for the returned value with `as` keyword.

> **References:**
>
> - [Type Assertions | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#type-assertions)

### **2. 9 When should you use the unknown type?**

`unknown` is similar to `any` but unlike `any`, `unkown` provides type safety. Any type of value can be assigned to a variable when used `any` but `unknown` can only be assigned to `unknown` or `any` typed varaibles without [type assertion](#2-8-what-are-type-assertions-in-typescript).

> **References:**
>
> - [What is `unknown` type and When to use it in TypeScript](https://www.geeksforgeeks.org/what-is-an-unknown-type-and-when-to-use-it-in-typescript/)

### **2. 10 What is the difference between types String and string in TypeScript?**

- `String` is the "JavaScript object" type which we could use to create new strings, using the `new` keyword.

- `string` is the TypeScript string type which we can set as a type for variables, functions, return types and so on.

> **References:**
>
> - [Difference between String and string in TypeScript](https://stackoverflow.com/questions/14727044/what-is-the-difference-between-types-string-and-string)

---

## **3. Advanced**

### **3. 1 What are string literal types?**

**String literal types** allow us to restrict possible string values that a variable can take. This is useful when combined with `unions`. For example; we could create functions that only accept certain set of known values.

> **References**
>
> - [Literal Types | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#literal-types)

### **3. 2 What are abstract classes? When should you use one?**

**Abstract classes** are base classes that hasn't had an implementation provided. They should be used when a common behavior needs to be shared with related subclasses.

> **References:**
>
> - [Abstract Classes and Members | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/classes.html#abstract-classes-and-members)
> - [When To Use Abstract Classes in TypeScript](https://khalilstemmler.com/blogs/typescript/abstract-class/#:~:text=The%20most%20common%20use%20of,abstract%20class%20with%20a%20subclass.)

### **3. 3 Explain the tuple types in TypeScript.**

`tuple` types are `Array`-like types that knows the exact type of each element it contains as well as their positions.

> **References:**
>
> - [Tuple Types | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/objects.html#tuple-types)

### **3. 4 Explain how tuple destructuring works in TypeScript.**

Tuples can be desctructured like `array`s. The destructuring variable matches with the type of corresponding tuple elements.

```typescript
let tuple: [number, string, boolean] = [7, 'hello', true];
let [a, b, c] = tuple; // a: number, b: string, c: boolean
```

> **References:**
>
> - [Tuple Destructuring | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/variable-declarations.html#tuple-destructuring)

---

## **Week 2**

## **1. General Questions**

### **1. 5 Mention some of the features of TypeScript?**

- Provides a complete OOP experience with classes, interfaces, inheritance and so on.
- Performs static-type checking on compile time which minimizes type-related errors/bugs before execution.
- Fully compatible with JavaScript libraries.
- Basically TypeScript is JavaScript with extra compilation step

> **References:**
>
> - [Introduction | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/intro.html)
> - [Features Of TypeScript](https://www.javatpoint.com/typescript-features)

### **1. 6 Explain the Components of Typescript**

TypeScript is iternally divided into three main layers:

- **Language** is where language specific syntax and keywords are defined.
- **TypeScript Compiler** is a configurable, internal compiler of TypeScript which converts TypeScript code into JavaScript code. During the conversion it also performs operations like type checking and parsing.
- **TypeScript Language Services** provides information to help editors and other tools about the structure of language.

> **References:**
>
> - [TypeScript Components](https://www.javatpoint.com/typescript-components)

## **Basics**

### **2. 11 Explain the purpose of the never type in TypeScript.**

`never` type represents **values which are never observed**. For example; if a function doesn't return anything or throws an error, it's type can be set to `never`.

`never` type also is assigned to the variables if no other option is possible in a union

> **References:**
>
> - [`never` | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/functions.html#never)

### **2. 12 What are union types in TypeScript?**

`union` type that is formed from two or more types. It's basically a type created by combining multiple types which indicates that type can be one of the given types.

> **References:**
>
> - [Union Types | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#union-types)

### **2. 13 How to make object properties immutable in TypeScript?**

We can create immutable object properties by using `readonly` keyword in TypeScript.

> **References:**
>
> - [`readonly` | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes-func.html#readonly-and-const)

### **2. 14 How to easily make all properties of an interface optional?**

`Partial<Type>` utility type can be used to make all properties of an interface optional

> **References:**
>
> - [`Partial<Type> | TypeScript Official Documentation`](https://www.typescriptlang.org/docs/handbook/utility-types.html#partialtype)

### **2. 15 What is the differance between keyof and typeof operators? Explain each of them**

- `keyof` type operator takes an object type and produces a string or numeric literal union from its keys.
- `typeof` type operator takes an expression's type and uses it as a type declaration.
  > **References:**
  >
  > - [`keyof` Type Operator | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/keyof-types.html)
  > - [`typeof` Type Operator | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/keyof-types.html)

### **2. 16 What is the difference between type and interface in TypeScript?**

`interface` can be extended by declaring it a second time, whereas `type` can not. `type` can not be changed outside of its declaration

> **References:**
>
> - [types vs Interfaces | TypeScript Playground](https://www.typescriptlang.org/play#example/types-vs-interfaces)

### **2. 17 What is tsconfig.json file?**

`tsconfig.json` file specifies the root files and the compiler options required to compile TypeScript project

> **References:**
>
> - [What is tsconfig.json | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html)

### **2. 18 What is the fundamental difference between Optional Chaining (?.) and Non-null assertion operator (!) in TypeScript?**

- **Non-Null Assertion Operator** states that the value will never be `null` and if it is `null`, it causes a crash.
- **Optional Chaining** checks against a value for being `null` or `undefined`. If it is, it just stops the execution of properety chain and moves on with the rest of the code.

> **References:**
>
> - [Optional Chaining vs Assertion Operator in TypeScript](https://codeburst.io/optional-chaining-vs-assertion-operator-in-typescript-522947c927a5)

## **Advanced**

### **3. 5 What is the difference between void and never types?**

`void` type represents the non-existance of a type for a returned value, whereas `never` represents the values that never occur such as a function that always throw an excepetion.

> **References:**
>
> - [Difference between `void` and `never`](https://medium.com/swlh/whats-the-difference-between-never-and-void-in-typescript-16f6629bfcdc)

### **3. 6 What are conditional types? How do you create them?**

**Conditional types** can be used to describe relation between types of inputs and outputs.

We can create conditional types like a conditional expression we use in JavaScript.
`condition ? trueExpression : falseExpression`

> **References:**
>
> - [Conditional Types | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)

### **3. 7 Does TypeScript support function overloading?**

**Yes**. TypeScript support function overloading. We can have multiple functions with the same names, but different argument types as long as number of parameters are the same.

> **References:**
>
> - [Function Overloading in TypeScript](https://www.tutorialsteacher.com/typescript/function-overloading)

### **3. 8 Explain Decorators in TypeScript.**

**Decorators** are special declarations that can be attached to a class declaration, method, accessor, property or parameters.

> **References:**
>
> - [Decorators | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/decorators.html)

### **3. 9 How to use Indexed Access Types**

**Indexed Access Types** can be used to lookup a specific property of another type. Their usage is like follows:

```typescript
type Person = { age: number; name: string; alive: boolean };
type Age = Person['age'];
```

Above example will set `Age` type's type to number.

> **References:**
>
> - [Indexed Access Types | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/2/indexed-access-types.html)

### **3. 10 Can Type aliases be recursive?**

As of TypeScript version 3.7, type aliases can be recursive which means a type alias can refer to itself within.

> **References:**
>
> - [Recursive Type References | TypeScript Playground](https://www.typescriptlang.org/play#example/recursive-type-references)

### **3. 11 What is Namespace and how to declare it?**

`namespace` refers to previous `internal modules` in TypeScript which helps us organize the code and split it into smaller pieces which can be included anywhere in the system.
They can be declaerd with the `namespace` keyword.

> **References:**
>
> - [Namespaces | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/namespaces.html)

### **3. 12 What is TypeScript Declare Keyword?**

`declare` keyword is much like the `import` keyword in JavaScript which allow us to bring in variables, functions or a whole service within the system to our existing file.

> **References:**
>
> - [Declaration Reference | TypeScript Official Documentation](https://www.typescriptlang.org/docs/handbook/declaration-files/by-example.html)
