# An HTML document has two main parts:

head. The head element contains title and meta data of a web document.
body. The body element contains the information that you want to display on a web page.

To make your web pages compatible with HTML 4, you need to add a document type declaration (DTD) before the HTML element. Many web authoring software add DTD and basic tags automatically when you create a new web page.

In a web page, the first tag (specifically, <html>) indicates the markup language that is being used for the document. The <head> tag contains information about the web page. Lastly, the content appears in the <body> tag. The following illustration provides a summary.

![image](https://letzcode.in/learn/html/Chapters/images/img1.png)

Understanding elements
To markup your web pages, you will need to learn the syntax (rules of a computing language) of HTML. HTML syntax is very simple to follow. Remember the syntax only controls the presentation or structure of a web page. The most fundamental piece of building block of HTML is the elements.

In HTML, an element refers to two different things:

element of structure of a document (for example, paragraph, web page title, etc.).
element in the sense of a tag (for example, <p>, <title>)
Because of the different meanings of the word "element", it can be confusing what the word "element" means in a particular context. The following discussion may help you to understand the differences in the meaning. When we talk about the element in the sense of element of structure of a document, we are referring to the structure of the document; for example, document's header information (head), title, body, etc. When, however, we use the word element to refer to a tag, we are talking about a specific HTML instruction that uses angled brackets like: <>. As the following table shows,

Examples of elements of structure of a document
head	body	p
Examples of elements as tags
<head>	<body>	<p>
an element becomes a tag when we use the angled brackets around it. To create a web page, we use tags. A tag instructs the browser what specific instruction to execute. Assume in your web page you want to emphasize some text as bold. To do this, HTML requires three pieces of information from you:

The <b>World Wide Web Consortium</b> (W3C) is a rule-making body for the Web.
Most elements in HTML have three parts: start tag, content, and end tag. The start tag is simply the element name surrounded by the angled brackets such as <b>, <body>, and <p>. The end tag is a element name surrounded by </ and > such as </b>, </body>, and </p>. In other words, an end tag simply has the forward slash (/) before the element name. So if you open (start) a tag with <i>, you will close (end) it with </i>.


## Understanding attributes

![image](https://s3.ap-south-1.amazonaws.com/s3.studytonight.com/tutorials/uploads/pictures/1589352735-1.png)

In HTML, elements (or tags) have attributes or properties. As an HTML writer, attributes allow you to add extra instruction to your tags. Because each tag has its own unique attributes, you have to learn which attribute(s) belongs which tag. (See the attributes reference table for details.) Any attribute cannot be just applied to any tag. Think of attributes as options. As such, options can only be applied to tags if the tags offer those options. If you incorrectly apply an option to a tag, the browser is likely to ignore that option.

An attribute has two parts: attribute name and attribute value. Because of these two-parts, they are also referred to as pairs. The attribute name identifies (or defines) what special instruction you want to add to a particular tag. The attribute value, on the other hand, indicates (usually predefined) option for that attribute. So if you are going to use an attribute, you will need to have value for that attribute. Let's go over the actual HTML.

The following shows the HTML code for the top paragraph:

<p align="right">This is my paragraph. Normally, text and other object on a web page are left-aligned. Because this paragraph has an extra instruction (align="right") to start this particular paragraph from the right, the paragraph is right-aligned.</p>
We stated earlier that an attribute adds an extra instruction to a tag. When does this extra instruction stop executing (or finish applying value of the attribute)? This is an important question because many times you will have nested tags and it may not be clear to you when the instruction will stop. The answer is that the instruction stops once the browser encounters the corresponding ending tag for the tag that contains the attribute. In our example, any text outside of this paragraph tag will be unaffected (specifically will not be right-aligned) because we apply the attribute to just one <p> tag.

## DOCTYPES
![image](https://www.seobility.net/en/wiki/images/a/a6/HTML-Doctype.png)

DOCTYPE must be used to tell a browser which version of HTML the page is using.
DOCTYPE can also help the browser to render a page correctly.

HTML5

<!DOCTYPE html>
HTML4

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
Transitional XHTML 1.0

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
Strict XHTML 1.0

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
XML Declaration

<?xml version="1.0" ?>
## Comment

    <!--Comment--> is used to add comments in the code.  

## Id & Class
attribute id is used to uniquely identify the element from other elemnts on the page. In additional, it can be styled differently than any other instance of the same element by CSS.
attribute class is used to identify several elements from other elements on the page.
    <!-- both have the properties of the class named importance -->
<p class="important">For a one-year period from November 2010, the Marugame Genichiro-Inokuma Museum of Contemporary Art (MIMOCA) will host a cycle of four Hiroshi Sugimoto exhibitions.</p>
<p>Each will showcase works by the artist thematically contextualized under the headings "Science," "Architecture," "History" and "Religion" so as to present a comprehensive panorama of the artist's oeuvre.</p>

<p class="important admittance">Hours: 10:00 – 18:00 (No admittance after 17:30)</p>

##  Grouping
<div> allows you to group a set of elements together in one block-level box.
<span> acts like an inline equivalent of the <div> and is used to contain a section of text, or to contain a number of inline elements.
## IFrames
<iframe> is used to cut a little window in your page and see another page on this window.
attributes scrolling is only supported in HTML4 and XHTML, for indicating whether the iframe should have scrollbars or not.
attributes frameborder is only supported in HMTL4 and XHTML, for indicating whether the frame should have a border or not.
attributes seamless is come in HTML5, for indicating that scrollbars is not desired in the iframe.
<iframe width="450" height="350" src="http://maps.google.co.uk/maps?q=moma+new+york&amp;output=embed">
</iframe>

![image](https://raw.githubusercontent.com/aleen42/PersonalWiki/docs/Programming/HTML/extra_markup/iframe.png)

## Information about the page
<meta> lives inside `<head> to contain information about the page.
attribute name is set as 'description' to contain the description of the page.
attribute name is set as 'keywords' to contain a list of keywords of the page.
attribute name is set as 'robots' to indicate whether search engines should add this page to their search results or not.
attribute httl-equiv is set as 'author' to define the author of the web page.
attribute httl-equiv is set as 'pragma' to prevent the browser from caching the page.
attribute httl-equiv is set as 'expires' to indicate when the page should expire and no longer be cached.
<head>
    <title>Information About Your Pages</title>
    <meta name="description" content="An Essay on Installation Art" />
    <meta name="keywords" content="installation, art, opinion" />
    <meta name="robots" content="nofollow" />
    <meta http-equiv="author" content="Jon Duckett" />
    <meta http-equiv="pragma" content="no-cache" />
    <meta http-equiv="expires" content="Fri, 04 Apr 2014 23:59:59 GMT" />
</head>

## HTML | Layout
Difficulty Level : Medium
Last Updated : 23 Jul, 2019
Page layout is the part of graphic design that deals with the arrangement of visual elements on a page. Page layout is used to make the web pages look better. It establishes the overall appearance, relative importance, and relationships between the graphic elements to achieve a smooth flow of information and eye movement for maximum effectiveness or impact.

![image](https://media.geeksforgeeks.org/wp-content/uploads/layout.png)

## html wireframes
![image](https://cronuts.digital/wp-content/uploads/2018/09/wireframe-CROnuts-1024x635.png)

For the first few years of my career, I didn’t know that wireframes existed. It wasn’t until I started working at a larger agency that I first encountered a strange new black-and-white InDesign world, where multiple rounds of 100+ page PDFs were generated and presented to clients.

While a lot of great thinking goes into these highly-detailed wireframes, the actual artifact creates a lot of issues.

Writing a Simple JavaScript Application
In this section, you explore the process of JavaScript development with a simple JavaScript application. This application doesn't do much, but it will help you understand the steps required to develop and test a script. You'll find much more sophisticated examples throughout this book.

## Creating the Script
First, let's look at a very simple JavaScript application. The following script simply displays the location of the current page and a brief message. This script will be combined with an HTML page and its use demonstrated.

document.write("<B> location: </B>" + document.location + "<br>")
document.write("This is a test of JavaScript." + "<br>")
After you've created the script, you need to do two things:

Embed the script in the HTML page. You can use the <SCRIPT> tag to do this, or use an event handler.
Test the script by viewing the document with Netscape.
Embedding the Script in an HTML Page
There are two ways to embed a JavaScript script in your HTML page. Each has its advantages and disadvantages. In a complex JavaScript application, you'll end up using both of these methods several times.

Using the <SCRIPT> tag
The simplest method of including a JavaScript script in an HTML page is to use the <SCRIPT> tag, as described earlier in this chapter. This tag is usually used as a container, and the script is included directly after it. Listing 1.3 adds the necessary opening and closing <SCRIPT> tags to the script:

## Listing 1.3. A simple example of the <SCRIPT> tag.
    <!-- <SCRIPT language=JAVASCRIPT>
    document.write("<B> location: </B>" + document.location + "<br>")
    document.write("This is a test of JavaScript." + "<br>")
    </SCRIPT> -->
Notice the strange syntax. The extra brackets and exclamation marks indicate a comment; the entire script is marked as a comment so that older browsers will not attempt to display it. JavaScript-aware browsers will execute it correctly.

If you use this method within the body of a Web page, the script will be executed immediately when the page loads, and the output of the script will be included at that point in the page. You can also use the <SCRIPT> tag within the header of a page to prevent it from executing immediately. This can be useful for subroutines that you will call later.

## Creating an Event Handler
An alternate approach is to use an event handler to perform a script when a certain event occurs. This is best used when you want to act on the press of a button or the entry of a field.

Rather than use the <SCRIPT> tag, an event handler is inserted as an attribute to an HTML tag. Tags that support event handlers include <LINK>, <IMG>, and the form element tags.

As a basic example of an event handler, here's a common use for JavaScript: creating a back button in a page that performs just like the browser's back button. You can easily accomplish this with an event handler, as in Listing 1.4.

Listing 1.4. A simple JavaScript event handler.
<INPUT TYPE="button" VALUE="Back!" onClick="history.go(-1); return true;">
This defines a button with an event handler. The event handler is defined as an attribute of the <INPUT> tag. The attribute name is the event name-in this case, onClick. This is an event that occurs when the user clicks the mouse on an object.

In this example, a button is used to send the user back to the previous page. You could also use this technique with an image, or a simple link to the word "back!".
Note
Because an event handler is inserted between double quotation marks, be sure to use single quotation marks to delimit any strings within the event handler.

## Viewing Your Script's Output
The main tool you'll use to view the script's output is a Web browser. Currently, you should use Netscape to view the output, but other browsers may support JavaScript in the future. There's nothing special you need to do to view a script's output-just load the Web page that contains the script. You can even test JavaScript on your local computer, without uploading anything to the Web server.

## Questions:

### Q1. Name an element which doesn't have a closing tag.
### Q2. What does HTML stand for?
### Q3. What section of a web page contains the author of the document, copyright information, links to the terms of the use, contact information, etc.
### Q4. Describe the purposes of the `<nav>` element.
### Q5. Describe the purposes of the `<section>` element.