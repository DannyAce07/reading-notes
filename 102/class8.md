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

Focus only on Comparison operators and Assignment operators.
