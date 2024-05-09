# 19AI308-Object-Oriented-Programming-using-CSharp-Exp-10-File-Manipulation
Develop a C# program to get the values from the user using structure and store it in a file in a specific path using file stream concept
# AIM:
To develop a C# program using file streams.

# ALGORITHM:
#### Interface Definition:
          Define an interface named FileManipulation with two abstract methods: ReadFile and WriteToFile.
#### Class Implementation:
          Create a class named FileManager that implements the FileManipulation interface.
#### File Reading Method:
          Implement the ReadFile method in the FileManager class to read content from a specified file and display it to the user.
#### File Writing Method:
          Implement the WriteToFile method in the FileManager class to accept user input and write it to the specified file using StreamWriter.
#### Constructor Initialization:
          In the constructor of the FileManager class, prompt the user for the file name and the operation choice (read or write).
#### Operation Execution:
          Based on the user's choice, either invoke the ReadFile or WriteToFile method to perform the corresponding file manipulation operation.
#### Main Method Execution:
          In the Main method, create an instance of the FileManager class to initiate the file manipulation operations.
## PROGRAM :

### DEVELOPED BY : Mohanish K
### REG NO : 212222100028
```c#
using System;
using System.IO;

class Student
{
    public string Name { get; set; }
}

class Program
{
    static void Main(string[] args)
    {
        Student[] students = new Student[5];

        for (int i = 0; i < 5; i++)
        {
            Console.WriteLine("Enter name for student " + (i + 1) + ":");
            students[i] = new Student();
            students[i].Name = Console.ReadLine();
        }

        string path = @"C:\path\to\file.txt";
        using (StreamWriter sw = File.AppendText(path))
        {
            foreach (Student student in students)
            {
                sw.WriteLine(student.Name);
            }
        }

        Console.WriteLine("Contents of the file:");
        Console.WriteLine(File.ReadAllText(path));

        Console.ReadKey();
    }
}
```
# OUTPUT:
![image](https://github.com/Mohanish7777777/Exp-10-File-Manipulation/assets/111619160/763bc407-4664-47a4-9506-8b280a8d49a2)

![image](https://github.com/Mohanish7777777/Exp-10-File-Manipulation/assets/111619160/92942d84-fde1-421b-b3c6-134c83ea2110)

# RESULT:
This C# program allows users to enter student names, which are then saved to a text file named "file.txt" using StreamWriter. 
