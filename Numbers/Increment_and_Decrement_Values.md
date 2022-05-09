<a href="README.md">Back to Appendix</a>

<a href="Numbers.md">Back to Numbers</a>

## Increment and Decrement Values

Operators like ```+=```, ```-=```, ```*=```, ```++```, and ```--``` are known as compound assignment operators because they compound some operation in addition to assigning the result to the variable. The ```+=``` operator is specifically termed the addition assignment operator.

```
int value = 1;

value = value + 1;
Console.WriteLine("First increment: " + value);

value += 1;
Console.WriteLine("Second increment: " + value);

value++;
Console.WriteLine("Third increment: " + value);

value = value - 1;
Console.WriteLine("First decrement: " + value);

value -= 1;
Console.WriteLine("Second decrement: " + value);

value--;
Console.WriteLine("Third decrement: " + value);

Output: 
First increment: 2
Second increment: 3
Third increment: 4
First decrement: 3
Second decrement: 2
Third decrement: 1
```


