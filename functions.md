# Functions:
![image](https://pbs.twimg.com/media/D1j5S_wWsAc3lPB.jpg)

Quite often we need to perform a similar action in many places of the script.

For example, we need to show a nice-looking message when a visitor logs in, logs out and maybe somewhere else.

Functions are the main “building blocks” of the program. They allow the code to be called many times without repetition.

## To create a function we can use a function declaration

It looks like this:

    function showMessage() {
    alert( 'Hello everyone!' );
    }

The function keyword goes first, then goes the name of the function, then a list of parameters between the parentheses (comma-separated, empty in the example above) and finally the code of the function, also named “the function body”, between curly braces.

## We can use also function expressions

In JavaScript, a function is not a “magical language structure”, but a special kind of value.

The syntax that we used before is called a Function Declaration:

There is another syntax for creating a function that is called a Function Expression.

It looks like this:

    let sayHi = function() {
    alert( "Hello" );
    };

Here, the function is created and assigned to the variable explicitly, like any other value. No matter how the function is defined, it’s just a value stored in the variable sayHi.

The meaning of these code samples is the same: "create a function and put it into the variable sayHi".

## Parameters

We can pass arbitrary data to functions using parameters (also called function arguments) .

In the example below, the function has two parameters: from and text.

    function showMessage(from, text) { // arguments: from, text
    alert(from + ': ' + text);
    }

    showMessage('Ann', 'Hello!'); // Ann: Hello! (*)
    showMessage('Ann', "What's up?"); // Ann: What's up? (**)

## Returning a value

A function can return a value back into the calling code as the result.

The simplest example would be a function that sums two values:

    function sum(a, b) {
    return a + b;
    }

    let result = sum(1, 2);
    alert( result ); // 3

The directive return can be in any place of the function. When the execution reaches it, the function stops, and the value is returned to the calling code (assigned to result above).

## Naming a function

Functions are actions. So their name is usually a verb. It should be brief, as accurate as possible and describe what the function does, so that someone reading the code gets an indication of what the function does.

For instance, functions that start with "show" usually show something.

Function starting with…

    "get…" – return a value,
    "calc…" – calculate something,
    "create…" – create something,
    "check…" – check something and return a boolean, etc.

Examples of such names:

    showMessage(..)     // shows a message
    getAge(..)          // returns the age (gets it somehow)
    calcSum(..)         // calculates a sum and returns the result
    createForm(..)      // creates a form (and usually returns it)
    checkPermission(..) // checks a permission, returns true/false

With prefixes in place, a glance at a function name gives an understanding what kind of work it does and what kind of value it returns.