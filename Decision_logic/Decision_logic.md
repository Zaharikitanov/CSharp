<a href="../README.md">Back to Appendix</a>

## The if statement

The ```if``` statement relies on a Boolean expression that is enclosed in a set of parentheses. If the expression is true, the code following the if statement will be executed. If not, the .NET runtime will ignore the code and won't execute it.

The double pipe characters ```||``` are the <b>logical OR</b> operator, which basically says "either the expression to my left OR the expression to my right must be true in order for the entire Boolean expression to be true". If both boolean expressions are false, then entire boolean expression is false. We use two logical OR operators so that we can extend the evaluation to a third boolean expression.

```
Random dice = new Random();

int roll1 = dice.Next(1, 7);
int roll2 = dice.Next(1, 7);
int roll3 = dice.Next(1, 7);

if ((roll1 == roll2) || (roll2 == roll3) || (roll1 == roll3))
{
    Console.WriteLine("You rolled doubles! +2 bonus to total!");
}
```

The double ampersand characters ```&&``` are the <b>logical AND</b> operator, which basically says "only if both expressions are true, then the entire expression is true". In this case, if roll1 is equal to roll2, and roll2 is equal to roll3, then by deduction, roll1 must be equal to roll3, and the user rolled triples.

```
Random dice = new Random();

int roll1 = dice.Next(1, 7);
int roll2 = dice.Next(1, 7);
int roll3 = dice.Next(1, 7);
if ((roll1 == roll2) && (roll2 == roll3)) 
{
    Console.WriteLine("You rolled triples! +6 bonus to total!");
}
```


