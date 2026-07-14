# Free Code Camp

## Variables and Strings
___

### Introduction to JavaScript
___

#### What Is a Data Type, and What Are the Different Data Types in JavaScript?
I
n JavaScript, a data type is the kind of value you store, like a number or piece of text.

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

* N/A Enable the interactive editor and try changing some of the integers to see it update in the console.

A floating point number is a number with a decimal point. Examples of floating point numbers include `3.14` and `5.2`.

* The next data type is a `String`.

A `String` is a sequence of characters, or text, enclosed in quotes. Here is an example string using double quotes:

`console.log("I love to code!");`

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

In this lesson, we'll focus on how string concatenation works, specifically using the + operator, the += operator, and the concat() method.

The + operator is one of the simplest and most frequently used methods to concatenate strings. It allows you to join multiple strings or combine strings with variables that hold text.

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



