What is a variable?
A variable is a container for a specific kind of data.

An int is used to hold an integer value.

```C#
using System;

class Program
{
    static void Main()
    {
        int x = 5;

        x = x + 1;
        x++; // This is shorthand for x = x + 1

        Console.WriteLine("x = {0}", x);

        int y = 0;

        y++;

        Console.WriteLine("y = {0}", y);

        Console.ReadLine();
    }
}
```

Lab - What is a variable? (10 mins)
Make the following program compile and run:

```C#
using System;

class Program
{
    static void Main()
    {
        // Declare a variable named "age" of type "int"
        age;

        // Set the value of "age" to 21
        age;

        Console.WriteLine("My age is {0}", age);

        // increment age by 2
        age;

        Console.WriteLine("My real age is {0}", age);
        Console.ReadLine();
    }
}
```

```C#
using System;
//Mark Byers Lab Session 01/29/2019
class Program
{
    static void Main()
    {
        // Declare a variable named "age" of type "int"
        int age;

        // Set the value of "age" to 21
        age = 21;

        Console.WriteLine("My age is {0}", age);

        // increment age by 2
        age = age + 2;

        Console.WriteLine("My real age is {0}", age);
        Console.ReadLine();
    }
}
```
---

