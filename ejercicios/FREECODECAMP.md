# Free Code Camp

Fase 1: JavaScript desde Cero (con base de programación)

    Sintaxis básica: Tipos, operadores, estructuras de control (if, for, while).
    Funciones: declaración, expresiones, ámbitos y closures.
    Objetos y arrays literales: creación, acceso, mutación.
    Programación orientada a prototipos vs clases (ES6)
    El entorno Node.js: REPL, ejecuución de scripts, módilos nativos (fs, path, http).
    Documentar en el repo: snippets que contrasten con otros lenguajes (Python, Java, C#). Notas sobre el modelo de objetos de JS.


### What Is a Data Type, and What Are the Different Data Types in JavaScript?
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

## What Are Variables, and What Are Guidelines for Naming JavaScript Variables?

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

