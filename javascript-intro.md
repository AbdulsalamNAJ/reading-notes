# So why do we need Javascript?
![javascript](https://insights.dice.com/wp-content/uploads/2020/07/shutterstock_1062509657.jpg)

JavaScript is a lightweight, cross-platform and interpreted scripting language. It is well-known for the development of web pages, many non-browser environments also use it. JavaScript can be used for Client-side developments as well as Server-side developments. 

## The story behind JavaScript:
 It was created in 1995 by Brendan Eich while he was an engineer at Netscape. It was originally going to be named LiveScript but was renamed. Unlike most programming languages, the JavaScript language has no concept of input or output. It is designed to run as a scripting language in a host environment.

## Javascript Expressions:

![image](https://imgs.developpaper.com/imgs/202002241908391.png)

The most common way to build a complex expression out of simpler expressions is with an operator. An operator combines the values of its operands (usually two of them) in some way and evaluates to a new value. The multiplication operator * is a simple example. The expression x * y evaluates to the product of the values of the expressions x and y. For simplicity, we sometimes say that an operator returns a value rather than “evaluates to” a value.

### 1. Primary Expressions

The simplest expressions, known as primary expressions, are those that stand alone—they do not include any simpler expressions. Primary expressions in JavaScript are constant or literal values, certain language keywords, and variable references.

Literals are constant values that are embedded directly in your program. They look like these:

    1.23          // A number literal
    "hello"       // A string literal
    /pattern/     // A regular expression literal
    true          // Evalutes to the boolean true value
    false         // Evaluates to the boolean false value
    null          // Evaluates to the null value
    this          // Evaluates to the "current" object
    i             // Evaluates to the value of the variable i.
    sum           // Evaluates to the value of the variable sum.
    undefined     // The value of the "undefined" property of the 

### 2. Object and Array Initializers

Object and array initializers are expressions whose value is a newly created object or array. These initializer expressions are sometimes called object literals and array literals. Unlike true literals, however, they are not primary expressions, because they include a number of subexpressions that specify property and element values. Array initializers have a slightly simpler syntax, and we’ll begin with those.

    []         // An empty array: no expressions inside brackets means no elements
    [1+2,3+4]  // A 2-element array.  First element is 3, second is 7

The element expressions in an array initializer can themselves be array initializers, which means that these expressions can create nested arrays:

    let matrix = [[1,2,3], [4,5,6], [7,8,9]];

### 3.  Function Definition Expressions

A function definition expression defines a JavaScript function, and the value of such an expression is the newly defined function. In a sense, a function definition expression is a “function literal” in the same way that an object initializer is an “object literal.” A function definition expression typically consists of the keyword function followed by a comma-separated list of zero or more identifiers (the parameter names) in parentheses and a block of JavaScript code (the function body) in curly braces. For example:

    // This function returns the square of the value passed to it.
    let square = function(x) { return x * x; };



### 4. Conditional Invocation

Array objects have a sort() method that can optionally be passed a function argument that defines the desired sorting order for the array elements. Before ES2020, if you wanted to write a method like sort() that takes an optional function argument, you would typically use an if statement to check that the function argument was defined before invoking it in the body of the if:

    function square(x, log) { // The second argument is an optional function
    if (log) {            // If the optional function is passed
        log(x);           // Invoke it
    }
    return x * x;         // Return the square of the argument
    }

## Javascript Operators:
![image](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/03/JavaScript-Operators-1200x720.jpg)

### 1. Assignment Operators

Name|	Shorthand|	Meaning
-----|------|------
Assignment|	x = y|	x = y
Addition Assignment	|x += y|	x = x + y
Subtraction Assignment	|x -= y	|x = x – y
Multiplication Assignment|	x *= y	|x = x * y
Division Assignment|	x /= y	|x = x / y
Remainder Assignment|	x % = y	|x = x % y
Exponentiation Assignment|	x **= y	|x = x ** y

### 2. Arithmetic Operators

Operator|	Type|	Description
--|--|---
Addition (+)|	Binary|	It returns the value after addition.
Subtraction (-)	|Binary|	It returns the value after subtraction.
Multiplication (*)|	Binary|	It returns the value after multiplying the operands.
Division (/)|	Binary|	It returns the value after dividing 2 operands.
Remainder (%)|	Binary|	It returns the integer remainder after dividing 2 operands.
Increment (++)|	Unary|	It adds 1 to the operand. For the prefix operator (++var2), it returns the value after adding 1. For the postfix operator (var2++), it adds 1 to the value then returns it.
Decrement (–)|	Unary|	It subtracts 1 from the operand. For the prefix operator (–var2), it returns the value after subtracting 1. For the postfix operator (var2–), it subtracts 1 from the value then returns it.
Unary negation (-)	Unary	It returns the negation of the value.
Unary plus (+)	Unary	It converts the operand to a number.
Exponentiation operator (**)	Binary	It calculates the base to the exponent power, i.e., baseexponent.

### 3. Comparison Operators

Operator|	Description
--|--
Equal (==) | It returns true if the operands are equal.
Not equal (!=)|	It returns true if the operands are not equal.
Strict equal (===)	| It returns true if the operands are equal and of the same type.
Strict not equal (!==)	| It returns true if the operands are of the same type but not equal, or are of different types.
Greater than (>)	| It returns true if the left operand is greater than the right operand.
Greater than or equal (>=)	| It returns true if the left operand is greater than or equal to the right operand.
Less than (>)	| It returns true if the right operand is greater than the left operand.
Less than or equal (>=)	| It returns true if the right operand is greater than or equal to the left operand.

##  Why is JavaScript so important?
![image](https://snipcart.com/media/204257/javascript-popularity-1.png)

Even if JavaScript has been the language of the browsers for a long time, it hasn’t been that long since it got (almost) universal recognition from the development community. 

We can also attribute the origin of this **JS revolution** to the release of ECMAScript 6 (or ECMAScript 2015). This update added new syntax for writing more complex applications and many other features that would define the next era of JavaScript.