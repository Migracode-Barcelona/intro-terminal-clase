# 1 - Hello Javascript

## Before the class

#### Fork the exercises module repo <a href="#fork-the-exercises-module-repo" id="fork-the-exercises-module-repo"></a>

Fork the [Javascript Module 1 repository](https://github.com/Migracode-Barcelona/javascript-module-1) to your personal account and clone it. Find help in the [Migracode GIT Guide](https://syllabus.migracode.org/git#fork-and-clone-an-existing-project-from-github). This is the repo we will use during the first Javascript module, and for homework.

### Learning Objectives <a href="#learning-objectives" id="learning-objectives"></a>

By the end of this class, you should be able to:

* Use `console.log()` to print information to the console
* List and describe the different primitive data types in JS
* Use `typeof` to find the type of a variable
* Assign data to variables using `let` and `const`
* Write, call and evaluate functions in JavaScript
* Manipulate strings with concatenation and interpolation techniques
* Manipulate numbers with mathematical operators using the `Math` library
* Define the difference between `console.log()` and `return`
* Call functions within functions
* Search and read documentation to help when you are stuck

## Hello World

It is programming tradition that the first thing you do in any language is make it output 'Hello world!'.

We'll do this in JavaScript, using a command called `console.log()`. The `console.log()` method writes a message to the console.

The console is a tool which is mainly used to log information - it's useful for testing purposes.

#### Exercise A (10 minutes) <a href="#exercise-a-10-minutes" id="exercise-a-10-minutes"></a>

(This exercise will help you understand how to run a basic JS script and explore the different ways you can run JS code)

1. Update your first `exercise-A.js` script in the folder `week-1/InClass` in the [Javascript Module 1 repository](https://github.com/Migracode-Barcelona/javascript-module-1) you forked before
2. Type `console.log("Hello World!")`
3. Run this script by going with the terminal to your directory and write `node exercise-A.js`, you will see the result of the console.log in the terminal

#### Exercise B (5 minutes) <a href="#exercise-b-5-minutes" id="exercise-b-5-minutes"></a>

(This exercise will help you expand your understanding of console.log)

1. Update the file `exercise-B.js` script in the folder `week-1/InClass`
2. Write 10 statements like these, but in different languages.

For example:

```
Halo, dunia! // Indonesian
Ciao, mondo! // Italian
Hola, mundo! // Spanish
```

## Variables

When you write code, you'll want to create shortcuts to data values so you don't have to write out the same value every time.

We can use a _variable_ to create a reference to a value. Variables can be thought of as named containers. You can place data into these containers and then refer to the data simply by naming the container.

Before you use a variable in a JavaScript program, you must declare it. Variables are declared with _let_ and _const_ keywords as follows.

```
let greeting = "Hello world";

console.log(greeting);
```

```
const name = "Irina";

console.log(name);
```

The program above will print "Hello world" to the console. Notice how it uses the value assigned to the variable `greeting`.

#### Exercise C (5 minutes) <a href="#exercise-c-5-minutes" id="exercise-c-5-minutes"></a>

1. Update the file `exercise-C.js` script in the folder `week-1/InClass`
2. Add a variable `greeting` to js1-week1.js and assign a greeting of your choice to the variable
3. Print your `greeting` to the console 3 times. You should see your greeting 3 times on the console, one on each line.

### Strings <a href="#strings" id="strings"></a>

In programming there are different _types of_ data. You've used one data type already: **string**.

Computers recognise strings as a sequence of characters but to humans, strings are simply lines of text.

```
const message = "This is a string";
```

Notice that strings are always wrapped **inside of quote marks**. We do this so that the computer knows when the string starts and ends.

You can check that the data is a string by using the `typeof` operator:

```
const message = "This is a string";
const messageType = typeof message;

console.log(messageType); // logs 'string'
```

#### Exercise D (5 minutes) <a href="#exercise-d-5-minutes" id="exercise-d-5-minutes"></a>

1. Update the file `exercise-D.js` script in the folder `week-1/InClass`
2. Write a program that:
   * creates a variable called `colors`
   * assigns colors "blue" and "yellow" as a comma separate string to `colors`
   * logs the type `colors` using `typeof`.
3. What is the `typeof` a number?

### String concatenation <a href="#string-concatenation" id="string-concatenation"></a>

You can add two strings together using the plus operator (`+`) or _string interpolation_.

String interpolation is a useful JavaScript feature that allows you to put variables directly into a string:

```
// Here is an example using the plus operator to concat strings
const greetingStart = "Hello, my name is ";
const name = "Daniel";

const greeting = greetingStart + name;

console.log(greeting); // Logs "Hello, my name is Daniel"
```

```
// Here is example using the String interpolation to concat strings
const greetingStart = "Hello";
const name = "Daniel";

const greeting = `${greetingStart}, my name is ${name}`;

console.log(greeting); // Logs "Hello, my name is Daniel"
```

#### Exercise E (5 mins) <a href="#exercise-e-5-mins" id="exercise-e-5-mins"></a>

1. Update the file `exercise-E.js` script in the folder `week-1/InClass`
2. Write a program that logs a message with a greeting and your name using the two concatenation methods we used

### Numbers as integers <a href="#numbers-as-integers" id="numbers-as-integers"></a>

The next data type we will learn is **number**.

Unlike strings, numbers do not need to be wrapped in quotes.

```
const age = 30;
```

You can use mathematical operators to calculate numbers:

```
const sum = 10 + 2; // 12
const product = 10 * 2; // 20
const quotient = 10 / 2; // 5
const difference = 10 - 2; // 8
```

#### Exercise F (10 mins) <a href="#exercise-f-10-mins" id="exercise-f-10-mins"></a>

1. Update the file `exercise-F.js` script in the folder `week-1/InClass`
2. Create two variables `numberOfStudents` and `numberOfMentors`
3. Log a message that displays the total number of students and mentors

**Expected result**

```
Number of students: 15
Number of mentors: 8
Total number of students and mentors: 23
```

### Numbers as decimals <a href="#numbers-as-decimals" id="numbers-as-decimals"></a>

Numbers can be integers (whole numbers) or floats (numbers with a decimal).

```
const preciseAge = 30.612437;
```

Numbers with decimals can be rounded to the nearest whole number using the `Math.round` function:

```
const preciseAge = 30.612437;
const roughAge = Math.round(preciseAge); // 31
```

#### Exercise G (15 mins) <a href="#exercise-g-15-mins" id="exercise-g-15-mins"></a>

1. Update the file `exercise-G.js` script in the folder `week-1/InClass`
2. Using the variables provided in the exercise calculate the percentage of mentors and students in the group (percentages must be a rounded to the nearest integer)
3. Using online documentation, what other things can you do with the `Math` library? Pick one thing on your table that you can do other than `Math.round` and prepare an explanation for the rest of the class

**Expected result**

```
Percentage students: 65%
Percentage mentors: 35%
```

## Functions

Functions are blocks of code that can do a task as many times as you ask them to. They take an input and return an output.

Here's a function that doubles a number:

```
function double(number) {
  return number * 2;
}
```

To use the function we need to: a) _call_ it with an input and b) do something with the returned value, for example assigning it to a variable

```
const result = double(2);

console.log(result); // 4
```

The input given to a function is called a **parameter**.

A function can take more than one parameter:

```
function add(a, b) {
  return a + b;
}
```

When you write a function (sometimes called _declaring a function_) you assign names to the parameters inside of the parentheses (`()`). Parameters can be called anything.

This function is exactly the same as the on above:

```
function add(num1, num2) {
  return num1 + num2;
}
```

#### Exercise H (20 minutes) <a href="#exercise-h-20-minutes" id="exercise-h-20-minutes"></a>

1. Update the file `exercise-H.js` script in the folder `week-1/InClass`
2. Design and create a function that:
   1. takes in more than one input
   2. uses string concatenation
   3. this means adding two strings together
   4. performs some form of operation on a number
   5. uses `return` to return a **string**
3. Add a comment above your function to explain what it does
4. Call your function and run your script
5. What's the difference between a `return` and `console.log`?
6. When would you choose to use functions over the way we have been scripting so far?

### Calling functions inside functions <a href="#calling-functions-inside-functions" id="calling-functions-inside-functions"></a>

Functions are very powerful.

* You can write more than one line of code inside of functions.
* You can use variables inside of functions.
* You can call other functions inside of functions!

```
function getAgeInDays(age) {
  return age * 365;
}

function createGreeting(name, age) {
  const ageInDays = getAgeInDays(age);
  const message =
    "My Name is " + name + " and I was born over " + ageInDays + " days ago!";
  return message;
}
```

#### Exercise I (20 mins) <a href="#exercise-i-20-mins" id="exercise-i-20-mins"></a>

1. Update the file `exercise-I.js` script in the folder `week-1/InClass`
2. Write a function that returns the year someone is born given their age as input
3. Using the answer from step 1, write a function that takes someone's name and age as input and returns a string that states the person's name and year they were born in a sentence

### Glossary <a href="#glossary" id="glossary"></a>

* Console: a place on your computer to run scripts or commands from
* Command: something that you type on your computer which performs an operation that your computer does
* Directory: another word for "folder" on your computer
* Parameter: a placeholder for values you can pass into functions
* Primitive type: a built-in type in JavaScript (e.g. strings and numbers are primitive types in JavaScript)
* Script: a file that contains a program
* Terminal: another word for "console"

## &#x20;<a href="#homework" id="homework"></a>

