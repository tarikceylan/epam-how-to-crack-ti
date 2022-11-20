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
