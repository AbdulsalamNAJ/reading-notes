# HTML links
![image](https://static.tildacdn.com/tild6662-3039-4031-b362-303765336564/image1.png)

You can click on a it and jump to another document.
When you move the mouse over a link, the mouse arrow will turn into a little hand. A link does not have to be text. It can be an image or any other HTML element.  
`<a href=”https://www.w3schools.com/html/">Visit our HTML tutorial</a>`  
The href attribute specifies the destination address (https://www.w3schools.com/html/) of the link.
The link text is the visible part, clicking on the link will send you to the specified address.
Without a forward slash on subfolder addresses, you might generate two requests to the server. Many servers will automatically add a forward slash to the address, and then create a new request.
Local Links
The example above used an absolute URL (A full web address)
A local link (link to the same web site) is specified with relative URL (without http://www…).  
`<a href=”html_images.asp”>HTML Images</a>`

## Advanced positioning
![image](https://www.internetingishard.com/html-and-css/advanced-positioning/css-positioning-schemes-790d5b.png)

“Static positioning” refers to the normal flow of the page that we’ve been working with up ’til this point. The CSS Box Model, floats, and flexbox layout schemes all operate in this “static” flow, but that’s not the only positioning scheme available in CSS.

The vast majority of elements on a web page should be laid out according to the static flow of the page. These other positioning schemes come into play when you want to do more advanced things like tweak the position of a particular element or animate a UI component without messing up the surrounding elements.

### Relative positioning
![image](https://www.internetingishard.com/html-and-css/advanced-positioning/css-relative-positioning-26842e.png)
It moves elements around relative to where they would normally appear in the static flow of the page. This is useful for nudging boxes around when the default flow is just a little bit off.

### Absolute positioning
It is just like relative positioning, but the offset is relative to the entire browser window instead of the original position of the element. Since there’s no longer any relationship with the static flow of the page, consider this the most manual way to lay out an element.

### Fixed positioning
It has a lot in common with absolute positioning: it’s very manual, the element is removed from the normal flow of the page, and the coordinate system is relative to the entire browser window. The key difference is that fixed elements don’t scroll with the rest of the page.

## z-index
![image](https://www.internetingishard.com/html-and-css/advanced-positioning/css-z-index-c87ef0.png)

We’ve never had to deal with “depth” issues before. Until now, all our HTML elements rendered above or below one another in an intuitive way. But, since we’re doing advanced stuff, relying on the browser to determine which elements appear on top of other ones isn’t going to cut it.

The z-index property lets you control the depth of elements on the page. If you think of your screen as 3D space, negative z-index values go farther into the page, and positive ones come out of the page.

# Functions
![image](https://s3.ap-south-1.amazonaws.com/s3.studytonight.com/tutorials/uploads/pictures/1587882057-1.png)

Quite often we need to perform a similar action in many places of the script.

For example, we need to show a nice-looking message when a visitor logs in, logs out and maybe somewhere else.

## Function Declaration
To create a function we can use a function declaration.

It looks like this:

    function showMessage() {
    alert( 'Hello everyone!' );
    }

If we ever need to change the message or the way it is shown, it’s enough to modify the code in one place: the function which outputs it.

## LOCAL GLOBAL Variables
![image](https://dz2cdn1.dzone.com/storage/temp/14015304-3808.pic2.png)

### Local variables
A variable declared inside a function is only visible inside that function.

For example:

    function showMessage() {
    let message = "Hello, I'm JavaScript!"; // local variable
    alert( message );
    }

    showMessage(); // Hello, I'm JavaScript!

If a same-named variable is declared inside the function then it shadows the outer one. For instance, in the code below the function uses the local userName. The outer one is ignored:

    let userName = 'John';

    function showMessage() {
    let userName = "Bob"; // declare a local variable

    let message = 'Hello, ' + userName; // Bob
    alert(message);
    }

### Global variables
Variables declared outside of any function, such as the outer userName in the code above, are called global.

Global variables are visible from any function (unless shadowed by locals).

It’s a good practice to minimize the use of global variables. Modern code has few or no globals. Most variables reside in their functions. Sometimes though, they can be useful to store project-level data.

## Parameters

![image](https://miro.medium.com/max/5992/1*5NVJBxAp6J1KtAy0BuCAxg.png)

We can pass arbitrary data to functions using parameters (also called function arguments) .

In the example below, the function has two parameters: from and text.

    function showMessage(from, text) { // arguments: from, text
    alert(from + ': ' + text);
    }

    showMessage('Ann', 'Hello!'); // Ann: Hello! (*)
    showMessage('Ann', "What's up?"); // Ann: What's up? (**)

## Pair programming

![image](https://unruly.co/wp-content/uploads/2019/08/Screenshot-2019-08-13-at-16.09.46-1024x439.png)

All code to be sent into production is created by two people working together at a single computer. Pair programming increases software quality without impacting time to deliver. It is counter intuitive, but 2 people working at a single computer will add as much functionality as two working separately except that it will be much higher in quality. With increased quality comes big savings later in the project.

 The best way to pair program is to just sit side by side in front of the monitor. Slide the key board and mouse back and forth. Both programmers concentrate on the code being written.

 Pair programming is a social skill that takes time to learn. You are striving for a cooperative way to work that includes give and take from both partners regardless of corporate status. The best pair programmers know when to say "let's try your idea first." Don't expect people to be good at it from the start. It helps if you have someone on your team with experience to show everyone what it should feel like.


 ## References :

 https://weblog.west-wind.com/posts/2019/Jan/21/NonNavigating-Links-for-JavaScript-Handling
 https://www.internetingishard.com/html-and-css/advanced-positioning/