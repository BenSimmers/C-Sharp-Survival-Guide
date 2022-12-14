# C-Sharp-Survival-Guide

This is a collection of notes and code snippets that have been made for myself to help me re-learn C# and begin learning ASP.NET and hopefully other C# based methodologies and frameworks. I hope that it will be useful to others as well.
Uses some of the content from QUT CAB201 Programming Principles in C#.
*Feel free to make Pull Request if you see that anything needs to be added.* 


#### Contributors:
[irls-svg](https://github.com/irls-svg)

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

**Differences between char and string**
```csharp
char a = 'a';
string b = "a";
```
The difference between char and string is that char is a single character and string is a sequence of characters. The char data type is used to store a single character. The string data type is used to store a sequence of characters (text). A string variable can contain a maximum of 2 billion characters.

**Differences between int, float, double, long**
* int is a 32-bit signed integer
* long is a 64-bit signed integer
* float is a single-precision 32-bit floating point number
* double is a double-precision 64-bit floating point number

**when to use int, float, double, long**
* int is used for whole numbers
* long is used for whole numbers that are larger than int
* float is used for decimal numbers
* double is used for decimal numbers that are larger than float

**difference between signed and unsigned variables**
* signed variables can be positive or negative
* unsigned variables can only be positive




#### Operators
Operators are used to perform operations on variables and values. These are known as simple operators. There are also assignment operators, which are used to assign values to variables. The following lists the most common operators in C#:
```csharp
int a = 1;
int b = 2;
int c = a + b;
int d = a - b;
int e = a * b;
int f = a / b;
int g = a % b;

// +=, -=, *=, /=, %= are also available
int a = 1;
int b = 2;
int c = a + b;
c += a; // c = c + a;
c -= a; // c = c - a;
c *= a; // c = c * a;
c /= a; // c = c / a;
c %= a; // c = c % a;

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
#### Functions/Methods
Functions are used to perform certain actions, and they are also called methods.
```csharp
static int Add(int a, int b)
{
    return a + b;
}
```

#### Uses of `Readline();`
`Readline()` is a powerful tool in C#, it allows the program to read an input from a user, furthermore it can also help when converting variables of different types. e.g.  String to Int or float to int.



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
    //the original variable called `name`
    private string name;
    public string Name 
    /**creating a property called Name which will  use the
    `name` variable to compute, change or read.
    */
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
            Person person = new Person(); //object instance of a class
            person.Name = "John"; //object.variable name
            person.Age = 30;//object.variable name
            person.Greet();//object. name

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




## Basics of C# Collections 

#### List
List is used to store a collection of objects.

what are lists used for?
Lists are used to store a collection of objects. They are very similar to arrays, but they are more flexible because the size of a list can be changed after it is created. Lists are also known as generic lists because they can store a list of objects of a specific type.

```csharp
List<int> list = new List<int>();
list.Add(1);
list.Add(2);
list.Add(3);
list.Add(4);
list.Add(5);
```

#### Dictionary
Dictionary is used to store a collection of key/value pairs.

What are dictionaries used for?
Dictionaries are used to store data values in key/value pairs. A dictionary is a collection which is unordered, changeable and indexed. In Python dictionaries are written with curly brackets, and they have keys and values.

Why are dictionaries used?
Dictionaries are used when we want to quickly retrieve the data without any specific order. Dictionaries are optimized to retrieve values when the key is known.

```csharp
Dictionary<string, string> dictionary = new Dictionary<string, string>();   
dictionary.Add("1", "One");
dictionary.Add("2", "Two");
dictionary.Add("3", "Three");
dictionary.Add("4", "Four");

foreach (KeyValuePair<string, string> pair in dictionary)
{
    Console.WriteLine(pair.Key + " " + pair.Value);
}
```

#### OOP with Collections
```csharp
using System;
using System.Collections.Generic;

namespace OOP
{
    class Program
    {
        static void Main(string[] args)
        {
            List<Person> people = new List<Person>();
            people.Add(new Person { Name = "John", Age = 30 });
            people.Add(new Person { Name = "Mary", Age = 20 });
            people.Add(new Person { Name = "Steve", Age = 50 });

            foreach (Person person in people)
            {
                Console.WriteLine(person.Name + " " + person.Age);
            }
        }
    }

    class Person
    {
        public string Name { get; set; }
        public int Age { get; set; }
    }
}
```


# Other Stuff
### ASP.NET
ASP.NET is a web application framework developed and marketed by Microsoft to allow programmers to build dynamic web sites, web applications and web services. It was first released in January 2002 with version 1.0 of the .NET Framework, and is the successor to Microsoft's Active Server Pages (ASP) technology.

### ASP.NET Core
ASP.NET Core is the next generation of ASP.NET. It is a modular framework that runs on both the full .NET Framework, on Windows, and the cross-platform .NET Core.

### ASP.NET MVC
ASP.NET MVC is a web application framework developed by Microsoft, which implements the model???view???controller (MVC) pattern. It is open-source software, apart from the ASP.NET Web Forms component which is proprietary.

### ASP.NET Web API
ASP.NET Web API is a framework that makes it easy to build HTTP services that reach a broad range of clients, including browsers and mobile devices. ASP.NET Web API is an ideal platform for building RESTful applications on the .NET Framework.


### REST API
REST (REpresentational State Transfer) is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other. REST-compliant systems, often called RESTful systems, are characterized by how they are stateless and separate the concerns of client and server.




## Blazor
## Web Assembly 

