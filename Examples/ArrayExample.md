# Array Example:


### Examples of how to use arrays

```csharp
// Declaration and Initialization
// Creates an integer array with a size of 5
int[] myArray = new int[5]; 

// Accessing Elements
// Assigns 10 to the first element
myArray[0] = 10; 

// Retrieves the value at index 2
int value = myArray[2];

// Iterating Through an Array
for (int i = 0; i < myArray.Length; i++)
{
    // Access and process each element
    Console.WriteLine(myArray[i]);
}

// Array Length
// Gets the length of the array
int arrayLength = myArray.Length; 

// Example: Sample program 
// Storing and Displaying Temperatures
using System;

class Program
{
    static void Main()
    {
        // Declare and initialize an array to store temperatures
        double[] temperatures = new double[7];

        // Assign values to each day's temperature
        temperatures[0] = 25.5;
        temperatures[1] = 28.0;
        temperatures[2] = 24.8;
        temperatures[3] = 26.2;
        temperatures[4] = 27.5;
        temperatures[5] = 23.7;
        temperatures[6] = 22.9;

        // Display temperatures for each day
        Console.WriteLine("Weekly Temperatures:");

        for (int day = 0; day < temperatures.Length; day++)
        {
            Console.WriteLine($"Day {day + 1}: {temperatures[day]}°C");
        }
    }
}
