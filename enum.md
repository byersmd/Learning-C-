**Enumeration Types**

An enum is a set of distinct named constants. 

---
By default, the first enumerator has the value 0, and the value of each successive enumerator is increased by 1. 

Enumerators can use initializers to override the default values

You can also assign non-unique values for the enum.

```C#
enum DaysPerMonth
{
    January = 30,
    February = 30,
    March = 30,
    April = 30,
    May = 30,
}

```

---

Usually it is best to define an enum directly within a namespace so that all classes in the namespace can access it with equal convenience. However, an enum can also be nested within a class or struct.

