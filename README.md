# javascript

**The modern mode**, "use strict"
To keep old version of code working "use strict" in the top.

## Variables
  Variable is name of data storage. There is 2 type of variables, "let" and "const".
  let - variable that can be changet
  const - this variable cannot be changet.
   
## Variable naming
1. First litter must be not a number(digit).
2. Not reserved name(reserved by programming language).
3. The name must contain only letters, digits, or the symbols $ and _.
4. The name should give a description of this variable
        
##  Data types
                                             
A variable in JS can contain any data.
There is a 7 different data types name:
1."number" - for number
2."boolean" - true/false
3."string" - for strings
4."symbol" - unique identifiers
5. "object" - complex data structure
6."undefined" - variable without any date or data with undefined value
7."null" - unknown value

when we type let someVariable = null, we clear value of this variable. So null is value with nothing.


There is also 2 form of typeof without any difference "typeof x and typeof(x)"

## Type Conversions
                                   
We can convert value type. Also JS have functions that automatically convert.

## Operators


An operand – is what operators are applied to. For instance, in the multiplication of 5 * 2 there are two operands: the left operand is 5 and the right operand is 2. Sometimes, people call these “arguments” instead of “operands”.

An operator is unary if it has a single operand. For example, the unary negation - reverses the sign of a number.
An operator is binary if it has two operands. 

    Remainder %
 The result of a % b is the remainder of the integer division of a by b.

   Exponentiation **
 For a natural number b, the result of a ** b is a multiplied by itself b times.

  Increment/decrement
 Increment ++ increases a variable by 1
 a++ = a+1;

 Decrement -- decreases a variable by 1
 a-- = a-1;

!!! Increment/decrement can only be applied to variables. Trying to use it on a value like 5++ will give an error. !!!

   Bitwise operators
    AND - ( & )
    OR - ( | )
    XOR  - ( ^ )
    NOT = ( ~ )
    LEFT SHIFT - ( << )
    RIGHT SHIFT - ( >> )
    ZERO-FILL RIGHT SHIFT - ( >>> )

   Comma 
   (rare to use)
 The comma operator allows us to evaluate several expressions, dividing them with a comma ,. Each of them is evaluated but only the result of the last one is returned.

## Comparisons
  Comparison type: '<, >, =, >=, <=, !=, ===, ==,'
  When we use 'if', condition was already boolean.
  for example:
  if (something) {
    ..
  }
  'something' - boolean.
## Boolean
true - yes(1) /correct
false - no(0) / wrong
We use comparing ofter for compare something to perform actions under a certain condition
Comparison operators return a boolean value.
Strings are compared letter-by-letter in the “dictionary” order.

## Interaction: alert, prompt, confirm
all this scripts paused script execution

alert

```(javascript)
 alert(message);
````

promt

Sshow a message and paused script until you press "OK"
 It returns the text or, if CANCEL or Esc is clicked, null.

```(javascript)
 result = prompt(title[, default]);
```
promt accepts two arguments, first will show message(before coma) and second will shows an input field.

confirm

```(javascript)
result = confirm(question);
```
show message with two option "OK" and "CANCLE", just for boolean.


##   Conditional operators: if, '?'

### The “if” statement

The if statement evaluates a condition and, if the condition’s result is true, executes a block of code.

#### Boolean conversion

The if (…) statement evaluates the expression in its parentheses and converts the result to a boolean.

### The “else” clause

The if statement may contain an optional “else” block. It executes when the condition is false.

### Several conditions: “else if”

We can do multiplicate time "else if" if its needed. Same as "else"


## Ternary operator ‘?’

same as "if, else" but with ternary operator its much simple and shorter.
 Example:
 ```(javascript)
let result = condition ? value1 : value2;
```
 Example:

```(javascript)
 let age = prompt('age?', 18);

 let message = (age < 3) ? 'Hi, baby!' :
  (age < 18) ? 'Hello!' :
  (age < 100) ? 'Greetings!' :
  'What an unusual age!';

 alert( message );
```

 with ternary operator "?" :

```(javascript)
 let age = prompt('age?', 18);

 let message = (age < 3) ? 'Hi, baby!' :
  (age < 18) ? 'Hello!' :
  (age < 100) ? 'Greetings!' :
  'What an unusual age!';

 alert( message );
```



## Logical operators

 There are three logical operators in JavaScript: 
 1.   || (OR) -  used for test if any conditions is true.
 2.   && (AND)
 3.   ! (NOT)


### || (OR)
Getting the first truthy value from a list of variables or expressions.

### && (AND)
&& (AND) finds the first falsy value
The AND && operator does the following:
   Evaluates operands from left to right.
   For each operand, converts it to a boolean. If the result isfalse, stops and returns the original value of that operand.
   If all operands have been evaluated (i.e. all were truthy),returns the last operand.

### Precedence of AND && is higher than OR ||
So the code a && b || c && d is essentially the same as if the && expressions were in parentheses: (a && b) || (c && d).


 Just like OR, the AND && operator can sometimes replace if.

```(javascript)
 let x = 1;

 (x > 0) && alert( 'Greater than zero!' );
```
The action in the right part of && would execute only if the evaluation reaches it. That is, only if (x > 0) is true.

transform to standart:
```(javascript)
let x = 1;

if (x > 0) {
  alert( 'Greater than zero!' );
}
```


## ! (NOT)

```
result = !value;
```
The operator accepts a single argument and does the following:

    Converts the operand to boolean type: true/false.
    Returns the inverse value.

A double NOT !! is sometimes used for converting a value to boolean type:
```
alert( !!"non-empty string" ); // true
alert( !!null ); // false
```
That is, the first NOT converts the value to boolean and returns the inverse, and the second NOT inverses it again. In the end, we have a plain value-to-boolean conversion.

The precedence of NOT ! is the highest of all logical operators, so it always executes first, before && or ||.

 ## Loops: while and for

 We have 3 type of loops:
1. while - when condition is checked before each iteration.
2. do..while - when condition is checked after each iteration.
3. for (;;) - when condition is checked before each iteration, additional settings available.


The “while” loop

  Example:
  ```(javaScript)
  while (condition) {
  // code
  // so-called "loop body"
}
```
While the condition is true, the code from the loop body is executed.
A single execution of the loop body is called an iteration.
Any expression or variable can be a loop condition, not just comparisons: the condition is evaluated and converted to a boolean by while.

For instance, a shorter way to write while (i != 0) is while (i):
```(javascript)
let i = 3;
while (i) { // when i becomes 0, the condition becomes falsy, and the loop stops
  alert( i );
  i--;
}
```

  The “do…while” loop

  “do…while” loop first will execute the body and then check the condition,and, while it’s truthy, execute it again and again 
   Example:
   ```(javascript)
   let i = 0;
do {
  alert( i );
  i++;
} while (i < 3);
   ```
   This form of syntax should only be used when you want the body of the loop to execute at least once regardless of the condition being truthy. Usually, the other form is preferred: while(…) {…}.
  

   The “for” loop

The for loop is the most commonly used loop.
Example:
```(javascript)
for (begin; condition; step) {
  // ... loop body ...
}
```
algoritm of this loop:
Run begin
1. (if condition → run body and run step)
2. (if condition → run body and run step)
3. (if condition → run body and run step)
→4. ...
Example:
```(javascript)
// for (let i = 0; i < 3; i++) alert(i)

// run begin
let i = 0
// if condition → run body and run step
if (i < 3) { alert(i); i++ }
// if condition → run body and run step
if (i < 3) { alert(i); i++ }
// if condition → run body and run step
if (i < 3) { alert(i); i++ }
// ...finish, because now i == 3
```

 Inline variable declaration
 Example:
 ```(javascript)
for (let i = 0; i < 3; i++) {
  alert(i); // 0, 1, 2
}
alert(i); // error, no such variable
 ```
 Here, the “counter” variable i is declared right in the loop. This is called an “inline” variable declaration. Such variables are visible only inside the loop.
  So there is 2 type of variable:
  1. Global - variable outside of any loops/function
  2. Local - variable in loops/function
 Local variable you can't use outside of his loops/function.
 Global you can use everywhere. 

Skipping parts
 We can skip any part of for.
 For example, we can omit begin if we don’t need to do anything at the loop start:
 ```(javascript)
let i = 0; // we have i already declared and assigned

for (; i < 3; i++) { // no need for "begin"
  alert( i ); // 0, 1, 2
}
 ```

 Skip step:
 ```(javascript)
let i = 0;

for (; i < 3;) {
  alert( i++ );
}
 ```
 This makes the loop identical to while (i < 3).
We can actually remove everything, creating an infinite loop:
```(javascript)
for (;;) {
  // repeats without limits
}
```
!! Semicolons ; must be present or you will have syntax error.

Breaking the loop
Normally, a loop exits when its condition becomes falsy.
But we can force the exit at any time using the special break directive.
 Example:
 ```(javascript)
 let sum = 0;

while (true) {

  let value = +prompt("Enter a number", '');

  if (!value) break; // (*)

  sum += value;

}
alert( 'Sum: ' + sum );
```
The break directive is activated at the line (*) if the user enters an empty line or cancels the input. It stops the loop immediately, passing control to the first line after the loop. Namely, alert.
The combination “infinite loop + break as needed” is great for           situations when a loop’s condition must be checked not in the beginning  or end of the loop, but in the middle or even in several places of its body.


 Continue to the next iteration
 The continue directive is a “lighter version” of break. It doesn’t stop the whole loop. Instead, it stops the current iteration and forces the loop to start a new one (if the condition allows).

We can use it if we’re done with the current iteration and would like to move on to the next one.

The loop below uses continue to output only odd values:
1st variant:
```(javascript)
for (let i = 0; i < 10; i++) {

  // if true, skip the remaining part of the body
  if (i % 2 == 0) continue;

  alert(i); // 1, then 3, 5, 7, 9
}
```
2nd variant:
```(javascript)
for (let i = 0; i < 10; i++) {

  if (i % 2) {
    alert( i );
  }
}
```
 There is no differnce beetwen first and second variant, but first variant easy(easy understand or better readability) then second, because second use "{}" brace and there cab be alot of this, so better use first varian for easy read.

!!! No break/continue to the right side of ‘?’
 Please note that syntax constructs that are not expressions cannot be used with the ternary operator ?. In particular, directives such as break/continue aren’t allowed there.
 Example:
 ```(javascript)
if (i > 5) {
  alert(i);
} else {
  continue;
}
 ```
 and if we use question mark "?" :
 ```(javascript)
(i > 5) ? alert(i) : continue; // continue isn't allowed here
 ```
 Code like this will have a syntax error:
 This is just another reason not to use the question mark operator ? instead of if.
 

Labels for break/continue
Sometimes we need to break out from multiple nested loops at once.
And for this manipulation we will use "Labels";
Example:
```(javscript)
labelName: for (...) {
  ...
}
```
Exanple in code:
```(javascript)
outer: for (let i = 0; i < 3; i++) {

  for (let j = 0; j < 3; j++) {

    let input = prompt(`Value at coords (${i},${j})`, '');

    // if an empty string or canceled, then break out of both loops
    if (!input) break outer; // (*)

    // do something with the value...
  }
}
alert('Done!');
```
So, break outer will breal geleral(global) loops from coomand inside of any loops.
Example:
```(javascript)
loop1: for (begin,condition,step) { //first loop
  for (begin,condotion,tep) {       // second loop in the first loop
body                             //body of loop
 if (!body) break loop1;
 do something with the value
  }
}
```
We also can have label into a separate lines:
```(javascipt)
loop1:
for (let i = 0; i < 3; i++) { ... }
```

To make an “infinite” loop, usually the while(true) construct is used. Such a loop, just like any other, can be stopped with the break directive.

If we don’t want to do anything in the current iteration and would like to forward to the next one, we can use the continue directive.



## **The "switch" statement**

A switch statement can replace multiple if checks. It gives a more descriptive way to compare a value with multiple variants.

Example :
```(javascript)
switch(x) {
  case 'value1':  // if (x === 'value1')
    ...
    [break]

  case 'value2':  // if (x === 'value2')
    ...
    [break]

  default:
    ...
    [break]
}
```
The value of x is checked for a strict equality to the value from the first case (that is, value1) then to the second (value2) and so on.
    If the equality is found, switch starts to execute the code starting from the corresponding case, until the nearest break (or until the end of switch).
    If no case is matched then the default code is executed (if it exists).
 
 If there is no break then the execution continues with the next case without any checks:
    ```(javascript)
     let a = 2 + 2;
     switch (a) {
      case 3:
       alert( 'Too small' );
      case 4:
       alert( 'Exactly!' );
      case 5:
      alert( 'Too big' );
     default:
      alert( "I don't know such values" );
      }
      ```
     
    So, in this example execution starts from 4(skip 3 because a=4 -> execution start from cas '4'), end we will see 3 results:

     ```(javascript)
     alert( 'Exactly!' );
     alert( 'Too big' );
     alert( "I don't know such values" );
     ```
    Any expression can be a switch/case argument:
     ```(javascript)
     let a = "1";
    let b = 0; 
    switch (+a) {
     case b + 1:
     alert("this runs, because +a is 1, exactly equals b+1");
     break;
    default:
     alert("this doesn't run");
     }
     ```
    Here +a gives 1, that’s compared with b + 1 in case, and the corresponding code is executed.



    Grouping of “case”
     We can group any cases if they hhave same execution
     Example:
      ```(javascript)
       let a = 2 + 2;
       switch (a) {
       case 4:
        alert('Right!');
        break;
       case 3:                    // (*) grouped two cases
       case 5:
        alert('Wrong!');
        alert("Why don't you take a math class?");
       break;
      default:
        alert('The result is strange. Really.');
        }
      ```
      So, if we run case 3 and or case 5 we will have same execution.


          Type matters:
         The values must be of the same type to match. If not - then execute 'default'.


# Functions

If we need use action many time in many places - we use Functions.

To create a function we can use a function declaration:

```(Javascript)
function nameFunction(parameters) {
  the function body
}
```
### Local variables
Local variable - variable that created in function and this variable can be used only in this function, outside this function this variable is not working.

### Outer variables
Outer variables - variable created outside of function and can be used at any function(global variable).
Global variables are visible from any function (unless shadowed by locals).
 Usually, a function declares all variables specific to its task. Global variables only store project-level data, and it’s important that these variables are accessible from anywhere. Modern code has few or no globals. Most variables reside in their functions.

 ### Parameters
  We can pass arbitrary data to functions using parameters (also called function arguments) .
  Example:
  ```(javascript)
function showMessage(from, text) { // arguments: from, text
  alert(from + ': ' + text);
}

showMessage('Ann', 'Hello!'); // Ann: Hello! (*)
showMessage('Ann', "What's up?"); // Ann: What's up? (**)
  ```
  Parameters - it's like variable, but temporary.
  ### When the function is called in lines (*) and (**), the given values are copied to local variables from and text. Then the function uses them.


  Here’s one more example: we have a variable from and pass it to the function. Please note: the function changes from, but the change is not seen outside, because a function always gets a copy of the value:
```(javascript)
function showMessage(from, text) {

  from = '*' + from + '*'; // make "from" look nicer

  alert( from + ': ' + text );
}

let from = "Ann";

showMessage(from, "Hello"); // *Ann*: Hello

// the value of "from" is the same, the function modified a local copy
alert( from ); // Ann
```
This example show how works global and local parameters(variable) in function


### Returning a value
 A function can return a value back into the calling code as the result:
 ```(javascript)
function sum(a, b) {
  return a + b;
}

let result = sum(1, 2);
alert( result ); // 3
 ```

 Return can be placed in any place, when execution reaches it, the function stops and the value is returned to the calling code.
 There may be many occerences of return in a single function. 
 Example:
```(javascript)
function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    return confirm('Do you have permission from your parents?');
  }
}

let age = prompt('How old are you?', 18);

if ( checkAge(age) ) {
  alert( 'Access granted' );
} else {
  alert( 'Access denied' );
}
 ```

 It is possible to use return without a value. That causes the function to exit immediately.

For example:
```(javascript)
function showMovie(age) {
  if ( !checkAge(age) ) {
    return;
  }

  alert( "Showing you the movie" ); // (*)
  // ...
}
```
In the code above, if checkAge(age) returns false, then showMovie won’t proceed to the alert.

### A function with an empty return or without it returns undefined
 If a function does not return a value, it is the same as if it returns undefined:
 ```(javascript)
function doNothing() { /* empty */ }

alert( doNothing() === undefined ); // true
 ```

 An empty return is also the same as return undefined:

```(javascript)
function doNothing() {
  return;
}

alert( doNothing() === undefined ); // true
```


## Function expressions and arrows
The syntax of Function Declaration:

function sayHi() {
  alert( "Hello" );
}

There is another syntax for creating a function that is called a Function Expression.

It looks like this:

let sayHi = function() {
  alert( "Hello" );
};

Copy functions to another variable:

```(javascript)
function sayHi() {   // (1) create
  alert( "Hello" );
}

let func = sayHi;    // (2) copy

func(); // Hello     // (3) run the copy (it works)!
sayHi(); // Hello    //     this still works too (why wouldn't it)
```

What happens:

 The Function Declaration (1) creates the function and puts it into the variable named sayHi.

 Line (2) copies it into the variable func.

 Please note again: there are no parentheses after sayHi. If there were, then func = sayHi() would write the result of the call sayHi() into func, not the function sayHi itself.

 Now the function can be called as both sayHi() and func().

Note:
By syntax  Function Expression have a semicolon `;` but Function Declaration does not.

### Callback functions
We’ll write a function ask(question, yes, no) with three parameters:

question
    Text of the question
yes
    Function to run if the answer is “Yes”
no
    Function to run if the answer is “No”

The function should ask the question and, depending on the user’s answer, call yes() or no():

```(javascript)
function ask(question, yes, no) {
  if (confirm(question)) yes()
  else no();
}

function showOk() {
  alert( "You agreed." );
}

function showCancel() {
  alert( "You canceled the execution." );
}

// usage: functions showOk, showCancel are passed as arguments to ask
ask("Do you agree?", showOk, showCancel);
```
###The arguments of ask are called callback functions or just callbacks.
We can use Function Expressions to write the same function much shorter:
```(javascript)
function ask(question, yes, no) {
  if (confirm(question)) yes()
  else no();
}

ask(
  "Do you agree?",
  function() { alert("You agreed."); },
  function() { alert("You canceled the execution."); }
);```



###A function is a value representing an “action”
Regular values like strings or numbers represent the data.

A function can be perceived as an action.

We can pass it between variables and run when we want.

##Function Expression vs Function Declaration

Function Declaration: a function, declared as a separate statement, in the main code flow.

 
Function Declaration:
```(javascript)
function sum(a, b) {
  return a + b;
}
```

Function Expression: a function, created inside an expression or inside another syntax construct. Here, the function is created at the right side of the “assignment expression” =:

 Function Expression:
```(javascript)
let sum = function(a, b) {
  return a + b;
};
```


A Function Expression is created when the execution reaches it and is usable from then on.

Once the execution flow passes to the right side of the assignment let sum = function… – here we go, the function is created and can be used (assigned, called, etc. ) from now on.

Function Declarations are different.

A Function Declaration is usable in the whole script/code block.

In other words, when JavaScript prepares to run the script or a code block, it first looks for Function Declarations in it and creates the functions. We can think of it as an “initialization stage”.

And after all of the Function Declarations are processed, the execution goes on.

As a result, a function declared as a Function Declaration can be called earlier than it is defined.

For example, this works:
```(javascript)
sayHi("John"); // Hello, John

function sayHi(name) {
  alert( `Hello, ${name}` );
}
```

The Function Declaration sayHi is created when JavaScript is preparing to start the script and is visible everywhere in it.

…If it was a Function Expression, then it wouldn’t work:

```(javascript)
sayHi("John"); // error!

let sayHi = function(name) {  // (*) no magic any more
  alert( `Hello, ${name}` );
};
```

Function Expressions are created when the execution reaches them. That would happen only in the line (*). Too late.



###When should you choose Function Declaration versus Function Expression?
In general we use Declaration fucntion because it much easy read and we need declare a function. 

### Arrow functions

```(javascript)
let func = (arg1, arg2, ...argN) => expression
```
This creates a function func that has arguments arg1..argN, evaluates the expression on the right side with their use and returns its result.

In other words, it’s roughly the same as:

```(javascript)
let func = function(arg1, arg2, ...argN) {
  return expression;
};
```

```(javascript)
let sum = (a, b) => a + b;

/* The arrow function is a shorter form of:

let sum = function(a, b) {
  return a + b;
};
*/

alert( sum(1, 2) ); // 3
```
If we have only one argument, then parentheses can be omitted, making that even shorter:
```(javascript)
// same as
// let double = function(n) { return n * 2 }
let double = n => n * 2;

alert( double(3) ); // 6
```
If there are no arguments, parentheses should be empty (but they should be present):
```(javascript)
let sayHi = () => alert("Hello!");

sayHi();
```
example arrow function:
```(javascript)
let age = prompt("What is your age?", 18);

let welcome = (age < 18) ?
  () => alert('Hello') :
  () => alert("Greetings!");

welcome(); // ok now
```

### Multiline arrow functions
In multiline arrow function we need use curly braces:
```(javascript)
let sum = (a, b) => {  // the curly brace opens a multiline function
  let result = a + b;
  return result; // if we use curly braces, use return to get results
};

alert( sum(1, 2) ); // 3
```





# Objects

 For creating objects we use {..}, example of empty Objects:

 ```(javascript)
let user = new Object(); // "object constructor" syntax
let user = {};  // "object literal" syntax
```
That declaration is called an object literal.

## Literals and properties

We can immediately put some properties into {...} as “key: value” pairs:

```(javascript)
let user = {     // an object
  name: "John",  // by key "name" store value "John"
  age: 30        // by key "age" store value 30
};
```
For get accesible to value of objects we use dot notation:
```(javascript)
// get fields of the object:
alert( user.name ); // John
alert( user.age ); // 30
```

## Square brackets
For multiword properties, the dot access doesn’t work:

```(javascript)
// this would give a syntax error
user.likes birds = true
```
That’s because the dot requires the key to be a valid variable identifier. That is: no spaces and other limitations.

Square brackets also provide a way to obtain the property name as the result of any expression – as opposed to a literal string – like from a variable as follows:

```(javascript)
let key = "likes birds";

// same as user["likes birds"] = true;
user[key] = true;
```
Example of square brackets:
```(javascript)
let user = {
  name: "John",
  age: 30
};

let key = prompt("What do you want to know about the user?", "name");

// access by variable
alert( user[key] ); // John (if enter "name")
```