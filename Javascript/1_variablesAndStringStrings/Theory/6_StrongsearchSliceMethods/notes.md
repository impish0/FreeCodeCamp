## How Can You Test if a String Contains a Substring?

When working with strings in JavaScript, there are many cases where you might need to check whether a string contains a specific substring, which is a smaller part of that string.

For example, you might want to check if a user's input includes a specific word or character before performing some action. One way to achieve this is by using the `includes()` method.

The `includes()` method is used to check if a string contains a specific substring. If the substring is found within the string, the method returns `true` otherwise, it returns `false`.

Here's the basic syntax:

```
string.includes(searchValue);
```

For the syntax, the `searchValue` is the substring you want to look for within the string. And here's an example:

```
let phrase = "JavaScript is awesome!";
let result = phrase.includes("awesome");

console.log(result);  // true
```

In this example, the word `awesome` is found within the string `JavaScript is awesome!`, so the `includes()` method returns `true`.

It's important to note that the `includes()` method is case-sensitive. This means that the exact match of the characters is required, including their case.

For example:

```
let phrase = "JavaScript is awesome!";
let result = phrase.includes("Awesome");

console.log(result);  // false
```

Since `Awesome` (with an uppercase `A`) does not match `awesome` (with a lowercase `a`), the result is `false`.

You can also use the `includes()` method to check for a substring starting at a specific index in the string by providing a second parameter:

```
let text = "Hello, JavaScript world!";
let result = text.includes("JavaScript", 7);

console.log(result);  // true
```

Here, the search for the substring `JavaScript` starts from the 7th position in the string, ensuring it skips any characters before this position.

The `includes()` method only returns a `true` or `false` result. It does not provide information on where the substring is located in the string or how many times it occurs. If you need that level of detail, other methods, such as the `indexOf()` method might be more suitable.

## How Can You Extract a Substring from a String?

When working with strings in JavaScript, you often need to extract a portion or substring from a larger string.

For example, you may want to extract part of a word, a specific character sequence, or just a fragment of a sentence.

JavaScript provides several methods for this task, one of the most commonly used being the `slice()` method.

The `slice()` method allows you to extract a portion of a string and returns a new string, without modifying the original string. It takes two parameters: the starting index and the optional ending index.

Here's the basic syntax:

```
string.slice(startIndex, endIndex);
```

`startIndex` is the position where the extraction starts. `endIndex` is where the extraction ends. If not provided, `slice()` extracts until the end of the string.

Let's look at a simple example of extracting part of a string:

```
let message = "Hello, world!";
let greeting = message.slice(0, 5);

console.log(greeting);  // Hello
```

In this example, `slice(0, 5)` extracts characters starting from index `0` up to but not including index `5`. As a result, the word `Hello` is extracted.

If you omit the second parameter, `slice()` will extract everything from the start index to the end of the string:

```
let message = "Hello, world!";
let world = message.slice(7);

console.log(world);  // world!
```

Here, `slice(7)` extracts the string from index `7` to the end of the string, resulting in `world!`.

You can also use negative numbers as indexes. When you use a negative number, it counts backward from the end of the string:

```
let message = "JavaScript is fun!";
let lastWord = message.slice(-4);

console.log(lastWord);  // fun!
```

In this case, `slice(-4)` extracts the last four characters from the string, giving us `fun!`.

Let's say you want to extract a section from the middle of a string. You can provide both the starting and ending indexes to precisely control which part of the string you want:

```
let message = "I love JavaScript!";
let language = message.slice(7, 17);

console.log(language);  // JavaScript
```

Here, `slice(7, 17)` extracts the substring starting at index 7 and ending right before index `17`, which is the word `JavaScript`.

The `slice()` method is a powerful tool for extracting parts of a string in JavaScript.

You specify the start and end indexes, and the method returns a new string that contains the extracted portion.

With options for positive, negative, and omitted indexes, you can adapt it to various situations without altering the original string.