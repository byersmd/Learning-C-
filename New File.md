The format of a new **C#** program is:
```C#
using System;

namespace Setup
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            
        }
    }
}

```

The `namespace` is not required for the program to run.

All **C#** programs must have a `Main`. 

Each program must return an object unless it is the `Main` which may return `void`.

---
You can comment a line with double `//`

---

In order to have a user input use `var = Console.ReadLine();` and convert to a number using `.Parse()`
```C#
// Byers, Mark
using System;

class Program
{
    static void Main()
    {
        Console.Write("User Input");
          // Define a string named "input"
        string input;
          // Assign "input" to Console.ReadLine() to allow the user to enter an input
        var = Console.ReadLine();
          // Convert the "input" into a double using Parse()
        price = int.Parse(var);
    }
}
```
