# What is CSS?

![CSS](https://www.freetutorialsplus.com/css-tutorial/images/css-illustration.png)

CSS stands for *Cascading Style Sheets*. It is the language for describing the presentation of Web pages, including colors, layout, and fonts, that  making our web pages presentable to the users. 
CSS is designed to make style sheets for the web. It is independent of HTML and can be used with any HTML webpage.

## How I can edit CSS?
Some of the popular editors that are best suited to wire CSS code are as following:  

1.	Atom  
2.	Visual Studio Code  
3.	Notepad++ (Great for HTML & CSS)  
4.	Sublime Text (Best Editor)  


## CSS Syntax

![image](https://lucidar.me/en/web-dev-class/files/en-internal-css-syntax.png)

-	Selector: selects the element you want to target
-	Always remains the same whether we apply internal or external styling 
- There are few basic selectors like tags, id’s, and classes
-	All forms this key-value pair
- Keys: properties(attributes) like color, font-size, background, width, height.
- Value: values associated with these properties
## CSS Comment

![image](https://www.sitesbay.com/css/images/comment.png)

1.	Comments don’t render on the browser.  
2.	Helps to understand our code better and makes it readable.  
3.	Helps to debug our code.  

## CSS How-To 
### There are 3 ways to write CSS in our HTML file.
1.	Inline CSS
2.	Internal CSS
3.	External CSS

###	Priority order

*** Inline > Internal > External ***

**1. Inline CSS**

Before CSS this was the only way to apply styles, not an efficient way to write as it has a lot of redundancy, it's uniquely applied on each element.

####	Example:

    <h3 style=” color:red”> Have a great day </h3>
    <p  style =” color: green”> I did this , I did that </p>
  
**2. Internal CSS**

With the help of style tag, we can apply styles within the HTML file
Redundancy is removed, But the idea of separation of concerns still lost, uniquely applied on a single document

#### Example:
    < style>
      h1{
      color:red;
      }
    </style>  
    <h3> Have a great day </h3>

**3. External CSS**

With the help of <link> tag in the head tag, we can apply styles, file saved with .css extension, the idea of separation of concerns is maintained.

#### Example:
    <head>
     <link rel="stylesheet" type="text/css" href="name of the Css file">
    </head>

    h1{
     color:red;        
     //.css file
    }


## CSS Colors

![image](https://cdn.educba.com/academy/wp-content/uploads/2020/03/CSS-Color-Codes.jpg)

There are different colouring schemes in CSS used as the following:

**1. RGB**  

This starts with RGB and takes 3 parameter
3 parameter basically corresponds to red, green and blue
The value of each parameter may vary from 0 to 255.

**2. HEX**  

Hex code starts with # and comprises of 6 numbers which are further divided into 3 sets
Sets basically correspond to Red, Green, and Blue
Single set value can vary from 00 to 09 and AA to FF

**3. RGBA**  

This starts with RGB and takes 4 parameter
4 parameter basically corresponds to red, green, blue and alpha
Value of the first three parameters may vary from 0 to 255 and the last parameter ranges from 0 to 1

Implementation of different types of colours in CSS:

    <!DOCTYPE html>
    <html>
    <head>
	  <title>HTML</title>
	  <link rel="stylesheet" type="text/css" href="first.css">
    <style>
    .center{ 
    color:#ff0099;
    }	
    h1 {
    color:rgba(255,0,0,0.5);
    }

    </style> 
    </head>
    <body>
    <h1>This heading will be green</h1>
    <p style="color:rgb(255,0,0)">This paragraph will be red</p>
    <p  class="center">This paragraph will be pink and </p>
    </body>
    </html>