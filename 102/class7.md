# Programming with JavaScript

## Control Flow
> The order in which the computer executes statements in a script

Code is run in order from the first line in the file to the last line unless the computer runs across the frequent structures that change the control flow such as contiginals and loops. For Exampl, a script used to validate user data from a webpage form. The script submits validated data, but if the user leaves a required field empty, the script prompts them to fill it in. The script uses a conditional strucure or if...else, so that different code executes depending on whether the form is complete or not:

        if (isEmpty(field)) {
          promtUser();
          } else {
             submitForm();
          }

A typical script in JavaScript or PHP includes many control structures, including conditionals, loops, and functions. Parts of a script may also include a loop, which iterates when the user clicks the **Submit** button for the form. The fuction could also include a loop which iterates through all fields in the form, checking each one in turn. Looking back at the code in the `if` and `else` sections, the lines `promptUser` and `submitForm` could also be calls to other functions in the script. Control flow means that when you read a script, you must not only read from start to finish but also look at program structures and how they affect order of execution.

## JavaScript Function Syntax

Javascript functions are defined by the `function` keyword, followed by a **name** followed by parenthesis **()**.

Functions can contain letters, digits, underscores, and dollar signs (same rules as variables).

the parenthesis cmay include parameter names separated by commas: 
**(parameter1, parameter2,..)**

Code to be executed by the function is placed inside curly brackets: **{}**

        function name(parameter1, parameter2, parameter3) {
        //code to be executed
        }
        
**Parameters** are listed inside the parenthesis in the function definition.

**Arguments** are the values recieved by the function when it is invoked.

Inside the function, the arguments (the parameters) behave as local variables.

## Function Invocation

The code inside the function will execute when something calls the function:
* when an event occurs (a user clicks a button)
* when it is called from  JavaScript code
* Automatically (self invoked)

## Function Return

When JavaScript reaches a `return` statement, the function will stop executing.

If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking Statement.

Functions often compute a **return value**. The value "returned" is returned back to the "caller":

> #### Example
> Calculate the product of two numbers, and return the result:
>>
>>         let x = myFunction(4, 3); //function is called, return value end up in x
>>
>>        function myFunction(a, b) {
>>         return a * b;           // Function retuns the product of a and b
>>           }
> 
>The result in x will be:
>>       12

## Why Functions?

You can reuse code: Define the code once, and use it many times.

You can use the same code many times with different arguments, to produce differet results. 

> #### Example
> Convert Farenheit to Celsius:
>> function to Celsius(farenheit) {
>> 
>> return (5/9) * (farenheit-32);
>> 
>> }
>> 
>> document.getElementbyId("demo").innerHTML = toCelsius(77);

## The () Operator Invokes the Function

Using the example above, `toCelsius` refers to the function object, and `toCelsius()` refers to the function result.

Accessing a function without () will return the function object instead of the function result.

> #### Example
> function to Celsius(farenheit) {
> 
> return (5/9) * (farenheit-32);
> 
> }
> document.getElementbyId("demo").innerHTML = toCelsius;

## Functions Used as Variable Values

Functions can be used the same way as you use variables, in all types of formulas, assignments, and calculations.

> #### Example
> Instead of using a variable to store the return value of a function:
>> let x = toCelsius(77);
>> 
>> let text = "The temperature is " + x + " Celsius";
>>
> You can use the function directly, as a variable:
>> let text = "The temperature is " + toCelsius(77) + " Celsius";

## Local Variables

Variables declared within a JavaScript Function, become **LOCAL** to the function.

Local variables can only be accessed from within the function.

> #### Example
>> // code here can NOT use carName
>> 
>> function myFunction() {
>> 
>>      let carName = "Volvo";
>>      
>>      // code here CAN use carName
>>      
>> }
>> 
>> // code here can NOT use carName

Sincle local variables are only reconized inside their functions, variables with the same name can be used in different functions.

Local variables are created when a function start, and deleted when the function is completed
