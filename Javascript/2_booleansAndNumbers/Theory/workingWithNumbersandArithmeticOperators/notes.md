## What Is the Number Type in JavaScript, and What Are the Different Types of Numbers Available?

The `Number` type is one of the most used data types in JavaScript and other programming languages. Numbers might seem simple, but there's a lot to explore when it comes to numbers in JavaScript. So, let's take a deeper look. In JavaScript, the `Number` data type represents a numeric value.

Unlike many other programming languages that separate integers and floating-point numbers into different types, JavaScript uses one unified `Number` type to account for numbers. This means you can work with whole numbers, decimals, and even special numeric values all under the same `Number` data type umbrella.

Here's a basic example showing you integers, floating point numbers, and negative numbers are all of type number:

```
const wholeNumber = 50;
const decimalNumber = 4.5;
const negativeNumber = -7;

console.log(typeof wholeNumber); // number
console.log(typeof decimalNumber); // number
console.log(typeof negativeNumber); // number
```

JavaScript's `Number` type includes various kinds of numeric values, ranging from simple integers and floating-point numbers to special cases like `Infinity` and `NaN`, or "Not a Number". Let's break down the main types you'll encounter. Integers are whole numbers without any fractional or decimal part. They can be positive, negative, or zero. Here are some examples:

```
const positiveInteger = 100;
const negativeInteger = -25;
const zero = 0;

console.log(typeof positiveInteger); // number
console.log(typeof negativeInteger); // number
console.log(typeof zero); // number
```

Floating point numbers are numbers with decimal points. They're often referred to as just "floats" by JavaScript developers. Floats are useful when you need more precision, such as when you're dealing with measurements or currencies. Here are some examples:

```
const floatingPointNumber = 4.5;
const anotherFloat = 89.56;
const oneMoreFloat = 16.462;

console.log(typeof floatingPointNumber); // number
console.log(typeof anotherFloat); // number
console.log(typeof oneMoreFloat); // number
```

JavaScript can represent numbers that are beyond the maximum limit with `Infinity`. You'll encounter this when you try to divide a number by zero or on rare occasions, exceed the upper boundary of the `Number` type. Here's an example:

```
const infiniteNumber = 1 / 0;
console.log(infiniteNumber); // Infinity
console.log(typeof infiniteNumber); // number
```

Sometimes in JavaScript, some mathematical operations don't result in a valid number. For instance, if you try to perform a mathematical operation on something that isn't a number, you'll get `NaN`, which stands for "Not a Number":

```
const notANumber = 'hello world' / 2;
console.log(notANumber); // NaN
```

Surprisingly, the type of `NaN` is also `Number`:

```
const notANumber = 'hello world' / 2;
console.log(typeof notANumber); // number
```

Apart from the standard decimal system (base 10), JavaScript also supports numbers in different bases such as binary, octal, and hexadecimal. Binary is a base-2 system that uses only digits 1 and 0. Octal is a base-8 system that uses only digits 0 to 7. Hexadecimal is a base-16 system that uses digits 0 to 9 and letters a to f, like you see in CSS hex colors.

## What Are the Different Arithmetic Operators in JavaScript?

JavaScript provides tools to perform basic arithmetic operations on numbers, such as addition, subtraction, multiplication, and division. JavaScript also includes operators for more complex arithmetic operations, such as remainder and exponentiation.

All these tools are called arithmetic operators. Let's look at these operators in detail, how to use them and how to combine them.

The addition operator is a plus sign (`+`). The addition operator allows you to find the total of two or more numbers. In addition operations, the order of the numbers doesn't matter:

```
const num1 = 10;
const num2 = 5;
const num3 = 15;

const result1 = num1 + num2;
const result2 = num2 + num1;
const result3 = num2 + num1 + num3;

console.log(result1); // 15
console.log(result2); // 15
console.log(result3); // 30
```

The subtraction operator is a minus sign (`-`). It allows you to find the difference between two numbers. Use the minus sign when you want to subtract a number from another number, usually a smaller one from a bigger one:

```
const difference = 10 - 5;
console.log(difference); // 5
```

If a smaller number comes first, you'll get a negative result:

```
const difference = 5 - 10;
console.log(difference); // -5
```

You can also assign the numbers to variables and do the subtraction with the variable names:

```
const num1 = 10;
const num2 = 5;
const result = num1 - num2;

console.log(result); // 5
```

In JavaScript, the multiplication operator is represented by an asterisk (`*`) and is used to find the product of two or more numbers. The order of the numbers you're multiplying does not matter:

```
const num1 = 10;
const num2 = 5;
const num3 = 15;

const result1 = num1 * num2;
const result2 = num2 * num1;
const result3 = num2 * num1 * num3;

console.log(result1); // 50
console.log(result2); // 50
console.log(result3); // 750
```

In JavaScript, the division operator is a slash (`/`), which differs from the division symbol used in traditional math (`÷`). You perform division operations with the division operator. The order of the numbers you're dividing matters in this case:

```
const num1 = 10;
const num2 = 5;
const num3 = 15;

const result1 = num1 / num2;
const result2 = num2 / num1;
const result3 = num2 / num1 / num3;

console.log(result1); // 2
console.log(result2); // 0.5
console.log(result3); // 0.03333333333333333
```

It's important to note that if you try to divide by zero, JavaScript will return `Infinity`:

```
const result = 10 / 0; 

console.log(result); // Infinity
```

Make sure to avoid those types of calculations so you don't end up with unexpected results in your code.

The remainder operator, represented by a percentage sign (`%`), returns the remainder of a division. The remainder in math is the leftover value after performing division:

```
const num1 = 10;
const num2 = 3;
const remainder = num1 % num2;

console.log(remainder); // 1
```

The exponentiation operator, represented by a double asterisk (`**`), raises one number to the power of another:

```
const num1 = 2;
const num2 = 3;

const exponent = num1 ** num2;
console.log(exponent); // 8
```

It's possible to mix operators in a single operation or expression:

```
const result = 10 + 5 * 2 - 8 / 4;
console.log(result); // 18
```

When you mix different operators in a single expression, the JavaScript engine follows a system called operator precedence to determine the order of operations. Operator precedence determines the order in which operations are executed in expressions. You will learn more about operator precedence in future lessons.

## What Happens When You Try to Do Calculations with Numbers and Strings?

JavaScript is a language where things sometimes work in surprising, or even weird, ways. One such surprise occurs when you mix numbers and strings in calculations. The first thing you'll probably try is to add a number and a string. In JavaScript, the `+` operator does double duty. It handles both addition and string concatenation, which is a way to join two strings together.

When you use `+` with a number and a string, JavaScript decides to treat them both as strings and joins them together. If you check the type of the result with the `typeof` operator, you'd see it's indeed a string:

```
const result = 5 + '10';

console.log(result); // 510
console.log(typeof result); // string
```

What do you think will happen if you switch the order of `5` and `'10'`?

```
const result = '10' + 5;

console.log(result); // 105
console.log(typeof result); // string
```

You can see the same thing happened. JavaScript sees a string in `'10'` and a number in `5`, so it converts the number to a string and concatenates them. This is known as type coercion. Type coercion is when a value from one data type is converted into another.

Things get more interesting when you try to perform other arithmetic operations like subtraction, multiplication, or division with a string and number. In these cases, JavaScript tries to convert the string into a number before doing the math – another type coercion! Here's what happens:

```
const subtractionResult = '10' - 5;
console.log(subtractionResult); // 5
console.log(typeof subtractionResult); // number

const multiplicationResult = '10' * 2;
console.log(multiplicationResult); // 20
console.log(typeof multiplicationResult); // number

const divisionResult = '20' / 2;
console.log(divisionResult); // 10
console.log(typeof divisionResult); // number
```

In the examples above, JavaScript successfully converts the string `'10'` or `'20'` to a number and then performs the calculation. As a result, `'10' - 5` yields `5`, `'10' * 2` gives `20`, and `'20' / 2` results in `10`.

But what if the string doesn't look like a number? Let's see what happens in that case:

```
const subtractionResult = 'abc' - 5;
console.log(subtractionResult); // NaN
console.log(typeof subtractionResult); // number

const multiplicationResult = 'abc' * 2;
console.log(multiplicationResult); // NaN
console.log(typeof multiplicationResult); // number

const divisionResult = 'abc' / 2;
console.log(divisionResult); // NaN
console.log(typeof divisionResult); // number
```

In the examples above, the string `'abc'` does not represent a valid numeric value, so JavaScript cannot convert it into a meaningful number. When such conversion fails, JavaScript returns `NaN`, which stands for "Not a Number". `NaN` is a special value of the `Number` type that represents an invalid or unrepresentable number.

What if you perform arithmetic operations with a boolean (`true` or `false`)? Let's see what happens. JavaScript treats booleans as numbers in mathematical operations: `true` becomes `1`, and `false` becomes `0`.

```
const result1 = true + 1;
console.log(result1); // 2
console.log(typeof result1); // number

const result2 = false + 1;
console.log(result2); // 1
console.log(typeof result2); // number

const result3 = 'Hello' + true;
console.log(result3); // "Hellotrue"
console.log(typeof result3); // string
```

In the first two examples, `true + 1` resulted in `2`, and `false + 1` resulted in `1`. In the third example, `'Hello' + true`, JavaScript converted `true` to a string and concatenates it with `'Hello'`, resulting in `'Hellotrue'`, which is a string.

For `null` and `undefined`, JavaScript treats `null` as `0` and `undefined` as `NaN` in mathematical operations:

```
const result1 = null + 5;
console.log(result1); // 5
console.log(typeof result1); // number

const result2 = undefined + 5;
console.log(result2); // NaN
console.log(typeof result2); // number
```

JavaScript often performs type coercion, automatically converting data types such as numbers, strings, and booleans in sometimes unexpected ways. Understanding these conversions is crucial for avoiding bugs and writing robust code in your projects.