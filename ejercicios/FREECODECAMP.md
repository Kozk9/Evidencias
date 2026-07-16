# Free Code Camp

## Variables and Strings
___

### Introduction to JavaScript
___

#### What Is a Data Type, and What Are the Different Data Types in JavaScript?

In JavaScript, a data type is the kind of value you store, like a number or piece of text.

A variable is a named container that stores a value of a specific data type, allowing you to reference and manipulate it throughout your code.

You might remember in math class working with variables like this:

``` 
x = 2
y = 4

x + y
``` 
You were able to create variables like `x` and `y` and then reference those throughout your program and do mathematical operations like addition. It is a similar concept in programming. You can create your own variable names and assign values to them. These values will be different data types.

Data types help the program understand the kind of data it's working with, whether it's a number, text, or something else.

JavaScript has several basic data types that you'll use in your programs. We'll explore each data type in greater detail in future lessons. For now, here is a brief introduction of the different data types in JavaScript.

* The first data type we will look at is the `Number` type.

A `Number` represents both integers and floating-point values. Examples of integers include `7`, `19`, and `90`.

*NOTE*: `console.log()` is a function that outputs information to the console, which is a part of your web browser used for debugging code. You will learn more about `console.log()` in future lessons. Also, the `//` symbols are used to add comments in your code. Comments are notes for yourself or other programmers that are ignored when the code runs.

A floating point number is a number with a decimal point. Examples of floating point numbers include `3.14` and `5.2`.

* The next data type is a `String`.

A `String` is a sequence of characters, or text, enclosed in quotes. Here is an example string using double quotes:

```
console.log("I love to code!");
```

Oftentimes you will use strings to represent names, labels, alert messages, etc.

Another data type used in JavaScript is the `Boolean` type.

A `Boolean` represents _one of two values_: `true` or `false`. For example, a program might check whether a user is logged in (`true`) or not (`false`) and change the page based on that. If the user is logged in, you probably want to show them the dashboard page. Otherwise, you will want to show them the login page.

The next two data types used in JavaScript are `undefined` and `null`.

`undefined` means a variable has been declared but hasn't been given a value yet. You will learn more about this in the next lesson.

`null` means the variable has been intentionally set to "nothing" and does not hold any value. We will explore more on how this works in future lessons.

The last three data types are more complex in nature. These are `Object`, `Symbol`, and `BigInt`.

An `Object` is a collection of key-value pairs.

```
{
  name: "Alice",
  age: 30
};
```

Objects are great for grouping related information together. You will learn more about how to work with objects in a future module.

A `Symbol` is a special type of value in JavaScript that is always unique and cannot be changed. It's often used to create unique labels or identifiers for properties:

```
Symbol('mySymbol');
```

BigInt is used for very large numbers that exceed the limit of the Number type:

```
1234567890123456789012345678901234567890n;
```

In this example, we create a `BigInt` by adding `n` at the end of a very large number.

`Symbol` and `BigInt` are two types that are less commonly used, but they are still important to know about.

Understanding these data types helps you handle and work with various kinds of data in your programs, as each type has its own characteristics and behaviors.

#### What Are Variables, and What Are Guidelines for Naming JavaScript Variables?

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

To assign a value to a variable you will need to use the assignment operator like this:

```
let age = 25;
```

Now when you use the `age` variable, it will return the value of `25`.

The assignment operator looks like an equals sign (`=`) but it doesn't check for equality. You'll learn about the correct operators for checking equality in future lessons.

The assignment operator is used to assign a value to a variable. This process of assigning a value to a variable is known as initialization.

One advantage of using the `let` keyword to declare variables is that you can reassign values to them. In programming, reassignment means giving a new value to a variable that already has one.

Here is an example of reassigning the value for the `age` variable.

```
let age = 25;
console.log(age); // 25
age = 30;
console.log(age); // 30
```

Now the `age` variable holds the value of `30`. Notice that the `let` keyword wasn't needed again because the `age` variable was already declared, so there's no need to declare it a second time.

When using reassignment, you only need to reference the variable name. Reassignment is useful because it allows you to update and change the value stored in a variable as your program runs. A good example of this would be updating points in a game.

Naming variables may seem straightforward, but there are some rules and best practices to ensure your code is readable and functional.

Your variable names should describe what the data represents. For example, instead of using a name like `x`, a more descriptive name such as `age` or `points` makes your code easier to understand.

```
// Bad variable names
let x = 10;
let y = "John";

// Good variable names
let age = 10;
```

Variables in JavaScript must begin with a letter, an underscore (`_`), or a dollar sign (`$`). They cannot start with a number.

```
// Valid variable names
let age;
let _score;
let $total;

// Invalid variable names
let 1stPlace; // starts with a number
```

Variable names are case-sensitive, meaning the word `age` in all lowercase and the word `Age` with a capital A are considered different variables.

```
let age = 25;
let Age = 30;
console.log(age); // 25
console.log(Age); // 30
```

This is why it's important to stick with a consistent naming convention like camelCase. camelCase is where the first word is all lowercase and each subsequent word starts with an uppercase letter.

Here is an example of using the camelCase naming convention for a variable:

```
let thisIsCamelCase;
let anotherExampleVariable;
let freeCodeCampStudents;
```

There are certain keywords in JavaScript that you cannot use as variable names, such as `let`, `const`, `function`, or `return`, as they are reserved for the language itself.

You should also avoid using special characters like exclamation points (`!`) or at (`@`) symbols, in your variable names. It is best to keep variable names readable by using letters, numbers, underscores, or dollar signs.

By following these guidelines, your code will be cleaner and more manageable as it grows in complexity.

#### How Do let and const Work Differently When It Comes to Variable Declaration, Assignment, and Reassignment?

When working with JavaScript, you'll often declare variables to store data that you plan to use throughout your program.

In modern JavaScript, `let` and `const` are the preferred ways to declare variables, but they differ in how they handle value assignment and reassignment.

In this lesson, we'll explore how let and const differ in variable declaration, assignment, and reassignment.

The `let` keyword allows you to declare variables that can be updated or reassigned later. You can think of let as a flexible container: once you've stored a value in it, you can change that value as needed throughout your program.

Here's an example of declaring and assigning a variable with let:

```
let score = 10;
```

In this case, the variable score is declared and assigned the value `10`. If you want to update the value later, you can easily do that:

```
let score = 10;
console.log(score); // 10
score = 20;
console.log(score); // 20
```

Now, score holds the value `20`. This makes let particularly useful when you know the value of a variable will change as your program runs.

On the other hand, `const` is used to declare variables that are constant. Once you assign a value to a variable declared with `const`, you cannot reassign it.

This makes `const` ideal for values that you don't want to change accidentally during the execution of your program.

Here's an example of declaring and assigning a variable with const:

```
onst maxScore = 100;
console.log(maxScore); // 100
```

Once maxScore is assigned the value `100`, it cannot be changed:

`maxScore = 200; // This will result in an error`

Trying to reassign a value to a `const` variable will throw an error in your JavaScript console, as `const` variables are immutable once they are assigned.

You can declare a `let` variable without immediately assigning it a value, and you can assign it a value later:

```
let age;
console.log(age); // undefined
age = 25;
console.log(age); // 25
```

Variables declared with `const` must be assigned a value at the time of declaration. If you try to declare a `const` variable without assigning it a value, you will get an error:

`const age; // Error: Missing initializer in const declaration`

You should use `let` when you need to declare variables that will be reassigned later. For example, tracking a changing score or updating a value over time in your program.

Use `const` when you want to declare variables that should remain constant, like configuration values or settings that shouldn't be changed accidentally.

You can also use the `var` keyword, but it's not as recommended anymore. The `var` is kind of like `let`, except it has a wider scope, which is more likely to cause problems in your program.

___

### Introduction to Strings

#### What Is a String in JavaScript, and What Is String Immutability?

In JavaScript, a string is a sequence of characters used to represent text data. Strings are one of the primitive data types in the language, along with numbers, booleans, `null`, and `undefined`.

To create a string in JavaScript, you can use single quotes (`'`), or double quotes (`"`).

Here is an example of creating two variables that hold string values:

```
let singleQuotes = 'This is a string';
console.log(singleQuotes);
let doubleQuotes = "This is also a string";
console.log(doubleQuotes);
```

Even though you can use single or double quotes to create strings, it's important to be consistent. If a string begins with a single quote, it must also end with a single quote.

The same applies to double quotes. The following example will throw an error because it starts with a double quote and ends with a single quote:

`const improperStr = "Do not do this';`

Another thing to take into account is that strings are immutable. In programming, immutability means that once something is created, it cannot be changed. So, when you create a string, you can't change its characters directly. Instead, you would create a new string if you want to make changes.

Here is an example of assigning a new string to a developer variable:

```
let developer = "Jessica";
console.log(developer);
developer = "Quincy";
console.log(developer);
```

Since strings are immutable, we can't update the first string directly. That is why we are assigning a new string to the `developer` variable.

Strings are an important part of programming, and in future lessons, you will learn advanced techniques for manipulating them and harnessing their full potential to create dynamic and interactive applications.

#### What Is String Concatenation, and How Can You Concatenate Strings with Variables?

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

#### What Is console.log Used For, and How Does It Work?

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

### Understanding Code Clarity

#### What Is the Role of Semicolons in JavaScript, and Programming in General?

In JavaScript, and many other programming languages, semicolons help delineate statements and improve code readability.

In JavaScript, a semicolon (`;`) is used to indicate the end of a statement.

Just as a period (`.`) marks the end of a sentence in English, a semicolon signifies the end of an executable line of code. This allows the JavaScript engine to distinguish between separate commands.

For example:

```
let variableOne = 5;  // Declare a variable and assign a value
let variableTwo = 10; // Declare another variable and assign a value
```

In this code, the semicolons at the end of each line mark the end of each statement. Without them, the JavaScript engine might have trouble interpreting where one statement ends and another begins.

Semicolons are primarily used to mark the end of a statement. This helps the JavaScript engine understand the separation of individual instructions, which is important for correct execution.

```
let a = 1;   // Statement ends here
let b = 2;   // Another statement starts here
```

While JavaScript has Automatic Semicolon Insertion (ASI) that can add semicolons automatically, explicitly including them improves code clarity and helps prevent errors that may arise from unexpected ASI behavior.

Semicolons are used in many programming languages, including C, C++, and Java.

Semicolons mark the end of statements or instructions, helping the compiler or interpreter parse the code correctly. A compiler translates high-level programming language code into machine-readable code, which creates an executable file.

By clearly delineating statements, semicolons contribute to the readability and maintainability of code. Semicolons help prevent ambiguities in code execution and ensure that statements are correctly terminated.

Semicolons are a fundamental part of JavaScript and many other programming languages.

They mark the end of statements, improve code readability, and help avoid errors related to Automatic Semicolon Insertion.

By understanding and using semicolons properly, you can write more reliable and maintainable code.

#### What Are Comments in JavaScript, and When Should You Use Them?

Comments in programming are used to provide additional context for the code or leave notes for yourself and others.

Comments are lines or blocks of text that are ignored by the JavaScript engine when your code is executed. They are there solely for the benefit of people reading the code, whether that's you or someone else.

JavaScript provides two ways to add comments to your code: single-line comments and multi-line comments.

Single-line comments are created using two forward slashes (`//`). Here is an example:

`// I am a single line comment in JavaScript`

This type of comment is great for brief explanations or clarifications.

Here is a real world example from the freeCodeCamp curriculum project files:

```
// This is to allow English to build without having to download the i18n files.
// It fails when trying to resolve the i18n-curriculum path if they don't exist.
const curriculumLocale = process.env.CURRICULUM_LOCALE ?? 'english';
const I18N_CURRICULUM_DIR = path.resolve(
  __dirname,
  curriculumLocale === 'english' ? '.' : 'i18n-curriculum/curriculum'
);
```

Do not worry about trying to understand what the code is actually doing because it is more advanced than what you have learned so far. Instead, focus on the comment left by the developer. This comment provides important context for why this code exists.

Comments like this are important for those working on teams for two reasons:

1. Other developers working on the project will understand the purpose of this code.

2. It helps prevent unnecessary changes or deletions without consulting the team, which could lead to bugs or issues.

Another type of comment is multi-line comments. Here is the basic syntax:

```
/*
 I am a multiline comment.
 This is helpful for longer explanations.
*/
```

Multi-line comments are useful when you need to write longer descriptions, explanations, or notes in your code.

Let's take another look at the freeCodeCamp curriculum project files to see how multiline comments can be used in the real world.

```
/* Since there can be more than one way to complete a certification (using the
legacy curriculum or the new one, for instance), we need a certification
field to track which certification this belongs to. */
const dupeCertifications = [
  {
    certification: 'responsive-web-design',
    dupe: '2022/responsive-web-design'
  }
];
const hasDupe = dupeCertifications.find(
  cert => cert.dupe === meta.superBlock
);
```

Just like before, ignore all of the JavaScript code because it uses concepts that haven't been taught yet. Instead, focus on the comment left by the developer.

A developer on the team, or even a new contributor working on the project, can understand why this piece of code is here and have the full context before working on this area of the project.

While comments are useful in programming, it is important to avoid over-commenting. You don't need to comment on every single line of code, especially if the code is straightforward and self-explanatory.

Here is an example of using comments to explain the obvious:

```
// This code uses the const keyword to create a new variable called price.
// We are assigning the number 10 to the price variable.
const price = 10;
```

In this situation, there is no need to add any comments here because the code is self-explanatory. The goal is to enhance readability, not clutter the code with unnecessary explanations.

If you want to add comments to your personal projects as you are learning to code, that is fine. But once you start working on real world projects with other developers, it is important not to use comments for code that is self-explanatory.

It is also important not to use comments to help explain away confusing, overly complicated, or poorly written code. In those situations, it is best to refactor, or change, your code so other developers will better understand what is going on.

Comments are powerful tools for documenting your code and making it easier to understand. You should use comments to provide context or leave notes for yourself and others.


### Lab

#### Build a Sentence Maker

```
// 1 & 2
let adjective = "little ";
let noun = "dog";
let verb = "playing";
let place = "town";
let adjective2 = "mad";
let noun2 = "cat";
// 3 & 4
let firstStory = "Once upon a time, there was a(n) " + adjective +" "+ noun +" who loved to eat " + noun2 +". The " + noun +" lived in a " + place + " and had " + adjective2 +" nostrils that blew fire when it was " + verb +".";
// 5
console.log("First story: " + firstStory)
// 6
adjective = "lovely ";
noun = "Lika";
verb = "dreaming";
place = "heart"
adjective2 = "beautyfull";
noun2 = "Kozk";
// 7 & 8
let secondStory = "Once upon a time, there was a(n) " + adjective +" "+ noun +" who loved to eat " + noun2 +". The " + noun +" lived in a " + place + " and had " + adjective2 +" nostrils that blew fire when it was " + verb +".";
// 9
console.log("Second story: " + secondStory)
```

### Working with Data Types

#### What Is Dynamic Typing in JavaScript, and How Does It Differ from Statically Typed Languages?

JavaScript is a dynamically typed language, meaning you don't need to specify the data type of a variable when you declare it. Instead, the type is determined based on the value assigned to the variable while the program is running. This allows you to change the type of a variable throughout the program.

Let's look at an example:

```
let example = "Hello";
example = 42;
```

In this example, we have a variable called `example` with the data type of string. But then we update value to be a number instead.

The flexibility of dynamic typing makes JavaScript more forgiving and easy to work with for quick scripting, but it can also introduce bugs that may be harder to catch, especially as your program grows larger.

In statically typed languages like C# or C++, you must declare the data type of a variable when you create it, and that type cannot change.

For instance, if you declare a variable as `integer`, you can only assign it integer values. If you try to assign it a different type, the program will throw an error.

Here's an example in C# language:

```
int data = 42; // data must always be an integer
data = "Hello"; // This would cause an error in C#
```

The difference between dynamic typing and static typing lies in the flexibility vs. the safety of your code. Dynamically typed languages offer flexibility but at the cost of potential runtime errors.

Statically typed languages enforce stricter rules that can prevent certain errors, but they require more upfront declaration and offer less flexibility in changing types.

Here is another example of creating a variable with a type set to `number` then changing it to later be of type `string`:

```
let data = 100;  // Initially a number
data = "New data";  // Dynamically changes to a string
```

In a statically typed language, this kind of change would not be allowed, as the data type would be fixed.

In conclusion, JavaScript's dynamic typing allows variables to change types freely, which offers flexibility but can lead to unexpected errors during execution.

Statically typed languages like Java require you to specify variable types upfront, which helps catch errors before the program runs but offers less flexibility.

#### Questions

> Which of the following best describes dynamic typing in JavaScript?

* You must declare the type of the variable before assigning a value.
* The data type of a variable is determined when it is assigned a value.
Correct!
* Variables can only hold one type of data.
* JavaScript does not allow changing variable types after they are declared.

> What is a key difference between dynamically typed languages and statically typed languages?

* Dynamically typed languages require you to declare variable types before assigning values.
* Statically typed languages allow changing variable types at runtime.
* Statically typed languages enforce a fixed variable type.
Correct!
* Dynamically typed languages do not allow variable reassignment.

> In JavaScript, what happens if you declare a variable and later assign it a value of a different type?

* JavaScript will throw a compile-time error.
* The variable will change to the new type without error.
Correct!
* The variable will retain its original type and ignore the new value.
* The program will crash.
___

#### How Does the typeof Operator Work, and What Is the typeof null Bug in JavaScript?

The `typeof` operator in JavaScript is a simple yet powerful tool that lets you see the data type of a variable or value. It always returns a string indicating the type.

Let's take a look at a few examples:

```
let num = 42;
console.log(typeof num); // "number"
```

In this first example, we have created a variable called `num` and assigned it the number `42`. When you use the `typeof` operator on the variable named `num`, it will return the string `number`.

Here is another example of using the `typeof` operator on variable called `isUserLoggedIn`:

```
let isUserLoggedIn = true;
console.log(typeof isUserLoggedIn); // "boolean"
```

When you use the `typeof` operator on the `isUserLoggedIn` variable, it will return a string `boolean` because the boolean `true` was assigned to the variable.

Using the `typeof` operator can be especially useful when you're debugging or trying to understand what kind of data you're working with in your code.

However, there's a well-known quirk in JavaScript when it comes to `null`.

Let's take a look at an example:

```
let exampleVariable = null;
console.log(typeof exampleVariable); // "object"
```

In this example, we have a variable called `exampleVariable` and have assigned it the value of `null`. But when we use the `typeof` operator, it returns the string `object`.

This is widely considered a bug in JavaScript, dating back to its early days. The reason for this behavior is rooted in the way JavaScript was originally designed.

When the language was first implemented, values like `null` were represented as a special type of object, leading to this unexpected result.

Unfortunately, this has become a part of the language, and while it's confusing, it's something you'll need to be aware of.

#### Questions

> What does the typeof operator return when used on a string in JavaScript?
* "string"
Correct!
* "text"
* "character"
* "object"

> Why is typeof null considered a bug in JavaScript?
* It returns "null" instead of "undefined".
* It returns "object" instead of "null".
Correct!
* It doesn't work on null.
* It returns an error.

> What does the typeof operator return when used on a number in JavaScript?
* "number"
Correct!
* "integer"
* "numeric"
* "float"
___

##### JavaScript Variables and Data Types Review

### Working with HTML, CSS, and JavaScript

While HTML and CSS provide website structure, JavaScript brings interactivity to websites by enabling complex functionality, such as handling user input, animating elements, and even building full web applications.

#### Data Types in JavaScript

Data types help the program understand the kind of data it's working with, whether it's a number, text, or something else.
* **Number**: A number represents both integers and floating-point values. Examples of integers include 7, 19, and 90.
* **Floating point**: A floating point number is a number with a decimal point. Examples include 3.14, 0.5, and 0.0001.
* **String**: A string is a sequence of characters, or text, enclosed in quotes. `"I like coding"` and `'JavaScript is fun'` are examples of strings.
* **Boolean**: A boolean represents one of two possible values: `true` or `false`. You can use a boolean to represent a condition, such as `isLoggedIn = true`.
* **Undefined** and **Null**: An `undefined` value is a variable that has been declared but not assigned a value. A `null` value is an empty value, or a variable that has intentionally been assigned a value of `null`.
* **Object**: An object is a collection of key-value pairs. The key is the property name, and the value is the property value.

Here, the `pet` object has three properties or keys: `name`, `age`, and `type`. The values are `Fluffy`, `3`, and `dog`, respectively.
```
let pet = {
  name: "Fluffy",
  age: 3,
  type: "dog"
};
```
* **Symbol**: The Symbol data type is a unique and immutable value that may be used as an identifier for object properties.

In this example below, two symbols are created with the same description, but they are not equal.

```
const crypticKey1= Symbol("saltNpepper");
const crypticKey2= Symbol("saltNpepper");
console.log(crypticKey1 === crypticKey2); // false
```
* **BigInt**: When the number is too large for the `Number` data type, you can use the BigInt data type to represent integers of arbitrary length.

By adding an n to the end of the number, you can create a BigInt.

`const veryBigNumber = 1234567890123456789012345678901234567890n;`

#### Variables in JavaScript

* Variables can be declared using the `let` keyword.

`let cityName;`

* To assign a value to a variable, you can use the assignment operator `=`.

`cityName = "New York";`

* Variables declared using `let` can be reassigned a new value.

```
let cityName = "New York";
cityName = "Los Angeles";
console.log(cityName); // Los Angeles
```

* Apart from `let`, you can also use `const` to declare a variable. However, a `const` variable cannot be reassigned a new value.
```
const cityName = "New York";
cityName = "Los Angeles"; // TypeError: Assignment to constant variable.
```
* Variables declared using `const` find uses in declaring constants, that are not allowed to change throughout the code, such as `PI` or `MAX_SIZE`.

#### Variable Naming Conventions

* Variable names should be descriptive and meaningful.
* Variable names should be camelCase like `cityName`, `isLoggedIn`, and `veryBigNumber`.
* Variable names should not start with a number. They must begin with a letter, `_`, or `$`.
* Variable names should not contain spaces or special characters, except for `_` and `$`.
* Variable names should not be reserved keywords.
* Variable names are case-sensitive. `age` and `Age` are different variables.

#### Strings and String immutability in JavaScript

Strings are sequences of characters enclosed in quotes. They can be created using single quotes and double quotes.
```
let correctWay = 'This is a string';
let alsoCorrect = "This is also a string";
```

* Strings are immutable in JavaScript. This means that once a string is created, you cannot change the characters in the string. However, you can still reassign strings to a new value.
```
let firstName = "John";
firstName = "Jane"; // Reassigning the string to a new value
```
#### String Concatenation in JavaScript

* Concatenation is the process of joining multiple strings or combining strings with variables that hold text. The `+` operator is one of the simplest and most frequently used methods to concatenate strings.

```
let studentName = "Asad";
let studentAge = 25;
let studentInfo = studentName + " is " + studentAge + " years old.";
console.log(studentInfo); // Asad is 25 years old.
```

* If you need to add or append to an existing string, then you can use the `+=` operator. This is helpful when you want to build upon a string by adding more text to it over time.
```
let message = "Welcome to programming, ";
message += "Asad!";
console.log(message); // Welcome to programming, Asad!
```
* Another way you can concatenate strings is to use the concat() method. This method joins two or more strings together.
```
let firstName = "John";
let lastName = "Doe";
let fullName = firstName.concat(" ", lastName);
console.log(fullName); // John Doe
```

#### Logging Messages with console.log()

* The `console.log()` method is used to log messages to the console. It's a helpful tool for debugging and testing your code.
```
console.log("Hello, World!");
// Output: Hello, World!
```

#### Semicolons in JavaScript

* Semicolons are primarily used to mark the end of a statement. This helps the JavaScript engine understand the separation of individual instructions, which is crucial for correct execution.
```
let message = "Hello, World!"; // first statement ends here
let number = 42; // second statement starts here
```
* Semicolons help prevent ambiguities in code execution and ensure that statements are correctly terminated.

#### Comments in JavaScript

* Any line of code that is commented out is ignored by the JavaScript engine. Comments are used to explain code, make notes, or temporarily disable code.
* Single-line comments are created using `//`.
```
// This is a single-line comment and will be ignored by the JavaScript engine
```
* Multi-line comments are created using `/*` to start the comment and `*/` to end the comment.

/*
This is a multi-line comment.
It can span multiple lines.
*/

#### JavaScript as a Dynamically Typed Language

* JavaScript is a dynamically typed language, which means that you don't have to specify the data type of a variable when you declare it. The JavaScript engine automatically determines the data type based on the value assigned to the variable.
```
let error = 404; // JavaScript treats error as a number
error = "Not Found"; // JavaScript now treats error as a string
```
* Other languages, like C#, that are not dynamically typed would result in an error:
```
int error = 404; // value must always be an integer
error = "Not Found"; // This would cause an error in C#
```
#### Using the typeof Operator

* The `typeof` operator is used to check the data type of a variable. It returns a string indicating the type of the variable.
```
let age = 25;
console.log(typeof age); // "number"

let isLoggedIn = true;
console.log(typeof isLoggedIn); // "boolean"
```
* However, there's a well-known quirk in JavaScript when it comes to `null`. The `typeof` operator returns `"object"` for `null` values.
```
let user = null;
console.log(typeof user); // "object"
```
___









































