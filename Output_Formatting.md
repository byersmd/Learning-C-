[Microsoft Reference](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/formatting-numeric-results-table)
---
The brackets { } are placeholders for data to be inserted.
```C#
Console.Writeline("Output {0}", variable);
```
Where each variable listed for input, is an increment of the number in curly braces
```C#
Console.Writeline("Output {0}, {1}, and {2}", var_1, var_2, var_3);
```
The colon in the brackets {0:C} is used to indicate additional formatting such as currency (C) or rounding numbers (F2, round to two decimal places).
---
