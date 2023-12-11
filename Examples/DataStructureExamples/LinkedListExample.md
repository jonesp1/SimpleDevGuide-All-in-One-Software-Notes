# Linked List Example

### Examples of how to use linked lists

```csharp
// Declaration and Initialization
// Creates a linked list to store names
LinkedList<string> namesList = new LinkedList<string>();

// Adding Elements
// Adds names to the linked list
namesList.AddLast("Alice");
namesList.AddLast("Bob");
namesList.AddLast("Charlie");

// Displaying Elements
// Display names in the linked list
foreach (var name in namesList)
{
    Console.WriteLine(name);
}

// Inserting a new element
// Insert "Eve" after "Bob" in the list
LinkedListNode<string> bobNode = namesList.Find("Bob");
namesList.AddAfter(bobNode, "Eve");

// Displaying Elements after Insertion
Console.WriteLine("\nNames after Insertion:");
foreach (var name in namesList)
{
    Console.WriteLine(name);
}

// Removing an element
// Remove "Charlie" from the list
namesList.Remove("Charlie");

// Displaying Elements after Removal
Console.WriteLine("\nNames after Removal:");
foreach (var name in namesList)
{
    Console.WriteLine(name);
}

// Sample program: Using Linked List to Store and Display Names
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // Create a linked list to store names
        LinkedList<string> namesList = new LinkedList<string>();

        // Add names to the linked list
        namesList.AddLast("Alice");
        namesList.AddLast("Bob");
        namesList.AddLast("Charlie");
        namesList.AddLast("David");

        // Display names in the linked list
        Console.WriteLine("Names in the Linked List:");
        DisplayLinkedList(namesList);

        // Insert a new name in the middle of the list
        LinkedListNode<string> bobNode = namesList.Find("Bob");
        namesList.AddAfter(bobNode, "Eve");

        // Display names after insertion
        Console.WriteLine("\nNames after Insertion:");
        DisplayLinkedList(namesList);

        // Remove a name from the list
        namesList.Remove("Charlie");

        // Display names after removal
        Console.WriteLine("\nNames after Removal:");
        DisplayLinkedList(namesList);
    }

    // Helper method to display elements in the linked list
    static void DisplayLinkedList(LinkedList<string> linkedList)
    {
        foreach (var name in linkedList)
        {
            Console.WriteLine(name);
        }
    }
}

