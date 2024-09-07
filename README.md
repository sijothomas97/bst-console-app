# Binary Search Tree (BST) Console Application

## Introduction

This C# console application implements a binary search tree (BST) that supports integer and string data types. The application provides methods to insert nodes, traverse the tree (in-order, pre-order, post-order), check for the presence of a value, find the longest string in the tree, and identify the common ancestor of two strings.

### Key Features
- **Node and BinTree Classes**: Represent the nodes and structure of the binary search tree.
- **InsertItem**: Insert values into the tree, maintaining the binary search tree properties.
- **Traversal Methods**: Perform in-order, pre-order, and post-order traversals.
- **Contains Method**: Search for an integer in the tree and return `true` if the item exists, or `false` otherwise.
- **Longest Method**: For string trees, find the longest string present.
- **Ancestor Method**: Find the first common ancestor of two strings in the tree.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Classes and Methods](#classes-and-methods)
- [Examples](#examples)
- [Dependencies](#dependencies)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [License](#license)

## Features

1. **InsertItem**: Insert integers or strings into the tree in a manner consistent with binary search trees.
2. **Tree Traversal**:
   - In-order
   - Pre-order
   - Post-order
3. **Contains**: Search for a specific integer in the tree.
4. **Longest String**: Find the longest string in a binary tree of strings.
5. **Common Ancestor**: Find the first common ancestor of two strings in a binary tree.

## Installation

1. **Clone or Download the Project**:
   - Clone the repository:
     ```bash
     git clone https://github.com/your-username/bst-console-app.git
     ```
   - Or download the ZIP file and extract it to a folder on your computer.

2. **Open the Project in Visual Studio**:
   - Open the `.sln` file in Visual Studio.

3. **Build the Solution**:
   - In Visual Studio, click on `Build > Build Solution` or press `Ctrl+Shift+B` to compile the code.

4. **Run the Project**:
   - Press `F5` to run the application in Debug mode.

## Usage

The main functionality is accessed via the `Main()` method, which allows you to test the binary search tree's various features. After running the program, it will automatically insert items, traverse the tree, and test the `Contains`, `Longest`, and `Ancestor` methods.

### Example Menu:
- In `Main()`, the application:
  - Inserts integers into the tree.
  - Displays the in-order, pre-order, and post-order traversals.
  - Uses the `Contains` method to test for the presence of values.
  - For the string version, finds the longest string and the common ancestor of two strings.

### Sample Output:
```
In-order Traversal: 5 10 15 20 25 30
Pre-order Traversal: 20 10 5 15 30 25
Post-order Traversal: 5 15 10 25 30 20

Contains 15? True
Contains 50? False

Longest string in tree: "Artificial"
Common ancestor of "Binary" and "Tree": "Data"
```

## Classes and Methods

### 1. `Node<T>` Class
Represents each node in the binary search tree.
- **Fields**:
  - `Data`: The value of the node (either integer or string).
  - `Left`: Reference to the left child.
  - `Right`: Reference to the right child.

### 2. `BinTree<T>` Class
Manages the binary search tree operations.
- **InsertItem(T item)**: Inserts an item (integer or string) into the tree.
- **InOrder()**: Traverses the tree in-order.
- **PreOrder()**: Traverses the tree pre-order.
- **PostOrder()**: Traverses the tree post-order.
- **Contains(int item)**: Checks if a given integer exists in the tree.
- **Longest()**: (For string trees) Returns the longest string in the tree.
- **Ancestor(string str1, string str2)**: Finds the first common ancestor of two strings in the tree.

## Examples

### 1. Inserting and Traversing Integer Tree:
```csharp
BinTree<int> intTree = new BinTree<int>();
intTree.InsertItem(20);
intTree.InsertItem(10);
intTree.InsertItem(30);
intTree.InsertItem(5);
intTree.InsertItem(15);
intTree.InsertItem(25);

Console.WriteLine("In-order Traversal: ");
intTree.InOrder();  // Expected output: 5 10 15 20 25 30
```

### 2. Testing the `Contains` Method:
```csharp
Console.WriteLine("Contains 15? " + intTree.Contains(15));  // True
Console.WriteLine("Contains 50? " + intTree.Contains(50));  // False
```

### 3. String Tree Example:
```csharp
BinTree<string> stringTree = new BinTree<string>();
stringTree.InsertItem("Binary");
stringTree.InsertItem("Tree");
stringTree.InsertItem("Search");
stringTree.InsertItem("Artificial");
stringTree.InsertItem("Data");

Console.WriteLine("Longest string in tree: " + stringTree.Longest());  // "Artificial"
```

### 4. Finding the Common Ancestor:
```csharp
Console.WriteLine("Common ancestor of 'Binary' and 'Tree': " + stringTree.Ancestor("Binary", "Tree"));  // "Data"
```

## Dependencies
- **C# .NET Core**: Ensure you have the correct version of the .NET Core SDK installed for compiling and running the application.
- **Visual Studio**: This project is designed to be developed and run in Visual Studio.

## Troubleshooting

- **Binary Search Tree Errors**: Ensure that the input data is structured correctly and valid for the operations (e.g., integers or strings).
- **Contains Method**: If testing for an integer or string that does not exist, verify the insertion order or call the method after adding items.

## Contributors
- [sijothomas97](https://github.com/sijothomas97)

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
