JavaScript Object Literal


A JavaScript object literal is a comma-separated list of name-value pairs wrapped in curly braces. Object literals encapsulate data, enclosing it in a tidy package. This minimizes the use of global variables which can cause problems when combining code.

The following demonstrates an example object literal:

var myObject = {
sProp: 'some string value',
numProp: 2,
bProp: false
};
var myObject = {
sProp: 'some string value',
numProp: 2,
bProp: false
};
Object literal property values can be of any data type, including array literals, functions, and nested object literals. Here is another object literal example with these property types:

var Swapper = {
// an array literal
images: ["smile.gif", "grim.gif", "frown.gif", "bomb.gif"],
pos: { // nested object literal
    x: 40,
    y: 300
},
onSwap: function() { // function
    // code here
}
};
var Swapper = {
// an array literal
images: ["smile.gif", "grim.gif", "frown.gif", "bomb.gif"],
pos: { // nested object literal
    x: 40,
    y: 300
},
onSwap: function() { // function
    // code here
}
};
Object Literal Syntax:
Object literals are defined using the following syntax rules:

A colon separates property name from value. A comma separates each name-value pair from the next. A comma after the last name-value pair is optional. If any of the syntax rules are broken, such as a missing comma or colon or curly brace, a JavaScript error will be triggered. Browser error messages are helpful in pointing out the general location of object literal syntax errors, but they will not necessarily be completely accurate in pointing out the nature of the error.

Why and How We Use Object Literals
Several JavaScripts from dyn-web use object literals for setup purposes. Object literals enable us to write code that supports lots of features yet still provide a relatively straightforward process for implementers of our code. No need to invoke constructors directly or maintain the correct order of arguments passed to functions. Object literals are also useful for unobtrusive event handling; they can hold the data that would otherwise be passed in function calls from HTML event handler attributes.

There is one drawback: if you are unfamiliar with the syntax, it can be very easy to introduce errors which cause the code to stop working.

More About Object Literals Find out how to add, modify, and access properties of an object literal.

A property name needs to be enclosed in quotes if it contains spaces, other special characters, or a keyword reserved in JavaScript.

If a trailing comma is included, old versions of Internet Explorer will trigger an error: 'Expected identifier, string, or number'.