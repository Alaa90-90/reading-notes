## Functions ...
### Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.
there are two types of functions

1- Function declarations    
2- Function expressions


## Function declarations 
While the function declaration above is syntactically a statement, functions can also be created by a function expression.

const square = function(number) { return number * number }
var x = square(4) // x gets the value 16
Copy to Clipboard
However, a name can be provided with a function expression. Providing a name allows the function to refer to itself, and also makes it easier to identify the function in a debugger's stack traces:

const factorial = function fac(n) { return n < 2 ? 1 : n * fac(n - 1) }

console.log(factorial(3))

Such a function can be anonymous; it does not have to have a name. For example, the function square could have been defined as:

## 2- Function expressions

While the function declaration above is syntactically a statement, functions can also be created by a function expression.

Such a function can be anonymous; it does not have to have a name. For example, the function square could have been defined as:

const square = function(number) { return number * number }
var x = square(4) // x gets the value 16
Copy to Clipboard
However, a name can be provided with a function expression. Providing a name allows the function to refer to itself, and also makes it easier to identify the function in a debugger's stack traces:

const factorial = function fac(n) { return n < 2 ? 1 : n * fac(n - 1) }

console.log(factorial(3))
Copy to Clipboard
Function expressions are convenient when passing a function as an argument to another function. The following example shows a map function that should receive a function as first argument and an array as second argument.