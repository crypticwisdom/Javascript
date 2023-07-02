# Javascript
## This is repository is usd for learning basic Javascript language with html and css.

# About Javascript
- A dynamic, interpreted and weakly typed language.
- It runs on a host environment, which must also have a javascript engine to execute the Javascript codes, example of a host environment is the web browser, server side.
- It can't access a system's file system.
- It can't interact with a system's O.S.
- Node.js is javascript that runs alone as a tool and on any machine, anywhere. so it can be installed and ran like a language like (Python ...). With Node.js you can now interact with a system and can access a system file system. Client Side Javascript and Node.Js has the same syntax.

# Variable:
use 'let' to declare variables, use 'const' to declare constants.
e.g: let age = 90;
     let age; (unintialized variable).

# Data Types:
- Numbers: 0, 2, -3 (integers) and  233.233 (floating points).
- String: 'hi', "hi" or `hi`, these are all strings in JS.
- booleans: true / false]
- object: {key:'name', age:23}

- Arrays: [1, 2, 3, 4, 'wisdom', 2.3]
    * methods of an Array:
      - .push(): adds an element into an array.

# Template Literals:
E.g: correct way: `${variableName + 232}`.  use back-ticks for string interpolations in JS. 
       Wrong way: "${varableName + 323}", right way `${variableName}`.
    - Aside from substituting variables with string literals in a back-tick string, It is also used for writing long strings.


# Functions:
    Syntax: 
               function funcName(parameter1, parameter2){
                       ...      
               }
  - Functions can be written at any part in the scripts and can be invoked before the function definition or after the function definition the order doesn't matter.
  E.G:      
               add(1, 2); 
                function add(num1, num2){
                   return num1 + num2;
               }

- The order of function invokation doesn't matter because the browser first scans through our scripts and gets aware of the presence of these functions and then put them at the TOP level of the file, so that even though the function is called before it's definition, it can still be reachable.
- You need to write your program correctly by writting your function definition before calling the  function, it is a good practice but not required.


# Shadowing Variable
- Shadowing Variable means creating a variable in a local scope that  already exist in the global scope, which will then now co-exists but in different scopes.
      "It creates a new variable on a different scope, this variables does not overwrite or remove the global variable by the way, both variables co-exist."


# Data Type Conversion:
you can convert data from one data type to another using these Javascript built-in function:
parseInt(value); ==> To parse a value to integer OR +(stringNumberValue). e.g +"98"
    - the difference between +(stringValue) and parseInt(value) is, the parseInt converts a value to an integer (i.e to a number without a decimal) while, +(...) can take a striing value of float "656.656" and converts it to 656.656 still leaving the precisions.

parseFloat(value) ==> To parse a value to float data type.
data.toString() ==> To parse a value to string data type.


# Comments:
can be written in 2 ways. 
- Single line comment: //
- Multi-Line comment: /* long comment */
