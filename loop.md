# Java script operators and loops
![image](https://webbynat.files.wordpress.com/2016/04/javascript.gif)

## Javascript operators we mentioned before

1. Arithmetic Operators
2. Comparison Operators
3. Logical Operators
4. Assignment Operators

## 5. Bitwise operator

Bitwise operators treat its operands as a set of 32-bit binary digits (zeros and ones) and perform actions. However, the result is shown as a decimal value.

![image](https://www.devopsschool.com/blog/wp-content/uploads/2020/07/JavaScript-Bitwise-Operators.png)

## 6. String operator

In JavaScript, you can also use the + operator to concatenate (join) two or more strings.
Example 4: String operators in JavaScript

    // concatenation operator
    console.log('hello' + 'world');
    let a = 'JavaScript';
    a += ' tutorial';  // a = a + ' tutorial';
    console.log(a);
    Output
    helloworld

## 7. Ternary Operator

JavaScript includes special operator called ternary operator :? that assigns a value to a variable based on some condition. This is like short form of if-else condition.
Syntax:

    <condition> ? <value1> : <value2>;

Ternary operator starts with conditional expression followed by ? operator. Second part ( after ? and before : operator) will be executed if condition turns out to be true. If condition becomes false then third part (after :) will be executed.
Example: Ternary operator

    var a = 10, b = 5;
    var c = a > b? a : b; // value of c would be 10
    var d = a > b? b : a; // value of d would be 5

## 8. Other JavaScript Operators
Here's a list of other operators available in JavaScript. 

Operator|	Description|	Example
--------|------------|---------
,|	evaluates multiple operands and returns the value of the last operand.|	let a = (1, 3 , 4); // 4
?:|	returns value based on the condition|	(5 > 3) ? 'success' : 'error'; // "success"
delete|	deletes an object's property, or an element of an array	|delete x
typeof	|returns a string indicating the data type	|typeof 3; // "number"
void	|discards the expression's return value	|void(x)
in|	returns true if the specified property is in the object|	prop in object
instanceof|	returns true if the specified object is of of the specified object |type	object instanceof object_type

## JavaScript for & while loop

### 1. JavaScript for loop

For example, if you want to show a message 100 times, then you can use a loop. It's just a simple example; you can achieve much more with loops.

The syntax of the for loop is:

    for (initialExpression; condition; updateExpression) {
    // for loop body
    }

Here,

1. The initialExpression initializes and/or declares variables and executes only once.  
2. The condition is evaluated.  
3. If the condition is false, the for loop is terminated.  
4. f the condition is true, the block of code inside of the for loop is executed.  
5. The updateExpression updates the value of initialExpression when the condition is true.  
6. The condition is evaluated again.This process continues until the condition is false.  

![image](https://cdn.programiz.com/sites/tutorial2program/files/javascript-for-loop.png)

#### Example : Display a Text Five Times

    // program to display text 10 times
    const n = 5;

    // looping from i = 1 to 5
    for (let i = 1; i <= n; i++) {
    console.log(`I love JavaScript.`);
    }

### 2. JavaScript while Loop

The syntax of the while loop is:

    while (condition) {
    // body of loop
    }

Here,

1. A while loop evaluates the condition inside the parenthesis ().
2. If the condition evaluates to true, the code inside the while loop is executed.
3. The condition is evaluated again.
4. This process continues until the condition is false.
5. When the condition evaluates to false, the loop stops.

![image](https://cdn.programiz.com/sites/tutorial2program/files/javascript-while-loop.png)

#### Example : Display Numbers from 1 to 5

    // program to display numbers from 1 to 5
    // initialize the variable
    let i = 1, n = 5;

    // while loop from i = 1 to 5
    while (i <= n) {
    console.log(i);
    i += 1;
    }