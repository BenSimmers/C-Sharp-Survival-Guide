# C-Sharp-Survival-Guide


# Basic C# Syntax
#### Variables
What are variables? Variables are containers for storing data values. In C#, there are different types of variables, for example a string variable, which can contain a text value:
```csharp
int a = 1;
int b = 2;
int c = a + b;



// Variables can be declared without an initial value
int a; or int a = 0;
string b; or string b = "Hello World";
string name = "John";
string greeting = "Hello " + name;



//long and short are also available
long a = 1000000000000000000;
short b = 10000;

//double and float are also available
double a = 1.5;
float b = 1.5f;

//bool is also available
bool a = true;
bool b = false;

```

#### Arrays
Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.
```csharp
int[] array = new int[5];
array[0] = 1;
array[1] = 2;
array[2] = 3;
array[3] = 4;
array[4] = 5;
```
#### Loops
Loops are used to execute a block of code a number of times.
```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine(array[i]);
}
```
#### Conditionals
Conditionals are used to perform different actions based on different conditions.
```csharp
if (a == 1)
{
    Console.WriteLine("a is 1");
}
else if (a == 2)
{
    Console.WriteLine("a is 2");
}
else
{
    Console.WriteLine("a is not 1 or 2");
}
```
#### Switch
Switch is used to perform different actions based on different conditions.
```csharp
switch (a)
{
    case 1:
        Console.WriteLine("a is 1");
        break;
    case 2:
        Console.WriteLine("a is 2");
        break;
    default:
        Console.WriteLine("a is not 1 or 2");
        break;
}
```
#### Functions
Functions are used to perform certain actions, and they are also called methods.
```csharp
static int Add(int a, int b)
{
    return a + b;
}
```

## Basics of Object Oriented Programming in C#

#### Classes
Classes are used to create objects, and they are the basic building blocks of OOP.
```csharp
class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}
```
#### Objects
Objects are created from classes, and they can contain data in fields, and code in methods.
```csharp
Person person = new Person();
person.Name = "John";
person.Age = 30;
```


#### Inheritance
Inheritance is used to form new classes using classes that have already been defined.
```csharp
class Student : Person
{
    public int Grade { get; set; }
}
```

#### Polymorphism
Polymorphism is used to perform a single action in different ways.
```csharp
class Person
{
    public virtual void Greet()
    {
        Console.WriteLine("Hello");
    }
}

class Student : Person
{
    public override void Greet()
    {
        Console.WriteLine("Hello Student");
    }
}
```

#### Encapsulation
Encapsulation is used to restrict access to methods and variables. This can prevent the accidental modification of data. To achieve this, you must declare variables of a class as private (cannot be accessed by an object outside the class) and provide public get and set methods to access and update the value of a private variable.
```csharp
class Person
{
    private string name;
    public string Name
    {
        get { return name; }
        set { name = value; }
    }
}
```

#### Abstraction
Abstraction is used to hide the internal details and show only the functionalities. In other words, it shows only essential things to the user and hides the internal details for example there is a remote you know only switch on and off but you don't know what internal mechanism is working in the remote.
```csharp
abstract class Shape
{
    public abstract void Draw();
}
```

#### Interfaces
Interfaces are used to achieve abstraction. They can contain only the declaration of methods, not the implementation. It is used to achieve abstraction and multiple inheritance in C#.
```csharp
interface IShape
{
    void Draw();
}
```

#### Access Modifiers
Access modifiers are used to set the accessibility of classes, methods, and variables.
```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}
```
#### Static
Static is used to create class members (fields, methods, properties, etc.) that belong to the class rather than the object of a class.
```csharp
class Person
{
    public static int Count { get; set; }
}
```

#### Properties
Properties are used to provide a flexible mechanism to read, write, or compute the value of a private field.
```csharp
class Person
{
    private string name;
    public string Name
    {
        get { return name; }
        set { name = value; }
    }
}
```


#### Indexers
Indexers are used to create classes and structs that can be indexed just like arrays.
```csharp
class Person
{
    private string[] names = new string[10];
    public string this[int index]
    {
        get { return names[index]; }
        set { names[index] = value; }
    }
}
```



#### A simple example of OOP in C#
```csharp
using System;

namespace OOP
{
    class Program
    {
        static void Main(string[] args)
        {
            Person person = new Person();
            person.Name = "John";
            person.Age = 30;
            person.Greet();

            Student student = new Student();
            student.Name = "Mary";
            student.Age = 20;
            student.Grade = 10;
            student.Greet();
        }
    }

    class Person
    {
        public string Name { get; set; }
        public int Age { get; set; }

        public virtual void Greet()
        {
            Console.WriteLine("Hello");
        }
    }

    class Student : Person
    {
        public int Grade { get; set; }

        public override void Greet()
        {
            Console.WriteLine("Hello Student");
        }
    }
}
```
