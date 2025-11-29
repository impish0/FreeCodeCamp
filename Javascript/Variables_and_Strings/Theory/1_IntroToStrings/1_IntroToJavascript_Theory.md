In JavaScript, a data type refers to the kind of value a variable holds.

A variable is a named container that stores a value of a specific data type, allowing you to reference and manipulate it throughout your code. Data types help the program understand the kind of data it's working with, whether it's a number, text, or something else.

JavaScript has several basic data types that you'll use in your programs. We'll explore each data type in greater detail in future lessons. For now, here is a brief introduction of the different data types in JavaScript.

The first data type we will look at is the `Number` type.

A `Number` represents both integers and floating-point values. Examples of integers include `7`, `19`, and `90`. Examples of floating point numbers include `3.14` and `5.2`. A floating point number is a number with a decimal point.

The next data type is a `String`.

A `String` is a sequence of characters, or text, enclosed in quotes. Here are two examples:

```
"Hello, world"
```
```
'JavaScript'
```

Another data type used in JavaScript is the `Boolean` type.

A `Boolean` represents one of two possible values: `true` or `false`. You can use a boolean to check if a page is loading, or if a user is logged in or not.

The next two data types used in JavaScript are `undefined` and `null`.

`undefined` means a variable has been declared but hasn't been given a value yet. `null` means the variable has been intentionally set to "nothing" and does not hold any value. We will explore more on how this works in future lessons.

The next data type we will look at is the `Object` type.

An `Object` is a more complex data type that can hold collections of key-value pairs. Let's break this down. The key (also called a property name), is like a label for the data, whereas the value, is the actual data you want to store. Here is an example:

```
let book = {
  title: "The Great Gatsby",
  author: "F. Scott Fitzgerald",
  year: 1925
};
```

In this object, `title`, `author`, and `year` are the keys (or property names). `The Great Gatsby`, `F. Scott Fitzgerald`, and `1925` are the corresponding values.

Each key-value pair in an object is called a property. So we can say that this book object has three properties. This is just a basic introduction to objects and their properties. In future lessons, we'll go deeper into more advanced concepts.

The last two data types are the `Symbol` and `BigInt` data types.

A `Symbol` is a special type of value in JavaScript that is always unique and cannot be changed. It's often used to create unique labels or identifiers for properties:

```
Symbol('mySymbol');
```

`BigInt` is used for very large numbers that exceed the limit of the `Number` type:

```
1234567890123456789012345678901234567890n;
```

In this example, we create a `BigInt` by adding `n` at the end of a very large number.

`Symbol` and `BigInt` are two types that are less commonly used, but they are still important to know about.

Understanding these data types helps you handle and work with various kinds of data in your programs, as each type has its own characteristics and behaviors.

In JavaScript, variables act as containers for storing data that you can access and modify throughout your program.

You can think of variables as boxes that hold values. With variables, you can keep track of things like numbers or text and refer to these values whenever you need them in your program.

One way to declare a variable in JavaScript is to use the `let` keyword. You will learn more about the `let` keyword as well as other ways to declare variables in future lessons.

Here's an example of using `let` to declare a variable called `age`:

```
let age;
```

Right now, the `age` variable does not have a value assigned to it. If you try to use it, it will return `undefined`, which means it has no value.

Here is an example.

**NOTE**: `console.log()` is a function that outputs information to the console, which is a part of your web browser used for debugging code. You will learn more about `console.log()` in future lessons. Also, the `//` symbols are used to add comments in your code. Comments are notes for yourself or other programmers that are ignored when the code runs.

9

1

2

let age;

console.log(age); // undefined

undefined

---

When working with JavaScript, you'll often declare variables to store data that you plan to use throughout your program.

In modern JavaScript, `let` and `const` are the preferred ways to declare variables, but they differ in how they handle value assignment and reassignment.

In this lesson, we'll explore how `let` and `const` differ in variable declaration, assignment, and reassignment.

The `let` keyword allows you to declare variables that can be updated or reassigned later. You can think of `let` as a flexible container – once you've stored a value in it, you can change that value as needed throughout your program.

Here's an example of declaring and assigning a variable with `let`:

```
let score = 10;
```

In this case, the variable `score` is declared and assigned the value `10`. If you want to update the value later, you can easily do that:

9

1

2

3

4

let score = 10;

console.log(score); // 10

score = 20;

console.log(score); // 20

10

20

10

20