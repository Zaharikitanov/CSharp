<a href="../README.md">Back to Appendix</a>

<a href="Data_structures.md">Back to Data Structures</a>

## Array 

An array is a sequence of individual data elements accessible through a single variable name. You use a zero-based numeric index to access each element of an array. As you'll see, arrays allow us to collect together similar data that shares a common purpose or characteristics in a single data structure for easier processing.

### Declaring arrays
An array is a special type of variable that can hold multiple values of the same data type. The declaration syntax is slightly different because you have to specify both the data type and the size of the array.

```
string[] fraudulentOrderIDs = new string[3];
```

The ```new``` operator creates a new instance of an array in the computer's memory that can hold three string values.<br>
Notice that the first set of square brackets ```[]``` merely tells the compiler that the variable named ```fraudulentOrderIDs``` will be an array, but the second set of square brackets ```[3]``` contains the number of elements that the array will hold.

### Assigning Values to Elements of an Array

At this point, we've declared an array of strings, but each element of the array is empty. To access an element of an array, you use a numeric zero-based index inside of square brackets.

You assign a value using the ```=``` assignment value as if it were a regular variable.

```
string[] fraudulentOrderIDs = new string[3];

fraudulentOrderIDs[0] = "A123";
fraudulentOrderIDs[1] = "B456";
fraudulentOrderIDs[2] = "C789";
```

### Getting Values of Elements in an Array

```
string[] fraudulentOrderIDs = new string[3];

fraudulentOrderIDs[0] = "A123";
fraudulentOrderIDs[1] = "B456";
fraudulentOrderIDs[2] = "C789";

Console.WriteLine($"First: {fraudulentOrderIDs[0]}");
Console.WriteLine($"Second: {fraudulentOrderIDs[1]}");
Console.WriteLine($"Third: {fraudulentOrderIDs[2]}");

Output:
First: A123
Second: B456
Third: C789
```

### Reassign the value of an array

```
string[] fraudulentOrderIDs = new string[3];

fraudulentOrderIDs[0] = "A123";
fraudulentOrderIDs[1] = "B456";
fraudulentOrderIDs[2] = "C789";

Console.WriteLine($"First: {fraudulentOrderIDs[0]}");
Console.WriteLine($"Second: {fraudulentOrderIDs[1]}");
Console.WriteLine($"Third: {fraudulentOrderIDs[2]}");

fraudulentOrderIDs[0] = "F000";

Console.WriteLine($"Reassign First: {fraudulentOrderIDs[0]}");

Output:
First: A123
Second: B456
Third: C789
Reassign First: F000
```

### Initializing an Array

```
string[] fraudulentOrderIDs = { "A123", "B456", "C789" };
```

### Getting the Size of an Array

Depending on how the array is created, you may not know in advance how many elements an array contains. To determine the size of an array, you can use the ```Length``` property.

```
string[] fraudulentOrderIDs = { "A123", "B456", "C789" };
Console.WriteLine($"There are {fraudulentOrderIDs.Length} fraudulent orders to process.");

Output:
There are 3 fraudulent orders to process.
```




