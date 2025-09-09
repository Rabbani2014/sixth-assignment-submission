#### 1) What is the difference between var, let, and const?
Answer:1. **var**
var is the way to declare variables in JavaScript. It is function-scoped or globally scoped.If declared inside a function, it is accessible everywhere inside that function.If declared inside a block {} (like an if or for), it ignores the block and “escapes” to the function/global scope.

**let**
let is the modern way to declare variables. It is block-scoped.
If declared inside a { ... } block, it stays inside that block only. It cannot be redeclared in the same scope, but can be reassigned.

**const**
const is also block-scoped like let, but it creates a constant variable that cannot be reassigned. It must be initialized when declared.The variable binding cannot change, but if it’s an object/array, the contents can change.

#### 2) What is the difference between map(), forEach(), and filter()? 
Answer: **map()**
map() is used to transform an array. It creates and returns a new array containing the results of a function called on every element. The new array will have the exact same length as the original. The original array remains unchanged.

**forEach()** 
forEach() is used to iterate over an array and perform an action for each element. It does not return a new array; it always returns undefined. It's primarily used for side effects, like printing elements to the console.

**filter()**
filter() is used to select a subset of elements. It creates and returns a new array containing only the elements that pass a given test.The new array's length will be less than or equal to the original array's. The original array remains unchanged.

#### 3) What are arrow functions in ES6?
Answer: Arrow functions are a new way to write functions in ES6 (ECMAScript 2015) that provide a more concise syntax. They are a shorter alternative to traditional function expressions and have a different behavior regarding the this keyword.

**Key Features**
Concise Syntax: Arrow functions remove the need for the function keyword, parentheses (for a single argument), and curly braces (for a single statement).

this Binding: Arrow functions do not have their own this context. Instead, they inherit this from the parent scope. This is a significant difference from traditional functions, which have their own this value that depends on how they are called. This feature makes them particularly useful for callbacks and event handlers, where we often want to preserve the this context of the surrounding code.

#### 4) How does destructuring assignment work in ES6?
Answer: Destructuring assignment in ES6 is a powerful feature that allows us to unpack values from arrays or properties from objects into distinct variables. It provides a more readable and efficient way to extract data.

Array destructuring allows us to assign elements from an array to variables based on their position.
Syntax: [variable1, variable2, ...rest] = array

Object destructuring allows us to unpack properties from an object into variables with the same name.
Syntax: { property1, property2, ...rest } = object

#### 5) Explain template literals in ES6. How are they different from string concatenation?
Answer: Template literals are a way to create strings in ES6 that offer a more flexible and readable syntax than traditional string concatenation. They are enclosed by backticks (`) instead of single or double quotes.

**Features of Template Literals**
String Interpolation: We can embed expressions directly within a string using ${expression}. The expression can be a variable, an arithmetic operation, or even a function call. This is the main feature that makes them so useful.

Multiline Strings: Unlike regular strings, template literals can span multiple lines without needing a special newline character (\n). This makes writing multiline strings much cleaner.

Tagged Templates: This is a more advanced feature where we can parse template literals with a function. The function can receive the string parts and the interpolated values as arguments, giving us full control over how the string is constructed.

**Difference from String Concatenation**
The primary difference lies in how they combine strings and variables.

Template Literals use string interpolation with ${} to embed variables and expressions directly into the string, which results in much cleaner and more readable code.

String Concatenation uses the plus sign (+) to join strings and variables. This can quickly become messy and hard to read, especially with many variables or complex expressions.

In summary, template literals provide a modern, more readable and feature-rich way to handle strings, making them the preferred method in modern JavaScript development over traditional string concatenation.