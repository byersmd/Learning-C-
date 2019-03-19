A `constructor` is a function with no return type and with the same name as the class.

By default, when an object is instantiated all fields are initialized to zero. Constructors enable the programmer to set default values, limit instantiation, and write code that is flexible and easy to read.

```C#
using System;

class Point
    {
    public int X;
    public int Y;

    // public Constructor
    public Point(int x, int y)
        {
        X = x;
        Y = y;
        }
    }

class TestPointClass
{
    static void Main()
    {
        Point pt = new Point(10,20);
            
        Console.WriteLine("{0},{1}", pt.X, pt.Y);
    }
}
```

---

A `struct` type is a value type that is typically used to encapsulate small groups of related variables, such as the coordinates of a rectangle or the characteristics of an item in an inventory. 

```C#
public struct Book
{
    public decimal price;
    public string title;
    public string author;
}
```

A `struct` is actually a lightweight class. It can have constructors, constants, methods, and so forth.

The difference between a **struct** and a **class** is that you don't need to call new unless there is a constructor. You also cannot inherit from a struct nor can a struct inherit from another type.
struct members cannot be declared as `protected`.
Since structures are stack-based no additional references are necessary for the garbage collector.


[Ref](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/using-structs)
