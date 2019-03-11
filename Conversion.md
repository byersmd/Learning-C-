**Data Type Conversion**

All the numeric types have a Parse function that converts a string into the appropriate type.
The `Parse` method returns the converted number;

input must "look" like an integer
    if it doesn't the Parse() function will fail.

```C#
// Byers, Mark
using System;

class Program
{
    static void Main()
    {
        // Display "Enter a price:" using Console.Write
        Console.Write("Enter a price ");
        // Define a string named "input"
        string input;
        // Assign "input" to Console.ReadLine() to allow the user to enter a price
        input = Console.ReadLine();
        // Define a double named price
        double price;
        // Convert the "input" into a double using Parse()
        price = int.Parse(input);
        // Display the price as currency ( {0:C} )
        Console.Write("Price {0:c}", price);
        Console.ReadLine();
    }
}
```
Converting ANY type to a string is trivial
    because EVERY type supports `ToString()`

|Numeric | Type	Method |
| --- | --- |
| decimal |	ToDecimal(String) |
| float |	ToSingle(String) |
| double | ToDouble(String) |
| short |	ToInt16(String) |
| int |	ToInt32(String) |
| long | ToInt64(String) |
| ushort | ToUInt16(String) |
| uint | ToUInt32(String) |
| ulong | ToUInt64(String) |


[Reference](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/types/how-to-convert-a-string-to-a-number)
