## How Does Operator Precedence Work?
If you write an expression with several operators in JavaScript, how does JavaScript decide which one to evaluate first? This is where operator precedence comes in. Let's explore operator precedence in detail with code examples, and also what happens when operators have the same precedence.

Operator precedence determines the order in which operations are evaluated in an expression. Operators with higher precedence are evaluated before those with lower precedence. Think of operator precedence like in math, where division and multiplication happen before addition and subtraction.

Without following this rule, basic equations would give you the wrong answer. JavaScript works the same way. It has its own rules for which operators come first, second, and so on. For example, take a look at the expression below:

```
const result = 2 + 3 * 4;

console.log(result); // 14
```

If JavaScript evaluated this expression from left to right, you'd expect `2 + 3 = 5`, then `5 * 4 = 20`. But because multiplication has a higher precedence than addition, JavaScript evaluates the `3 * 4` part first, resulting in `2 + 12 = 14`.

Sometimes, you may want certain parts of your expression to run first, regardless of precedence rules. You can use parentheses, `()`, to do this. Anything inside parentheses is evaluated first, no matter what. Let's make the `2 + 3` part of the previous example evaluate first:

```
const result = (2 + 3) * 4;

console.log(result); // 20
```

In the example above, the parentheses force JavaScript to evaluate `2 + 3` first, and then multiply the result by `4`. This gives you `20` instead of `14`.

The division operator has more precedence than addition or subtraction too:

```
const result = 2 + 6 / 3;

console.log(result); // 4
```

If JavaScript evaluated this expression from left to right, you might expect `2 + 6 = 8`, then `8 / 3 = 2.67`. But since division has a higher precedence than addition, JavaScript evaluates the division first: `6 / 3 = 2`, and then adds `2 + 2`, giving the result `4`.

So, in both multiplication and division, those operations will always take place before addition and subtraction unless you use parentheses to change the order. So what happens if the operators have the same precedence? JavaScript uses associativity to figure out the order to evaluate them.

Associativity is what tells JavaScript whether to evaluate operators from left to right or right to left. For most operators like addition and multiplication, associativity is left to right. So, JavaScript processes these from the leftmost side of the expression to the right:

```
const result = 10 - 2 + 3;

console.log(result); // 11
```

First, `10 - 2 = 8`, then `8 + 3 = 11`. JavaScript moves left to right in this case. Some operators, like assignment (`=`), are right-to-left associative. This means the right side of the expression gets evaluated first:

```
let a, b;
a = b = 5;

console.log(a); // 5
console.log(b); // 5
console.log(a + b); // 10
```

In the example above, JavaScript assigns `5` to `b` first, then assigns `b` (which is now `5`) to `a`.

The exponent operator is also right-to-left associative:

```
const result = 2 ** 3 ** 2;

console.log(result); // 512
```

First, JavaScript evaluates `3 ** 2`, which equals `9`, then, it evaluates `2 ** 9`, which equals `512`. If the exponent operator had left-to-right associativity, JavaScript would have calculated `2 ** 3` first to get `8`, then `8 ** 2` to get `64`.

## How Do the Increment and Decrement Operators Work?

If you're working with numbers and need to increase or decrease a value by one, the increment and decrement operators make the job easier. Let's break it down in a simple way.

The increment and decrement operators are represented by `++` and `--`, respectively. They both allow you to adjust the value of a variable by `1`.

Instead of writing something like `x = x + 1` or `x = x - 1`, you can simply use `x++` to add `1`, or `x--` to subtract `1`. It's faster, cleaner, and easier to read.

There's a twist to how the increment and decrement operators work: they come in two forms, prefix and postfix, with the difference being when the value gets updated. For the increment operator, prefix is `++x` and postfix is `x++`.

Prefix (`++x`) increases the value of the variable first, then returns a new value. Postfix (`x++`) returns the current value of the variable first, then increases it:

```
let x = 5;

console.log(++x); // 6
console.log(x); // 6
```

In the code above, `++x` means "increment `x` first, then use it". So when you log `++x`, you immediately get the incremented value, which is `6`.

Now, let's take a look at an example using the postfix:

```
let y = 5;

console.log(y++); // 5
console.log(y); // 6
```

In this example, `y++` means "use `y` first, then increment it". When you log `y++`, you get `5`, but `y` becomes `6` after that line of code.

The decrement operator does the same thing as increment, except it decreases the value by `1`. Again, there are two forms: prefix (`--x`) decreases the value of the variable first, then returns the new value. And postfix (`x--`) returns the current value first, then decreases it:

```
let x = 5;
console.log(--x); // 4
console.log(x); // 4

let y = 5;
console.log(y--); // 5
console.log(y); // 4
```

So, which should you use: prefix or postfix? In many cases, it doesn't matter which one you use. Both get the job done. However, if you're using the value immediately in an expression, the difference becomes important. Let's take a look at this example:

```
let a = 5;
let b = ++a;
console.log(b); // 6 (a was incremented before assignment)

let c = 5;
let d = c++;
console.log(d); // 5 (c was incremented after assignment)
```

So, if you need the updated value right away, use prefix. If you want the current value first and you don’t care about the increment until later, go with postfix.

## What Are Compound Assignment Operators in JavaScript, and How Do They Work?

In JavaScript, all arithmetic operators have a compound assignment form. Compound assignment operators allow you to perform a mathematical operation and reassign the result back to the variable in one line of code. Instead of writing something like this:

```
let num = 5;
num = num + 2;

console.log(num); // 7
```

You can write something like this:

```
let num = 5;
num += 2;

console.log(num); // 7
```

Notice how `num += 2` combines both the addition and assignment steps into one. This saves time and reduces clutter in your code. Let's dive deeper into the most common compound assignment operators in JavaScript.

As you've already seen, the `+=` operator lets you add a value to an existing variable. It is known as the addition assignment operator. The addition assignment operator takes the current value of the variable, adds the specified number to it, and then assigns the result back to the variable:

```
let total = 10;
total += 5;

console.log(total); // 15
```

As you might guess, there's a subtraction assignment operator denoted by `-=`. The subtraction assignment operator subtracts the specified value from the current value of the variable and assigns the new value back to the variable:

```
let score = 20;
score -= 7;

console.log(score); // 13
```

If you didn't use the subtraction assignment, you'd have done something like this:

```
let score = 20;
score = score - 7;

console.log(score); // 13
```

The multiplication assignment operator is represented by `*=`. It multiplies the current value of the variable by the specified number and reassigns it back to the variable:

```
let points = 5;
points *= 3;

console.log(points); // 15
```

Lastly, there's a division assignment operator denoted by `/=`. Just like others before it, it lets you divide the current value of a variable by a number you specify, then assign the result back to the variable:

```
let balance = 100;
balance /= 4;

console.log(balance); // 25
```

Remember there's a compound assignment operator for every operator in JavaScript. So, apart from the four already mentioned, we also have:

- Remainder assignment operator (`%=`), which divides a variable by the specified number and assigns the remainder to the variable.
- Exponent assignment operator (`**=`), which raises a variable to the power of the specified number and reassigns the result to the variable.
- Bitwise AND assignment operator (`&=`), which performs a bitwise AND operation with the specified number and reassigns the result to the variable.
- Bitwise OR assignment operator (`|=`), which performs a bitwise OR operation with the specified number and reassigns the result to the variable.