<a href="../README.md">Back to Appendix</a>

## Stateful versus stateless methods
In computing, state describes the condition of the execution environment at a specific moment in time. As your code executes line by line, values are stored in variables. At any moment during execution, the current state of the application is the collection of all values stored in memory.

Some methods don't rely on the current state of the application to work properly. In other words, <b>stateless methods</b> are implemented so that they can work without referencing or changing any values already stored in memory. Stateless methods are also known as <b>static methods</b>.

For example, the ```Console.WriteLine()``` method doesn't rely on any values stored in memory. It performs its function and finishes without impacting the state of the application in any way.

Other methods, however, must have access to the state of the application to work properly. In other words, <b>stateful methods</b> are built in such a way that they rely on values stored in memory by previous lines of code that have already executed. Or they modify the state of the application by updating values or storing new values in memory. They're also known as <b>instance methods</b>.

Stateful (instance) methods keep track of their state in fields, which are variables defined on the class. Each new instance of the class gets its own copy of those fields in which to store state.

A single class can support both stateful and stateless methods. However, when you need to call stateful methods, you must first create an instance of the class so that the method can access state.

 - To call methods of a class in the .NET Class Library, you use the format ```ClassName.MethodName()```, where the ```.``` symbol is the member access operator to access a method defined on the class, and the ```()``` symbols are the method invocation operators.
- When calling a stateless method, you don't need to create a new instance of its class first.
- When calling a stateful method, you need to create an instance of the class, and access the method on the object.
- Use the ```new``` operator to create a new instance of a class.
- An instance of a class is called an object.

## Return values
Some methods are designed to complete their function, and end "quietly". In other words, they don't return values when they finish. They are referred to as <b>void methods</b>.

Methods designed to return a value upon completion are typically the result of an operation. A return value is a primary way a method can communicate back to the code that calls the method.

A method can be designed to return any data type, even another class.

## Input parameters
Some methods are designed to accept no input parameters. These methods need no additional input to complete their task.

Other methods are designed to accept one or more input parameters. The input parameters might configure how the method performs its work. Or, the input parameters might be operated on directly.

When calling methods, separate each input parameter with a ```,``` symbol.<br>
Input parameters are defined using a data type.<br>
A <b>method signature</b> is the number of input parameters defined for each input parameter and the data type.

## Overloaded methods

An <b>overloaded method</b> is defined with multiple method signatures. Overloaded methods provide different ways to call the method or provide different types of data.
