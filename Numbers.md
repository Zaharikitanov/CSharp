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
