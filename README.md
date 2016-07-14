# JavaScript Cheatsheet

Last updated 07/14/2016

## Primitives
Primitives are javascript building blocks

  - Boolean - `true` or `false`
  - Numbers - integers or floats
  - Strings - `"text"`
  - Undefined - value has not been defined
  - Null - intentional absence of an object value
  - Symbols (ecmaScript6)

## Variables

Container to store data (values)
Shortcut for storing data
  - Declared using `var`
  - Naming - Can't start with a number, no spaces, avoid symbols except `_`, `$`, `-`, name should be descriptive, best practice is to use camelCase


## Data Structures
  - Arrays - container for primitives(and other data structures), accessed via index, maintain ordered
  - Objects - key/value pairs, accessed via bracket or dot notation
methods, accesing data, etc.

## Programming Paradigms

Procedural vs functional
  - Procedural: JS renders commands in order (set of instructions)
  - Functional: break apart code/problem logically, generally separate state from behavior, reusable

## Flow Control

Flow control - decides which things run based on specific conditions or loops

Conditionals control the flow of the program
  - if, if-else, else-if
  - can be nested

## Loops

  - you can keep running a piece of code for a certain amount of iterations
  - infinite loop - loop that runs foreer, stack overflow, no more memory and computer crash :(

    for
    while
    for in
    for of
    do while

## Operators

  Math - `+`, `-` , `*`, `/`, `%`, can combine (`++`, `+=`)
  Logical
  Comparison `===` (strict), `==` (loose), `<`, `>`, `>=`, `<=`, `!`

## functions
  functions

  Set of instructions that achieve a specific task defined by code block. Can be defined, and then invoked to return some output, can contain parameters (when defined) and arguments (pass in when called/invoked)

  - methods vs functions: method is a function that is contained within an Object
  - functions are first class citizens and can be used as arguments (just like the primitives and data structures) in JS
  - functions always return something; if not explicitly set, then it returns `undefined`
  - expression vs declaration
  - can have optional (see Higher OrderF functions)
## scope
  - range in which a variable can be accessed
  - global and local (function/lexical)
  - global - accessible everywhere; local accessible only when the functionis invoked

  ```
  function foo(){
    var test = 'some string'
      function bar() {
        console.log(test);
    }
  }
  ```

## hoisting

The process by which the computer moves all variable declarations to the top of the applicable scope, so that it never encounters a variable it is unaware of. It's important to note that it does not move the variable assignment to the top of the page.

`var foo = 'bar'`

moves declarations (`var foo;`) BUT NOT assignment ('var foo = bar')

## callbacks

  A function that takes other functions as arguments or returns functions as its result is called a higher-order function, and the function that is passed as an argument is called a callback function.

  It's named “callback” because at some point in time it is “called back” by the higher-order function

  IE
    - function add (num) {
        return function (input) {
          return input + num;
        }
    }

  async - different code can run at different times

  what happens if one function is dependent on another functions output?

  function() {
    (this takes 20 mins to run then returns)
    return 'ing'
  }

  function test(arg) {
    return 'test' + arg
  }

## string concatenation

  used to join 2 or more string
  ```
  'test' + 'ing'
  ```

  ```
  'test'.concat('ing') => 'testing'
  ```

  you can also use `+=`

## computer science
bigO Notation

Big-O notation is how developers discuss the complexity of an algorithm as a way to understand how fast a program will run given it's input. Big-O notation deals with the worst case scenario for the algorithm. In other words, if the program may run quickly, but there is a chance it could take a long time given some input, then the Big-O runtime will deal with the longer case.

* O(n)
  * Linear Time - Directly related to input size (longer input, longer runtime)
* O(1)
  * Constant time - It's bound by a constant number. Regardless of input
* O(n^2)
  * Quadratic time - A loop that iterates over all tiems nested within a loop that also iterates over all items.
  The Exponent grows based on the number of nested loops.

  A "flogarithm" of a positive number (n) represent by (log(n)) is the number of digits it has.

* Factorials - Way Worse than quadratic wayyyyyyyyyyyyyyyy worse

[Big O Cheat Sheet](http://bigocheatsheet.com)
