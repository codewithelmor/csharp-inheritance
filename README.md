# Pillars of Object-Oriented Programming (OOP) - Inheritance

**`Inheritance`** is another fundamental concept in Object-Oriented Programming (OOP) that allows a class (the subclass or derived class) to inherit properties and behaviors from another class (the base class or parent class). Here's a simple example in C#:

```csharp
using System;

// Base class
class Animal
{
    public string Name { get; set; }

    // Constructor
    public Animal(string name)
    {
        Name = name;
    }

    public void Eat()
    {
        Console.WriteLine($"{Name} is eating.");
    }

    public void Sleep()
    {
        Console.WriteLine($"{Name} is sleeping.");
    }
}

// Derived class
class Dog : Animal
{
    public Dog(string name) : base(name)
    {
    }

    // Additional method specific to Dog
    public void Bark()
    {
        Console.WriteLine($"{Name} is barking.");
    }
}

class Program
{
    static void Main()
    {
        // Create an Animal object
        Animal genericAnimal = new Animal("Generic Animal");

        // Use methods from the base class
        genericAnimal.Eat();
        genericAnimal.Sleep();

        Console.WriteLine();

        // Create a Dog object
        Dog myDog = new Dog("Buddy");

        // Inherited methods from the base class
        myDog.Eat();
        myDog.Sleep();

        // Dog-specific method
        myDog.Bark();
    }
}
```

In this example:

* The **`Animal`** class is the base class, containing properties (**`Name`**) and methods (**`Eat`** and **`Sleep`**).
* The **`Dog`** class is the derived class, which inherits from the **`Animal`** class using **`: base(name)`** in the constructor. This means that a **`Dog`** object has all the properties and methods of an **`Animal`**, and it can also have additional members.
* The **`Dog`** class introduces a new method **`Bark`**, which is specific to dogs.

In the **`Main`** method:

* An **`Animal`** object is created, and its methods (**`Eat`** and **`Sleep`**) are called.
* A **`Dog`** object is created, and it inherits the methods from the **`Animal`** class. Additionally, the **`Bark`** method, specific to the **`Dog`** class, is called.

This demonstrates how inheritance allows for code reuse and the creation of specialized classes based on more general ones. The derived class inherits the properties and behaviors of the base class and can also add new members or override existing ones to tailor the behavior to its specific needs.
