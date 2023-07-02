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
- booleans: true / false
- object: {key:'name', age:23};
     * Operation of an Object:
          - object.key: unlike Python (object['key']). Here you can access an object with the '.' dot notation. console.log(object.key) => 'name'

- Arrays: [1, 2, 3, 4, 'wisdom', 2.3]
    * 'Methods' of an Array:
      - .push(): adds an element into an array.
      - array[index]: to access the elements of that array.
      - an array is an object, a special type of object, becase when we check the runtime type with typeof [], it yields 'object' as the type.

- null:
     * it's not the default value of an uninitialized variable.
     * I can manually assign the 'null' data type manaually to variable in other to clear or reset that variable.
     * null is an object, a special type of object, becase when we check the runtime type with typeof null, it yields 'object' as the type.
     
- undefined: 
   * This is the default value of uninitialized variable.
   * You shouldn't assign undefine as a value to a variable manually. Technically, it will work but, it's not recommended.
   * When you access an element of an array that doesn't exists, the value will be undefined.

# NaN (Not a Number):
   - It yields a new NaN and it's the result of invalid calculations e.g 3 * "hello".
   - It's of type number and can be therefore used in calculations. But will yield a new NaN.
   - it's like an error you get when calculating between numbers and string.
   example: 
        - 3 * "hi" => NaN
        - 45 * NaN => NaN

# Template Literals:
E.g: correct way: `${variableName + 232}`.  use back-ticks for string interpolations in JS. 
       Wrong way: "${varableName + 323}", right way `${variableName}`.
    - Aside from substituting variables with string literals in a back-tick string, It is also used for writing long strings.

# typeof:
This is used to evaluate the type of a value at runtime.
typeof "wisdom is a boy"; => string.

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
- parseInt(value); ==> To parse a value to integer OR +(stringNumberValue). e.g +"98"
    - the difference between +(stringValue) and parseInt(value) is, the parseInt converts a value to an integer (i.e to a number without a decimal) while, +(...) can take a striing value of float "656.656" and converts it to 656.656 still leaving the precisions.
- parseFloat(value) ==> To parse a value to float data type.
- data.toString() ==> To parse a value to string data type.


# Comments:
can be written in 2 ways. 
- Single line comment: //
- Multi-Line comment: /* long comment */

# Import Scripts Correctly
inspect your page on the browser -> go to 'performance' tab. his is a grest tool for understandin how to scripts are loading and executing.
record, reload your page and pause.

## What happens when:
  - we import JS script at the html head tag without any attribute (defer / async): when this page is loaded on the browser, the browser parses the first html tags and pause parsing html to download and execute the scripts upon encountering them, after downloading and executing the scripts it then continues parsing html code. This is not right as it causes error if the scripts were supposed to interact with the html tags.

  - we import JS script at the html head tag with the 'defer' attribute: the attribute will tell the browser that it should download the scripts right away but that it should not block parsing of the html codes, so tht instead it should continue parsing the html codes, it then executes the scripts after every html has been parsed completely. in summary, the attribute downloads the scripts early but it doesn't execute the script immediately after download instead it guarantees us that it only execute the scripts once they were downloaded and once parsing the html finishes. The order of execution is guaranteed.

  - we import JS script at the html head tag with the 'async' attribute: if we want the scripts to download and execute early use the 'async' eyword, it tells the browser to start loading the script as early as possible but then, the broswer is not bloced but instead continues to parse the html, but the difference with defer is that with async the scripts gets executed onc the scripts are downloaded so, it does not wait for all the html to be parsed, instead it executes as early as possible. the order of the scripts execution is not guaranteed, the last script could first execute before the first script once it is loaded.

  - note that 'defer' and 'async' are only available if you have external scripts. you can't used those html attributes on an inline script.

  - inline scripts should be written at the end of the body section.

  - you can't combine the inline and external scripts, the external script will run and therefore the inline script will be ignored.