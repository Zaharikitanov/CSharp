<a href="README.md">Back to Appendix</a><br>
<a href="Numbers.md">Back to Numbers</a>

## Addition, subtraction, multiplication, and division with integers.
- ```+``` is the addition operator
- ```-``` is the subtraction operator
- ```*``` is the multiplication operator
- ```/``` is the division operator

```
int sum = 7 + 5;
int difference = 7 - 5;
int product = 7 * 5;
int quotient = 7 / 5;

Console.WriteLine("Sum: " + sum);
Console.WriteLine("Difference: " + difference);
Console.WriteLine("Product: " + product);
Console.WriteLine("Quotient: " + quotient);

Output: 
Sum: 12 
Difference: 2
Product: 35
Quotient: 1
```

However, the resulting quotient of our division example may not be what you may have expected. The values after the decimal are truncated from ```quotient``` since it is defined as an ```int```, and ```int``` cannot contain values after the decimal.

## Division using literal decimal data.

To see division working properly, we need to use a data type that supports fractional digits after the decimal point like ```decimal```.

```
decimal decimalQuotient = 7.0m / 5;
Console.WriteLine("Decimal quotient: " + decimalQuotient);

Output: Decimal quotient: 1.4
```

In order for this to work, the quotient (left of the assignment operator) must be of type ```decimal``` <b>and</b> either the dividend or divisor must be of type ```decimal``` (or both).

```
decimal decimalQuotient = 7 / 5.0m;
decimal decimalQuotient = 7.0m / 5.0m;
```

What if you are not working with literal values? In other words, what if you need to divide two variables of type ```int``` but do not want the result truncated? In that case, you must perform a data type cast from ```int``` to ```decimal```. Casting is one type of data conversion that instructs the compiler to temporarily treat a value as if it were a different data type.

To cast ```int``` to ```decimal```, you add the cast operator before the value. You use the name of the data type surrounded by parenthesis in front of the value to cast it. In this case, we would add ```(decimal)``` before the variables first and second.

```
int first = 7;
int second = 5;
decimal quotient = (decimal)first / (decimal)second;
Console.WriteLine(quotient);

Output: 1.4
```

## Determine the remainder after int division

The remainder operator ```%``` tells you the remainder of ```int``` division. What you really learn from this is whether one number is divisible by another. 

```
Console.WriteLine("Modulus of 200 / 5 : " + (200 % 5));
Console.WriteLine("Modulus of 7 / 5 : " + (7 % 5));

Output:
Modulus of 200 / 5 : 0
Modulus of 7 / 5 : 2
```

## Order of Operations

1. Parentheses (whatever is inside the parenthesis is performed first)
2. Exponents (While there's no exponent operator in C#, you can use the ```System.Math.Pow()``` method)
3. Multiplication and Division (from left to right)
4. Addition and Subtraction (from left to right)

```
int value1 = 3 + 4 * 5;
int value2 = (3 + 4) * 5;
Console.WriteLine(value1);
Console.WriteLine(value2);

Output:
23
35
```
