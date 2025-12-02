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

In JavaScript, working with text is an essential part of coding, and often, you'll need to combine or join pieces of text together. This process is called string concatenation.

In this lesson, we'll focus on how string concatenation works, specifically using the `+` operator, the `+=` operator, and the `concat()` method.

The `+` operator is one of the simplest and most frequently used methods to concatenate strings. It allows you to join multiple strings or combine strings with variables that hold text.

Here's an example:

```
let firstName = "John";
let lastName = "Doe";

let fullName = firstName + " " + lastName; 
console.log(fullName); // John Doe
```

In this example, we used the `+` operator to concatenate the `firstName` and `lastName` variables along with a space (`" "`) to create the full name.

One disadvantage of using the `+` operator for string concatenation is that it can lead to spacing issues if you don't carefully manage the spacing between the concatenated strings.

Here is an example where a space is missing:

```
let firstName = "John";
let lastName = "Doe";

let fullName = firstName + lastName; 
console.log(fullName); // "JohnDoe"
```

Whenever you use the `+` operator to concatenate strings, it is important to double check for any potential spacing issues.

If you need to add or append to an existing string, then you can use the `+=` operator. This is helpful when you want to build upon a string by adding more text to it over time.

Here's an example of appending one string to another using the `+=` operator:

```
let greeting = 'Hello';
greeting += ', John!';

console.log(greeting); // "Hello, John!"
```

It is important to remember that strings are immutable which means once a string is created you can not alter it.

In this case, the original string of `Hello` is not modified. Instead, greeting now references the new string of `Hello, John!`

Another way you can concatenate strings is to use the `concat()` method.

Before we begin learning about the `concat()` method, it is important to first understand what a method and a function are at a higher level.

In programming, a function is a reusable block of code that performs a specific task and can be called with various inputs. A method, on the other hand, is a type of function that is associated with an object, meaning it operates on the data contained within that object.

In future lessons, we will dive much deeper into how functions, objects, and methods work in JavaScript. But for now, it is important to understand that JavaScript has dozens of methods you can use, like the `concat()` method.

Here's an example of using the `concat()` method to join two strings together:

```
let str1 = 'Hello';
let str2 = 'World';

let result = str1.concat(' ', str2); 
console.log(result); // Hello World
```

In this example, we use the `concat()` method to join `str1`, a space (`' '`), and `str2` into a single string.

To conclude, `+` operator is best for simple concatenation, especially when you need to combine a few strings or variables.

The `+=` operator is useful when building up a string step by step or appending new content to an existing string variable.

Finally, the `concat()` method is beneficial when you need to concatenate multiple strings together.

## What Is console.log Used For, and How Does It Work?

The prior lessons introduced you to `console.log()` but this lesson will dive deeper into its purpose and usage.

In JavaScript, `console.log()` is a simple yet powerful tool used to display messages or output information to the browser's console. It's mostly used by developers to debug and inspect code while working on their programs.

You can use `console.log()` to log text or variables to the console and ensure your code is running correctly.

To use `console.log()`, you call the method with the value or message you want to output inside the parentheses. Here are some examples:

```
console.log("Hello, world!");

let num = 5;
console.log(num); // 5
```

The first example prints `Hello, world!` in the browser's console, while the second example prints the value `5`.

Here is another example of working with `console.log()`:

```
let name = "Alice";
console.log("Hello, " + name + "!"); // Hello, Alice!
```

You can also pass in multiple values to `console.log()` separated by commas. For example:

```
let name = "Alice";
let age = 25;
console.log("Name:", name, "Age:", age); // Name: Alice Age: 25
```

This is helpful for logging multiple pieces of information at once.

The `console.log()` method helps you monitor your code as it runs, making it easier to spot mistakes and understand how your program behaves.