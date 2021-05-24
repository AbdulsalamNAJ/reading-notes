# HTML text fundamentals

One of HTML's main jobs is to give text structure and meaning (also known as semantics) so that a browser can display it correctly. This article explains the way HTML can be used to structure a page of text by adding headings and paragraphs, emphasizing words, creating lists, and more.

## Implementing structural hierarchy
For example, in this story, the <h1> element represents the title of the story, the <h2> elements represent the title of each chapter, and the <h3> elements represent sub-sections of each chapter:

    <h1>The Crushing Bore</h1>
    <p>By Chris Mills</p>
    <h2>Chapter 1: The dark night</h2>
    <p>It was a dark night. Somewhere, an owl hooted. The rain lashed down on the ...</p>
    <h2>Chapter 2: The eternal silence</h2>
    <p>Our protagonist could not so much as a whisper out of the shadowy figure ...</p>
    <h3>The specter speaks</h3>
    <p>Several more hours had passed, when all of a sudden the specter sat bolt upright and exclaimed, "Please have mercy on my soul!"</p>

It's really up to you what the elements involved represent, as long as the hierarchy makes sense. You just need to bear in mind a few best practices as you create such structures:

## Why do we need semantics?
Semantics are relied on everywhere around us—we rely on previous experience to tell us what the function of an everyday object is; when we see something, we know what its function will be. So, for example, we expect a red traffic light to mean "stop," and a green traffic light to mean "go." Things can get tricky very quickly if the wrong semantics are applied. (Do any countries use red to mean "go"? We hope not.)

In a similar vein, we need to make sure we are using the correct elements, giving our content the correct meaning, function, or appearance. In this context, the <h1> element is also a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page."

<h1>This is a top level heading</h1>
By default, the browser will give it a large font size to make it look like a heading (although you could style it to look like anything you wanted using CSS). More importantly, its semantic value will be used in multiple ways, for example by search engines and screen readers (as mentioned above).

On the other hand, you could make any element look like a top level heading. Consider the following:

<span style="font-size: 32px; margin: 21px 0; display: block;">Is this a top level heading?</span>
This is a <span> element. It has no semantics. You use it to wrap content when you want to apply CSS to it (or do something to it with JavaScript) without giving it any extra meaning. (You'll find out more about these later on in the course.) We've applied some CSS to it to make it look like a top level heading, but since it has no semantic value, it will not get any of the extra benefits described above. It is a good idea to use the relevant HTML element for the job.

## An introduction to Cascading Style Sheets
CSS is the acronym for: ‘Cascading Style Sheets’. CSS is an extension to basic HTML that allows you to style your web pages.

An example of a style change would be to make words bold. In standard HTML you would use the <b> tag like so:

<b>make me bold</b>
This works fine, and there is nothing wrong with it per se, except that now if you wanted to say change all your text that you initially made bold to underlined, you would have to go to every spot in the page and change the tag.

Another disadvantage can be found in this example: say you wanted to make the above text bold, make the font style Verdana and change its color to red, you would need a lot of code wrapped around the text:

    <font color="#FF0000" face="Verdana, Arial,  Helvetica, sans-serif">
    <strong>This is  text</strong></font>

This is verbose and contributes to making your HTML messy. With CSS, you can create a custom style elsewhere and set all its properties, give it a unique name and then ‘tag’ your HTML to apply these stylistic properties:

    <p class="myNewStyle">My CSS styled text</p>
And in between the tags at the top of your web page you would insert this CSS code that defines the style we just applied:

    <style type="text/css">
    .myNewStyle {
    font-family: Verdana, Arial, Helvetica, sans-serif;
    font-weight: bold;
    color: #FF0000;
    }
    </style>

Besides the fact that you will be cluttering up your pages with the same CSS code, you also find yourself having to edit each of these pages if you want to make a style change. Like with JavaScript, you can define/create your CSS styles in a separate file and then link it to the page you want to apply the code to:

<link href="myFirstStyleSheet.css" rel="stylesheet"  type="text/css">
The above line of code links your external style sheet called ‘myFirstStyleSheet.css’ to the HTML document. You place this code in between the <head> </head> tags in your web page.

## Basic JavaScript Instructions

### 1.Statements
An individual instruction or step in javascript. Ends with a semi colon

var today = new Date();

### 2.Comments
Used to explain code. You can have multi line using syntax /* */ or single line using // syntax . Any script surrounded by a comment is not processed by the js interpreter

### 3.Is Javascript a case sensitive language?
Yes. hournow and hourNow would be treated as two different items

### 4.code block
lines of code surrounded by curly braces { } do not end in a semi colon

### 5.Variable
variables are used to store bits of information. If you need to reuse a piece of information you're best to store it in a variable. Programmers say you declare a variable. You can then assign it a value. Variables stand in for a value, so rather than saying the specific number it represents (which may change), its use whatever is stored in this item instead
var dinosaur = "Spinosaurus";

### 6. =
This is the assignment operator. it assigns a value to a variable.

### 7.undefined
Until a variable has a value its undefined

### 8.Data types
Javascript variables can have a range of types.
numeric (e.g. 2, 0.75)
String ("Used for text)
Boolean (results in a true or false value)

There's also arrays, objects, undefined and null

### 9.Quote marks
Used to mark out strings. You can use single or double but they must match i.e. don't start with string ' and end with "

### 10.escaping quotes

Used when you want to show quote marks inside a string.

You can either use a backslash before a quote mark or Start the string with double quotes and then use single quotes inside the string
### 11.Booleans are useful...

1. When a value can only be true or false

2. When code can take more than a single path (allows us to test if a condition/s are true or false)
### 12. Rules for naming variables
    - must begin with a letter, dollar sign or underscore
    - names can contain letters, numbers, $ or an underscore
    - You cannot use keywords/reserved words
    - case sensitive
    - use a name that describes the info that the variable stores
    - camelcase

4 The For Loop
A for loop is a sequential statement that allows a designer to specify a fixed number of iterations in a behavioral design description. It is important to note that in VHDL, unlike other software programs, each iteration occurs concurrently, which means that the loop is “unrolled.” A for loop can be used only inside a sequential statement, such as a process statement, a function, or a procedure. The example in Figure 4.24 illustrates the form of a for statement. A for loop executes the sequential statement within its body each time the index of the loop changes its value within the range of the loop. The label of the for loop is optional; the user may choose not to include it.

![images](https://www.oreilly.com/library/view/introduction-to-digital/9780470900550/images/ch004-f024.jpg)

4.11.2 While Loop

A while loop is another form of sequential loop statement that specifies the conditions under which the loop should continue rather than specifying a discrete number of iterations. The condition ...

![images](https://www.oreilly.com/library/view/introduction-to-digital/9780470900550/images/ch004-f025.jpg)

**References:**

https://www.brainscape.com/flashcards/chapter-2-basic-javascript-instructions-3856200/packs/5586185