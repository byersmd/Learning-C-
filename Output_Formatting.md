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
The colon in the brackets `{0:_}` is used to indicate additional formatting

| Format specifier	| Description	| Examples |	Result |
| ----------------- | ----------- | -------- | ------- |
| C or c	          | Currency string | `s = $"{2.5:C}";` | $2.50 |
| C or c	          | Currency string | `s = $"{-2.5:C}";` | ($2.50) |
| D or d	          | Decimal	string  | `s = $"{25:D5}";` |	00025 |
| E or e	          | Exponential	string | `s = $"{250000:E2}";` |	2.50E+005 |
| F or f	          | Fixed-point	string | `s = $"{2.5:F2}";` | 2.50 |
| F or f	          | Fixed-point	string | `s = $"{2.5:F0}";` | 3 |
| G or g	          | General	string | `s = $"{2.5:G}";` |	2.5 |
| N or n	          | Numeric	string | `s = $"{2500000:N}";` | 	2,500,000.00 |
| P or p	          | Percent	string | `s = $"{0.25:P}";` |	25.00% |
| R or r	          | Round-trip	string  | `s = $"{2.5:R}";`	| 2.5 |
| X or x	          | Hexadecimal	string | `s = $"{250:X}";` | FA |
| X or x	          | Hexadecimal	string | `s = $"{0xffff:X}";` | FFFF |

You use a format specifier to create a format string. The format string is of the following form: `Axx`, where

`A` is the format specifier, which controls the type of formatting applied to the numeric value.
`xx` is the precision specifier, which affects the number of digits in the formatted output. The value of the precision specifier ranges from 0 to 99.

You can format the amount of spaces the output uses or left & right align, e.g. `{0,-5:F2}` will display the variable with space for `5` digits aligned to the **left**, with `2` digits trailing the decimal

---
