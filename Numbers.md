<a href="README.md">Back to Appendix</a>

## Addition, subtraction, multiplication, and division with integers.
- ```+``` is the addition operator
- ```-``` is the subtraction operator
- ```*``` is the multiplication operator
- ```/``` is the division operator

```int sum = 7 + 5;```<br>
```int difference = 7 - 5;```<br>
```int product = 7 * 5;```<br>
```int quotient = 7 / 5;```<br>

```Console.WriteLine("Sum: " + sum);```<br>
```Console.WriteLine("Difference: " + difference);```<br>
```Console.WriteLine("Product: " + product);```<br>
```Console.WriteLine("Quotient: " + quotient);```<br>

Result: <br>
Sum: 12 <br>
Difference: 2<br>
Product: 35<br>
Quotient: 1<br>

However, the resulting quotient of our division example may not be what you may have expected. The values after the decimal are truncated from ```quotient``` since it is defined as an ```int```, and ```int``` cannot contain values after the decimal.

## Division using literal decimal data.

To see division working properly, we need to use a data type that supports fractional digits after the decimal point like ```decimal```.

```decimal decimalQuotient = 7.0m / 5;```<br>
```Console.WriteLine("Decimal quotient: " + decimalQuotient);```<br>

Result: Decimal quotient: 1.4

In order for this to work, the quotient (left of the assignment operator) must be of type ```decimal``` <b>and</b> either the dividend or divisor must be of type ```decimal``` (or both).

```decimal decimalQuotient = 7 / 5.0m;```<br>
```decimal decimalQuotient = 7.0m / 5.0m;```<br>

What if you are not working with literal values? In other words, what if you need to divide two variables of type ```int``` but do not want the result truncated? In that case, you must perform a data type cast from ```int``` to ```decimal```. Casting is one type of data conversion that instructs the compiler to temporarily treat a value as if it were a different data type.

To cast ```int``` to ```decimal```, you add the cast operator before the value. You use the name of the data type surrounded by parenthesis in front of the value to cast it. In this case, we would add ```(decimal)``` before the variables first and second.

```int first = 7;```<br>
```int second = 5;```<br>
```decimal quotient = (decimal)first / (decimal)second;```<br>
```Console.WriteLine(quotient);```<br>

Result: 1.4

## Determine the remainder after int division

The remainder operator ```%``` tells you the remainder of ```int``` division. What you really learn from this is whether one number is divisible by another. 

```Console.WriteLine("Modulus of 200 / 5 : " + (200 % 5));```<br>
```Console.WriteLine("Modulus of 7 / 5 : " + (7 % 5));```<br>

Result:<br>
Modulus of 200 / 5 : 0<br>
Modulus of 7 / 5 : 2






