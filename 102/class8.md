# Operators and Loops

## Expressions and Operators

An *expression* is a valid unit of code that resolves to a value. There are two types of expressions: those that have side effects and those that purely elevate.

the expression `x = 7` is an example of one that has a side effect. This expression uses the `=` operator to assign the value of seven to the variable `x`. The expression itself elevates to `7`.

the expression `3 + 4` is an example of one that elevates. this expression uses the operator `+` to add `3` and `4` and produces a value of `7`. Hoever, the result will immediately be discarded unless its a part of a bigger construct such as `const = 3 + 4`

All complex expressions are joined by operators such as `=` and `+`.

## Assignment Operators

An Assignment Operator assigns a value to its left operand based on the value of its right operand. The Simplest assignment operand is equal (`=`), which assigns the value of its right operand to its left operand. that is, `x = f()` is an assignment expression that assigns the value of `f()` to `x`.

## Assigning to Properties

If an expression evaluates to an object, then the left-hand side of an assignment expressionmay make assignments to properties of that expression. For Example:

        const obj = {};
        
        obj.x = 3;
        console.log(obj.x); // Prints 3.
        console.log(obj); // Prints { x: 3}.
        
        cont key = "y";
        obj[key] = 5;
        console.log(obj[key]); //prints 5.
        console.log(obj); // prints { x: 3, y: 5 }
        
If an expression does not elevate an object, then assignments to properties of that extension do not assign:

        const val = 0;
        val.x = 3;
        
        console.log(val.x); // Prints undefined
        console.log(val); // Prints 0.
        
In strict mode the code above throws because one cannot assign properties to primitives.

It is an error to assign values to unmodifiable properties or to properties of an expression without properties (`null` or `undefined`)

## Decunstructing

Deconstructiong assignment syntax is a JavaScript expression that makes it possible to extract data from arrays or objects using a syntax that mirrors the construction of array and object literals.

        const foo = ['one', 'two', 'three'];

        // without destructuring
        const one   = foo[0];
        const two   = foo[1];
        const three = foo[2];

        // with destructuring
        const [one, two, three] = foo;
        
## Evaluation and Nesting

In general, assignments are used within a variable declaration.

        // Declares a variable x and initializes it to the result of f()
        // The result of the x = f() assignment expression is declared.
        let x = f();
        
        
        x = g(); // Reassigns the variable x to the result of g().
        
Assignment expressions like `x = f()` evaluate into a result value. Although this result value is usually not used, it can be used by another expression.

Chaining assignments or nesting assignments in another expression can result in surprising behavior. For this reason it is sometimes discouraged. Nevertheless it may occur.

By chaining or nesting an assignment expression, its result can itself be assigned to another variable. It can be logged, put inside an array literal or function call, and so on.

                                let x;
                                
                                const y = (x = f()); //Or equivalently: cont y = x = f();
                                console.log(y); // logs the return value of the assignment x = f().
                                
                                console.log(x = f()); // Logs the return value directly
                                
                                // An assignment expression can be nested in any place
                                // where expressions are generally allowed,
                                // such as array literals' elements or as function calls' arguments.
                                console.log([ 0, x = f(), 0 ]);
                                console.log(f(0, x f(), 0));
                                
## Comparison Operators

Comparison Operators compare their operands and return logical values based on whether the comparison is true.The operands can be numerical, strings, logical, or objects. Strings are compared based on standard lexicographical ordering, using Unicode values. In most cases if operands are not of the same type JavaScripts attempts to convert them to an appropriate type for comparison, usually resulting in comparing the operands numerically. The sole exceptions to type comparisons involve the `===` and `!==` operators, which perform strict equality and inequality comparisons. These operators do not attempt to convert the operands to compatible types before checking inequality.

## Loops

Loops offer a quick way to do something repeatedley. Think of a loop as a computerized version of the game where you tell someone to take X steps in one direction, then  Y steps in another. For example, the idea "go five steps to the east" could be expressed as such:

        for (let step = 0; step < 5; step++) {
        // Runs 5 times, with values of step 0 through 4.
        console.log('Walking east one step');
        }
        
There are many different kind of loops, all repeating an action  a number of times. There are various situations that are more easily served by one typre of loop over the others. The Statement for loops provided in JavaScript are:
* for
* do...while
* while
* labeled
* break
* continue
* for...in
* for...of

### For statement

`for` loops repeat themselves until a specified condition evaluates to false. The JS `for` loop is similar to the Java and C `for` loop.

When a `for` loop executes, the following occurs:

The initializing expression `initialExpression`, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.

The `conditionExpression` expression is evaluated. If the value of `conditionExpression` is true, the loop statements execute. Otherwise, the `for` loop terminates. (If the `conditionExpression` expression is omitted entirely, the condition is assumed to be true.)

The `statement` executes. To execute multiple statements, use a block statement (`{ }`) to group those statements.

If present, the update expression `incrementExpression` is executed.

Control returns to Step 2.
