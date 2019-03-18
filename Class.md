**Classes**

```C#
using System;

class VerySimple //classes are treated similar to objects, they provide definition and functionality
{
   //fields (data)
   int simpleValue;
   
   //constructor
   public VerySimple()
   {
      simpleValue = 10;
   }
   
   //methods with -or- without parameters
   
   //properties
   
   //enums

}
```

A `class` is synonymous with `type`

Constructors have the look of a method but return nothing. They are used as **initializers**
A constructor **MUST** have the same name as the class it is created in.

making use of a class is called **instantiation**


Classes are called upon in one another by creating the object (instantiation)

```C#
class VerySimple //This class is the "toolbox"
{}

class TestVerySimpleClass //This class uses the `VerySimple` class via instantiation
{
   static void Main() //starting point for the compiler
   {
      //To use the `VerySimple` class, the object of type `VerySimple` class must be created
      
      VerySimple ver; // where `ver` is any chosen new name to create an object 
                      // based on the "toolbox" class called `VerySimple`
                      // the new object named `ver` is null | just like defining a new type
      
      // The full instantiation now requires using the `new` keyword
      // to call on the constructor `VerySimple()`
      ver = new VerySimple();
   }
}
```

A Classs instantiation may be simplified in **one line** as follows:
```C#
class VerySimple
{

}
class TestVerySimpleClass
   static void Main()
   {
      
      VerySimple ver = new VerySimple();
   }
}
```
