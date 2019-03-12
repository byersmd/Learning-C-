**Boxing** is used to place known types (int, string, float, etc) into an object type
* An object can hold any type.
* An object is a **box** that you place known types in.
---
**Unboxing** is when you retrieve the contents of an object.
* To retrieve the contents of an object **you must first know what type is in the object**.
* If you box a float but then try to unbox it as an integer, you will get an error.
---
An **object** has four functions associated with it:
1. `Equals(object)` - Determines whether the two objects are equal
2. `GetHashCode( )` - Get's a hash value for the object
3. `GetType( )` - Get's the real type of the object
4. `ToString( )` - Returns a string that represents the type

```C#
using System;

class Program
{
    static void Main()
    {
        // This called boxing
        object box = 15;
        Console.WriteLine("The value inside the box is {0}", box);

        // Convert the object box to a string
        Console.WriteLine("The ToString of the box is {0}", box.ToString());

        // This is called unboxing - converting an object to an integer
        int number = (int)box;
        Console.WriteLine("Number is {0}", number);

        Console.ReadLine();
    }
}
```

[Reference](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/types/boxing-and-unboxing)
