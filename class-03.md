# HTML Lists
![image](https://static.javatpoint.com/htmlpages/images/html-lists.png)

HTML Lists are used to specify lists of information. All lists may contain one or more list elements. There are three different types of HTML lists:

Ordered List or Numbered List (ol)
Unordered List or Bulleted List (ul)
Description List or Definition List (dl)
Note: We can create a list inside another list, which will be termed as nested List.
HTML Ordered List or Numbered List
In the ordered HTML lists, all the list items are marked with numbers by default. It is known as numbered list also. The ordered list starts with <ol> tag and the list items start with <li> tag.

    <ol>  
    <li>Aries</li>  
    <li>Bingo</li>  
    <li>Leo</li>  
    <li>Oracle</li>  
    </ol>  



HTML Unordered List or Bulleted List
In HTML Unordered list, all the list items are marked with bullets. It is also known as bulleted list also. The Unordered list starts with <ul> tag and list items start with the <li> tag.

    <ul>  
    <li>Aries</li>  
    <li>Bingo</li>  
    <li>Leo</li>  
    <li>Oracle</li>  
    </ul>  

HTML Description List or Definition List
HTML Description list is also a list style which is supported by HTML and XHTML. It is also known as definition list where entries are listed like a dictionary or encyclopedia.

The definition list is very appropriate when you want to present glossary, list of terms or other name-value list.

The HTML definition list contains following three tags:

    <dl> tag defines the start of the list.
    <dt> tag defines a term.
    <dd> tag defines the term definition (description).
    <dl>  
      <dt>Aries</dt>  
      <dd>-One of the 12 horoscope sign.</dd>  
      <dt>Bingo</dt>  
      <dd>-One of my evening snacks</dd>  
    <dt>Leo</dt>  
    <dd>-It is also an one of the 12 horoscope sign.</dd>  
      <dt>Oracle</dt>  
      <dd>-It is a multinational technology corporation.</dd>   
    </dl>  

HTML Nested List
A list within another list is termed as nested list. If you want a bullet list inside a numbered list then such type of list will called as nested list.

Code:

    <!DOCTYPE html>  
    <html>  
    <head>  
        <title>Nested list</title>  
    </head>  
    <body>  
        <p>List of Indian States with thier capital</p>  
    <ol>  
        <li>Delhi  
            <ul>  
                <li>NewDelhi</li>  
            </ul>  
        </li>  
        <li>Haryana  
            <ul>  
                <li>Chandigarh</li>  
            </ul>  
        </li>  
        <li>Gujarat  
            <ul>  
                <li>Gandhinagar</li>  
            </ul>  
        </li>  
        <li>Rajasthan   
            <ul>  
                <li>Jaipur</li>  
            </ul>  
        </li>  
        <li>Maharashtra  
            <ul>  
                <li>Mumbai</li>  
            </ul>  
        </li>  
        <li>Uttarpradesh  
            <ul>  
                <li>Lucknow</li></ul>  
        </li>  
    </ol>  
    </body>  
    </html>  

## The CSS Box Model
![image](https://codinglead.github.io/images/box-model.png)

Throughout our HTML Basics tutorial, we referred to HTML elements as "containers," because most of them are meant to hold things like content or other HTML elements. However, CSS takes that concept a step further. When it comes to CSS, every HTML element is considered to be a box with distinct layers. This concept is called the box model.

labeled diagram of box model, showing margins, borders, and padding
What is the box model?
Every block-level HTML element you put on a webpage is a box, even if it doesn't ordinarily look like it. For example, if you add a <p> element to your webpage and load it, it initially looks like it's just loose text. If you add some CSS colors, though, you can see the square box shape:

![image](https://media.gcflearnfree.org/content/5ef2084faaf0ac46dc9c10be_06_23_2020/basicparagraph.PNG)

A paragraph with colors
The box model defines the different parts of that shape, which are broken up into four pieces, or sub-boxes:

Content: the inner content of your HTML element. In a <p> element, for example, this is the area where text would be displayed. In the image above, it's the entire area made visible with the background color. 
Padding: a box that surrounds an HTML element's inner content. In the image below, it's the extra space around the content that also shares the background color: 

![image](https://media.gcflearnfree.org/content/5ef2084faaf0ac46dc9c10be_06_23_2020/paragraph-with-padding.PNG)

A paragraph with padding
Border: a box that surrounds an HTML element's padding. In the image below, it's the darker space around the padding: 

![image](https://media.gcflearnfree.org/content/5ef2084faaf0ac46dc9c10be_06_23_2020/paragraph-with-border.PNG)

A paragraph with padding and a border
Margin: a functionally invisible box that surrounds an HTML element's border. The margin is meant to act as white space to separate HTML elements from each other. In the image below, it's the white spaces between and around the two paragraphs: 

![image](https://media.gcflearnfree.org/content/5ef2084faaf0ac46dc9c10be_06_23_2020/two-paragraphs2.PNG)

Two paragraphs with padding and borders
You may not always style all four of these sub-boxes, so they may not always be visible. Regardless, they are part of the make-up of every block-level HTML element.

Inline HTML elements are still boxes, but they don't respect all of the box model behavior and aren't as flexible. You'll get a feel for the differences over time, but in general, inline elements are incompatible with any CSS that would disrupt the basic flow of a line of text.

In particular, let's consider the height and width declarations you can use to resize HTML elements. While at first glance they may appear to resize an element as a whole, they are actually only resizing an element's content. The padding, border, and margin boxes can be resized separately from the content. Take this paragraph as an example:

![image](https://media.gcflearnfree.org/content/5ef2084faaf0ac46dc9c10be_06_23_2020/paragraph-no-height.PNG)

paragraph with no height
 It has been styled to add to the padding and border and make them visible. Now let's add a height: 50px; declaration to it:

![image](https://media.gcflearnfree.org/content/5ef2084faaf0ac46dc9c10be_06_23_2020/paragraph-with-height.PNG)

paragraph with height
Notice that while the content box has increased in size, the padding and border boxes have remained the same.

Try this!
We'll talk about margins, borders, and padding in more detail in the following lessons, but try adding each of these declarations, one by one, to the input below:

    background-color: #15AAD7;
    color: white;
    padding: 10px;
    border: solid 3px #0F7391;
    margin: 10px;

## Basic JavaScript Instructions

![image](https://lh3.googleusercontent.com/-YXC3gtpMlko/X3HA5DHH6MI/AAAAAAAAB3Q/VYM81zAFldY-cItuj7GMYA0Xy7Fy0GWBgCLcBGAsYHQ/image.png)


In JavaScript, we can assign strings to a variable and use concatenation to combine the variable to another string.
To concatenate a string, you add a plus sign+ between the strings or string variables you want to connect.

    let myPet = 'seahorse';
    console.log('My favorite animal is the ' + myPet + '.'); 
    // My favorite animal is the seahorse.

Using a single quote or a double quote doesn’t matter as long as your opening and closing quotes are the same. The one time it matters if you are using a word that has an apostrophe like “I’m”. It will be easier to use a double quote instead of using an escape character.

Another thing to take note of is when concatenating numbers and strings. When you concatenate a number with a string, the number becomes a string.

    let myAge = 85;
    console.log("I am " + myAge + " years old.");
    // I am 85 years old.

Another way to include a variable to a string is through String Interpolation. In JavaScript, you can insert or interpolate variables into strings using template literals. Here is an example of a template literal using our first example:

    let myPet = 'seahorse';
    console.log(`My favorite animal is the ${myPet}.`);

Template literals are enclosed in backticks. You write the string as normal but for the variable you want to include in the string, you write the variable like this: ${variableName} . For the example above, the output will be the same as the example before it that uses concatenation. The difference is, the interpolation example is much easier to read.

## Enclosing quotation marks

![image](https://media.vlpt.us/images/suyeonme/post/1d76ad97-4289-461d-a93a-d7c988ad7f56/Screen%20Shot%202020-08-27%20at%209.54.07%20AM.png)

You can use a backslash (\) with the particular word or string to escape the quotation mark. Remember one thing; if you do not want to use the backslash (\), you have to use the quotation mark alternatively inside and outside of a string. This means that if you try to use a single quote inside a string, the outside quotes should be double quotes. Similarly, if you try to use a double quote inside a string, the outside quotes must be single quotes.

Let's see how it will be done in JavaScript.

Example: Print quotes using backslash (\)
In this example, we will use the backslash (\) to escape the quotation mark.


    <html>  
    <body>  
    <script>  
    var ssingleQ = 'It\'s nine o\' clock in the morning.';  
    var doubleQ = "Mukesh Ambani is \"the richest man\" of India.";  
    document.write(singleQ + "</br>");  
    document.write(doubleQ + "</br>");  
    </script>  
    </body>  
    </html>  