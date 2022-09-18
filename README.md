# C-Sharp-Survival-Guide


# Basic C# Syntax
#### Variables
```csharp
int a = 1;
int b = 2;
int c = a + b;
```
#### Arrays
```csharp
int[] array = new int[5];
array[0] = 1;
array[1] = 2;
array[2] = 3;
array[3] = 4;
array[4] = 5;
```
#### Loops
```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine(array[i]);
}
```
#### Conditionals
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
```csharp
static int Add(int a, int b)
{
    return a + b;
}
```

## Basics of Object Oriented Programming in C#

#### Classes
```csharp
class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}
```
#### Objects
```csharp
Person person = new Person();
person.Name = "John";
person.Age = 30;
```

