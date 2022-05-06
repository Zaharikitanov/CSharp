<a href="README.md">Back to Appendix</a>

## Character Escape Sequences and Verbatim Strings
Here's the most important items to remember about formatting literal strings:

- Use character escape sequences when you need to insert a special character into a literal string, like a tab ```\t```, new line ```\n```, or a double quotation mark ```\"```.
- Use an escape character for the backslash ```\\``` when you need to use a backslash in all other scenarios.
- Use the ```@``` directive to create a verbatim string literal that keeps all whitespace formatting and backslash characters in a string.
- Use the ```\u``` plus a four-character code to represent Unicode characters (UTF-16) in a string.
- Unicode characters may not print out correctly depending on the application.

## String Interpolation
String interpolation combines multiple values into a single literal string by using a "template" and one or more interpolation expressions. An interpolation expression is a variable surrounded by an opening and closing curly brace symbol ```{ }```. The literal string becomes a template when it's prefixed by the ```$``` character. <br>
```string message = $"{greeting} {firstName}!";```

### Combine verbatim literals and string interpolation
```string projectName = "First-Project";``` <br>
```Console.WriteLine($@"C:\Output\{projectName}\Data");```

Result: C:\Output\First-Project\Data

