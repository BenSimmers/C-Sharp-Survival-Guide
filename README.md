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